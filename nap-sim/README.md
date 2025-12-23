# Nap Simulation Home Assistant Add-on

This add-on exposes the Nap simulator container behind Home Assistant's Supervisor. The configuration expects that you publish a multi-architecture Docker image for the application (see `docs/DEPLOY_HOME_ASSISTANT.md` in the root of this repo).

## Configuration

| Option | Type | Description |
| --- | --- | --- |
| `slack_alerts_enabled` | bool | Toggle Slack notifications inside the container. |
| `slack_token` | str | Slack Bot/User token (optional). |
| `slack_channel_id` | str | Channel ID that should receive alerts. |

The add-on writes cache files under `/share/nap-cache`. Use Home Assistant secrets to store sensitive values if you publish this repository.
