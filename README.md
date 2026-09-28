# Heimdall Research status

Public uptime monitor and status page for Heimdall Research.

- Status page: https://status.heimdallresearch.com
- Source: this repository ([Upptime](https://github.com/upptime/upptime), MIT License)
- Checks run every five minutes via GitHub Actions

## Monitored endpoints

| Name | URL |
| --- | --- |
| Website | https://heimdallresearch.com |
| API | https://api.heimdallresearch.com/healthz |
| App | https://app.heimdallresearch.com |

Docs (`https://docs.heimdallresearch.com`) stay paused until October launch. The entry is commented out in `.upptimerc.yml`.

Do not list staging or Railway addresses here.

## Downtime alerts

Email to `engineering@heimdallresearch.com` via Resend SMTP (`smtp.resend.com`). From address: `status@notify.heimdallresearch.com`.

## Repository secrets

Required Actions secrets (set with `gh secret set NAME --repo heimdallresearch/status`):

| Secret | Purpose |
| --- | --- |
| `GH_PAT` | Fine-grained PAT for Contents, Issues, Actions and Workflows (read/write); Metadata (read). Resource owner `heimdallresearch`, repository `status` only. |
| `NOTIFICATION_EMAIL` | `true` |
| `NOTIFICATION_EMAIL_FROM` | `status@notify.heimdallresearch.com` |
| `NOTIFICATION_EMAIL_TO` | `engineering@heimdallresearch.com` |
| `NOTIFICATION_EMAIL_SMTP` | `true` |
| `NOTIFICATION_EMAIL_SMTP_HOST` | `smtp.resend.com` |
| `NOTIFICATION_EMAIL_SMTP_PORT` | `465` |
| `NOTIFICATION_EMAIL_SMTP_USERNAME` | `resend` |
| `NOTIFICATION_EMAIL_SMTP_PASSWORD` | Resend API key |

### GH_PAT expiry reminder

Create the fine-grained token with a one-year expiry. Target renewal date: **2027-09-28**. Rotate before that date and update the secret.

## License

This repository is based on [Upptime](https://github.com/upptime/upptime), distributed under the MIT License. See [LICENSE](./LICENSE).
