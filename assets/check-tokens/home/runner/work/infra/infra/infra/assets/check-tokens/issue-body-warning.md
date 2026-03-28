## Why is this issue open?

The automated [token expiration check](https://github.com/{{ .repoFullName }}/actions/runs/{{ .runId }}) detected that `{{ .tokenSecret }}` is expiring soon.

| Field | Value |
|-------|-------|
| **Token** | `{{ .tokenSecret }}` (`{{ .tokenName }}`) |
| **Status** | `warning` — expiring soon |
| **Days remaining** | {{ .daysLeft }} |
| **Expiration date** | {{ .expirationDate }} |

## Action required

Please rotate this token before it expires. There is no immediate outage, but workflows depending on this secret will start failing on **{{ .expirationDate }}**.

1. Generate a new classic PAT for the token owner at `https://github.com/settings/tokens`
2. Update the `{{ .tokenSecret }}` secret in the repository (or organization) settings
3. Close this issue once the new token is in place

## Related issues
**Issue URL(s)**: N/A
