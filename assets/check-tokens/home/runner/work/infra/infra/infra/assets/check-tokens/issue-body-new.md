## Why is this issue open?

The automated [token expiration check](https://github.com/{{ .repoFullName }}/actions/runs/{{ .runId }}) detected that `{{ .tokenSecret }}` is **{{ .tokenStatus }}**.

| Field | Value |
|-------|-------|
| **Token** | `{{ .tokenSecret }}` (`{{ .tokenName }}`) |
| **Status** | `{{ .tokenStatus }}` |
| **Days remaining** | {{ .daysLeft }} |
| **Expiration date** | {{ .expirationDate }} |

## Action required

1. Generate a new classic PAT for the token owner at `https://github.com/settings/tokens`
2. Update the `{{ .tokenSecret }}` secret in the repository (or organization) settings
3. Close this issue once the new token is in place

## Related issues
**Issue URL(s)**: N/A
