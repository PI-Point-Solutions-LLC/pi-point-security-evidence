# Smokeball API Security Evidence

Reviewed source provenance: private application repository, commit `c0d740c9231650cb4fd10db0b21561639985aebe`, plus subsequent Smokeball hardening work where identified. Full source is private; sanitized excerpts below contain no credentials or customer data.

## D1 — Use case and data scope

PI Point's Smokeball integration supports authorized OAuth/SSO/custom-action launches, Matter context, contacts, document metadata/content, PI Point assignments linked to a Matter, controlled document exchange, messages, invoices/payments and write-back.

The shared integration types and field allowlists define minimized Matter, contact and document fields. Representative private-source paths:

- `supabase/functions/_shared/smokeball.ts`
- `supabase/functions/smokeball-list-matters/index.ts`
- `supabase/functions/smokeball-get-matter/index.ts`
- `supabase/functions/smokeball-list-matter-contacts/index.ts`
- `supabase/functions/smokeball-list-matter-documents/index.ts`

Sanitized representative field allowlist:

```text
Matter list: id, display number, description, status, updated timestamp,
client identifier/name, and practice-area identifier/name.

Contact list: identifier, Matter identifier/number, name components,
relationship/type, primary email/phone, and updated timestamp.

Document list: identifier, name/filename, type/content type, size,
lock state, and lifecycle timestamps.
```

This public record corroborates design intent. Controlled full-source review or test-output attachment is required to corroborate the complete current implementation.

## D2 — Token and secret storage

The private source implements AES-GCM encryption of OAuth secrets before storage. Sanitized excerpt from `supabase/functions/_shared/smokeball.ts`:

```typescript
const key = await crypto.subtle.importKey(
  "raw",
  await crypto.subtle.digest("SHA-256", new TextEncoder().encode(secret)),
  { name: "AES-GCM" },
  false,
  ["encrypt", "decrypt"],
);

const iv = crypto.getRandomValues(new Uint8Array(12));
const ciphertext = await crypto.subtle.encrypt(
  { name: "AES-GCM", iv },
  key,
  new TextEncoder().encode(value),
);
```

The server-only connection schema stores `access_token_ciphertext` and `refresh_token_ciphertext`; the required encryption key is read from a server-side environment secret and is not returned to browser clients.

Production corroboration requires the redacted Supabase secret-name and schema attachments listed in the [provider attachment register](provider-console-attachments-required.md).

## D3 — Backend-only request path

Architecture:

```text
Authorized browser user
        |
        | HTTPS request; PI Point session / signed launch context
        v
Supabase Edge Function
        |
        | validates authorization and retrieves/decrypts server-side token
        | server-to-server HTTPS request
        v
Smokeball OAuth / API
```

Smokeball API key, client secret, token-encryption key, refresh token and Supabase service-role credential remain in backend runtime configuration. Representative private-source paths:

- `supabase/functions/_shared/smokeball-config.ts`
- `supabase/functions/smokeball-start-oauth/index.ts`
- `supabase/functions/smokeball-oauth-callback/index.ts`
- `supabase/functions/smokeball-get-matter/index.ts`

## D4 — Additional API safeguards

Documented/implemented safeguards include:

- production HTTPS/TLS endpoints;
- OAuth state, nonce and PKCE validation where applicable;
- signed, short-lived Matter launch context;
- tenant/user/Matter/assignment authorization and scoped database access;
- API rate-limit/error handling;
- server-only credentials and OAuth-token encryption;
- redaction/avoidance of raw tokens, authorization headers and unnecessary sensitive payloads in logs;
- controlled document transfer with signed/short-lived access paths;
- AI separation: optional PI Point CRM AI does not use Smokeball Matter data.

Public policy corroboration:

- [Security Policy](https://app.pipointsolutions.com/security)
- [AI Usage Policy](https://app.pipointsolutions.com/ai-usage-policy)
- [Vulnerability Disclosure](https://app.pipointsolutions.com/vulnerability-disclosure)

Passing private integration-test output should be supplied as a redacted attachment if Smokeball requires operating evidence rather than design/source evidence alone.
