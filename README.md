# CS-Aggressor-Kit
Homemade aggressor scripts kit for Cobalt Strike

## Table of Contents
- [CS-Aggressor-Kit](#cs-aggressor-kit)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
  - [Alert](#alert)

## Summary

The following table illustrates all the CNA files included in this project:

| Section | Name | Description |
|:-----------:|:-----------:|:-----------:|
| Alert |[slack-alerts_linux.cna](/Alert/Slack/slack-alerts_linux.cna)| Slack CNA file for Linux CS client |
| Alert |[slack-alerts_windows.cna](/Alert/Slack/slack-alerts_windows.cna)| Slack CNA file for Windows CS client |
| Alert |[discord-alerts_linux.cna](/Alert/Discord/discord-alerts_linux.cna)| Discord CNA file for Linux CS Client |
| Alert |[teams-alerts_linux.cna](/Alert/Teams/teams-alerts_linux.cna)| Teams CNA file for Linux CS Client |

## Alert

These CNA files will notify you via the `Slack`/`Discord`/`Teams` applications when:

- A new client connects to the team server.
- A CS client disconnects from the team server.
- A new incoming beacon.
- A new web hit occurs.
- A CS client posts something in the event log.
- New site hosts.
- New credentials come in from keylogging.
- A new screenshot is taken from Cobalt Strike.

:information_source: Some CNA files are compatible with both Windows and Linux operating systems.

The following table illustrates the CNA files included in the Alert section:

| Name | OS | App | Description |
|:-----------:|:-----------:|:-----------:|:-----------:|
|[slack-alerts_linux.cna](/Alert/Slack/slack-alerts_linux.cna)| Linux | Slack | Slack CNA file for Linux CS client |
|[slack-alerts_windows.cna](/Alert/Slack/slack-alerts_windows.cna)| Windows | Slack | Slack CNA file for Windows CS client |
|[discord-alerts_linux.cna](/Alert/Discord/discord-alerts_linux.cna)| Linux | Discord | Discord CNA file for Linux CS Client |
|[teams-alerts_linux.cna](/Alert/Teams/teams-alerts_linux.cna)| Linux | Teams | Teams CNA file for Linux CS Client |

### Setup Slack and Webhooks

:information_source: To set up a Slack server and webhook, you can follow these guides provided on the [Slack website](https://api.slack.com/incoming-webhooks).

### Setup Discord and Webhooks

:information_source: To set up a Discord server and webhook, you can follow these guides provided on the [Discord website](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).

### Setup Teams Webhooks

:information_source: To set up a Microsoft Teams webhook, you can follow these guides provided on [Microsoft website](https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook?tabs=newteams%2Cdotnet).
