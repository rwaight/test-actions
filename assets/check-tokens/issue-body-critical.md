## Why is this issue open?

The automated [token expiration check](https://github.com/{{ .repoFullName }}/actions/runs/{{ .runId }}) detected that `{{ .tokenSecret }}` is expiring **critically soon** and must be rotated immediately.

| Field | Value |
|-------|-------|
| **Token** | `{{ .tokenSecret }}` (`{{ .tokenName }}`) |
| **Status** | `critical` — rotate immediately |
| **Days remaining** | {{ .daysLeft }} |
| **Expiration date** | {{ .expirationDate }} |

## Action required

**{{ .daysLeft }} day(s) remaining.** Any workflows using this secret will fail after **{{ .expirationDate }}**.

1. Generate a new classic PAT for the token owner at `https://github.com/settings/tokens`
2. Update the `{{ .tokenSecret }}` secret in the repository (or organization) settings
3. Verify dependent workflows are running successfully after the rotation
4. Close this issue once the new token is in place

## Related issues
**Issue URL(s)**: N/A
