## Why is this issue open?

The automated [token expiration check](https://github.com/{{ .repoFullName }}/actions/runs/{{ .runId }}) detected that `{{ .tokenSecret }}` has **expired or been revoked**. Workflows depending on this secret are likely failing now.

| Field | Value |
|-------|-------|
| **Token** | `{{ .tokenSecret }}` (`{{ .tokenName }}`) |
| **Status** | `expired` — workflows are broken |
| **Days remaining** | 0 |
| **Expiration date** | {{ .expirationDate }} |

## Action required

**This is urgent.** Any workflow using `{{ .tokenSecret }}` is returning HTTP 401 and failing silently or erroring out.

1. Generate a new classic PAT for the token owner at `https://github.com/settings/tokens`
2. Update the `{{ .tokenSecret }}` secret in the repository (or organization) settings
3. Re-run any workflows that failed due to the expired token
4. Verify dependent workflows are running successfully after the rotation
5. Close this issue once the new token is in place and workflows are healthy

## Related issues
**Issue URL(s)**: N/A
