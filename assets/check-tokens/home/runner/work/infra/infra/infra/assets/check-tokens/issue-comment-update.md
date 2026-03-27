## Token expiration update

| Field | Value |
|-------|-------|
| **Status** | `{{ .tokenStatus }}` |
| **Days remaining** | {{ .daysLeft }} |
| **Expiration date** | {{ .expirationDate }} |
| **Token** | `{{ .tokenSecret }}` (`{{ .tokenName }}`) |
| **Checked at** | {{ .runId }} ([view run](https://github.com/{{ .repoFullName }}/actions/runs/{{ .runId }})) |

Please rotate `{{ .tokenSecret }}` and update the secret in the repo/org settings.
