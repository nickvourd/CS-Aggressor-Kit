# CS-Aggressor-Kit
Homemade Aggressor scripts kit for Cobalt Strike

## Table of Contents
- [CS-Aggressor-Kit](#cs-aggressor-kit)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
  - [Alert](#alert)
  - [Misc](#misc)

## Summary

The following table illustrates all the CNA files included in this project:

| Section | Name | Description |
|:-----------:|:-----------:|:-----------:|
| Alert |[slack-alerts_linux.cna](/Alert/Slack/slack-alerts_linux.cna)| Slack CNA file for Linux CS client |
| Alert |[slack-alerts_windows.cna](/Alert/Slack/slack-alerts_windows.cna)| Slack CNA file for Windows CS client |
| Alert |[discord-alerts_linux.cna](/Alert/Discord/discord-alerts_linux.cna)| Discord CNA file for Linux CS Client |
| Alert |[teams-alerts_linux.cna](/Alert/Teams/teams-alerts_linux.cna)| Teams CNA file for Linux CS Client |
| Alert |[mattermost-alerts_linux.cna](/Alert/Mattermost/mattermost-alerts_linux.cna)| Mattermost CNA file for Linux CS Client |
| Alert |[mattermost-alerts_windows.cna](/Alert/Mattermost/mattermost-alerts_windows.cna)| Mattermost CNA file for Windows CS Client |
| Misc | [Beacon-Name-Tab.cna](/Misc/Beacon-Name-Tab.cna) | Changes Beacon tab name format from default to "/<username/>@<hostname> (<pid>)" |
| Misc | [Beacon-Name-Tab-Colors.cna](/Misc/Beacon-Name-Tab-Colors.cna) | Changes Beacon tab name format from default to "<username>@<hostname> (<pid>)", for admin's beacon the color is red, for user's beacon the color is green |
| Misc | [CS-All-Tabs-Bold.cna](/Misc/CS-All-Tabs-Bold.cna) | Makes all CS client tabs bold |
| Misc | [CWD-Beacon-Bar.cna](/Misc/CWD-Beacon-Bar.cna) | Enhances Beacon console status bar to display the Beacon's last known working directory path. Additionally, improves the 'cd' command to support restoring the previous directory path seamlessly (Usage: cd -) |

## Alert

These CNA files will notify you via the `Slack`/`Discord`/`Teams`/`Mattermost` applications when:

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
|[mattermost-alerts_linux.cna](/Alert/Mattermost/mattermost-alerts_linux.cna)| Linux | Mattermost | Mattermost CNA file for Linux CS Client |
|[mattermost-alerts_windows.cna](/Alert/Mattermost/mattermost-alerts_windows.cna)| Windows | Mattermost | Mattermost CNA file for Windows CS Client |

### Setup Slack and Webhooks

:information_source: To set up a Slack server and webhook, you can follow these guides provided on the [Slack website](https://api.slack.com/incoming-webhooks).

### Setup Discord and Webhooks

:information_source: To set up a Discord server and webhook, you can follow these guides provided on the [Discord website](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).

### Setup Teams Webhooks

:information_source: To set up a Microsoft Teams webhook, you can follow these guides provided on [Microsoft website](https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook?tabs=newteams%2Cdotnet).

### Setup Mattermost Webhooks

:information_source: To set up a Mattermost webhook, you can follow these guides provided on [Mattermost website](https://developers.mattermost.com/integrate/webhooks/incoming/).

## Example Alert CNA Output

#### New incoming Beacon notification example (Slack):

![New-Beacon-Example](/Pictures/New-Beacon-Example1.png)

#### New Web hit notification example (Discord):

![Web-Hit-Example](/Pictures/Web-Hit-Example1.png)

#### New CS client connects to the teamserver notification example (Slack):

![New-CS-Client-Connect-Example](/Pictures/New-CS-Client-Connect-Example1.png)

#### CS Client disconnects from the teamserver notification example (Discord):

![CS-Client-Disconnect](/Pictures/CS-Client-Disconnect.png)

#### CS Client hosts a file or clones a website notification example (Slack):

![Host-File-Clone-Site](/Pictures/Host-File-Clone-Site.png)

#### CS client posts something in the event log (Discord):

![New-message-CS](/Pictures/New-message-CS.png)

#### New credentials come in from keylogging (Discord):

![New-credentials-come-in](/Pictures/Keystrokes-Received.png)

#### New screenshot is taken from Cobalt Strike (Slack):

![New-Screesnhot-taken](/Pictures/New-Screesnhot-taken.png)

## Misc
