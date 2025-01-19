# CS-Aggressor-Kit
Homemade Aggressor scripts kit for Cobalt Strike

## Table of Contents
- [CS-Aggressor-Kit](#cs-aggressor-kit)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
  - [Alert](#alert)
  - [Auto](#auto)
  - [Misc](#misc)
  - [Utils](#utils)

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
| Auto | [auto-sleep-on-start.cna](/Auto/auto-sleep-on-start.cna) | This CNA file automatically sets the sleep time to a specific value when a new user joins the teamserver. It requires a client to remain open at all times, ensuring the sleep time is configured even if the Cobalt Strike client is closed or you forget to set it while away. |
| Auto | [auto-sleep-on-exit.cna](/Auto/auto-sleep-on-exit.cna) | This CNA file automatically sets the sleep time to a specific value when all users, except one, disconnect from the teamserver. A client must remain open at all times. |
| Misc | [Beacon-Name-Tab.cna](/Misc/Beacon-Name-Tab.cna) | This CNA file modifies the Beacon tab name format from the default to `username`@`hostname` (`pid`) |
| Misc | [Beacon-Name-Tab-Colors.cna](/Misc/Beacon-Name-Tab-Colors.cna) | This CNA file modifies the Beacon tab name format from the default to `username`@`hostname` (`pid`), for admin's beacon the color is red, for user's beacon the color is green |
| Misc | [CS-All-Tabs-Bold.cna](/Misc/CS-All-Tabs-Bold.cna) | This CNA file makes all CS client tabs bold |
| Misc | [CWD-Beacon-Bar.cna](/Misc/CWD-Beacon-Bar.cna) | This CNA file enhances Beacon console status bar to display the Beacon's last known working directory path. Additionally, improves the 'cd' command to support restoring the previous directory path seamlessly (Usage: `cd -`) |
| Utils | [Sonata.cna](/Utils/Sonata.cna) | This CNA file is a port of the [Sonata](https://github.com/nickvourd/Sonata) tool. Sonata is a file hash calculator that supports MD5, SHA1, SHA256, and SHA512 algorithms. The CNA port enhances functionality by supporting string hash calculations as well |
| Utils | [locate.cna](/Utils/locate.cna) | This CNA functions like the `locate` Linux command. Additionally, it performs case-insensitive keyword searches. This CNA requires a Linux CS client |

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

## Auto

These CNA files automatically configure certain actions in Cobalt Strike.

The following table illustrates the CNA files included in the Auto section:

| Name | Description |
|:-----------:|:-----------:|
| [auto-sleep-on-start.cna](/Auto/auto-sleep-on-start.cna) | This CNA file automatically sets the sleep time to a specific value when a new user joins the teamserver. It requires a client to remain open at all times. |
| [auto-sleep-on-exit.cna](/Auto/auto-sleep-on-exit.cna) | This CNA file automatically sets the sleep time to a specific value when all users, except one, disconnect from the teamserver. A client must remain open at all times. |

### How Auto Sleep Works

:information_source: The two auto-sleep CNA files can be used individually or together, depending on your preferences.

**Diagram 1**: The two Cobalt Srike clients are connected to the Team server.

![Diagram-1](/Pictures/Diagram-1.png)

**Diagram 2**: At the end of the day's engagement tasks, the operators decide to stop the engagement. One operator, using a Cobalt Strike client without the CNA file, disconnects from the teamserver, while the other operator ensures his/her Cobalt Strike client with the CNA file ([auto-sleep-on-exit.cna](/Auto/auto-sleep-on-exit.cna)) remains open.

![Diagram-2](/Pictures/Diagram-2.png)

**Diagram 3**: The Cobalt Strike client with the CNA file will detect the user disconnection event and automatically adjust the sleep time to the predefined value specified in the CNA file.

![Diagram-3](/Pictures/Diagram-3.png)

**Diagram 4**: The next day, when the operator (with the Cobalt Strike client without the CNA file) connects to the Team Server, the always-open client with the loaded CNA file ([auto-sleep-on-start.cna](/Auto/auto-sleep-on-start.cna)) will detect the new user connection. It will then automatically set the sleep time to the predefined value specified in the CNA file.

![Diagram-4](/Pictures/Diagram-4.png)

## Misc

These CNA files will configure the output format for various default functionalities of Cobalt Strike.

The following table illustrates the CNA files included in the Misc section:

| Name | Description |
|:-----------:|:-----------:|
| [Beacon-Name-Tab.cna](/Misc/Beacon-Name-Tab.cna) | This CNA file modifies the Beacon tab name format from the default to `username`@`hostname` (`pid`) |
| [Beacon-Name-Tab-Colors.cna](/Misc/Beacon-Name-Tab-Colors.cna) | This CNA file modifies the Beacon tab name format from the default to `username`@`hostname` (`pid`), for admin's beacon the color is red, for user's beacon the color is green |
| [CS-All-Tabs-Bold.cna](/Misc/CS-All-Tabs-Bold.cna) | This CNA file makes all CS client tabs bold |
| [CWD-Beacon-Bar.cna](/Misc/CWD-Beacon-Bar.cna) | This CNA file enhances Beacon console status bar to display the Beacon's last known working directory path. Additionally, improves the 'cd' command to support restoring the previous directory path seamlessly (Usage: `cd -`) |

### Beacon Name Tab

This CNA file modifies the Beacon tab name format from the default to `username`@`hostname` (`pid`).

![Beacon-Tab-Name-Example](/Pictures/Beacon-Tab-Name-Example.png)

### Beacon Name Tab Colors

This CNA file modifies the Beacon tab name format from the default to `username`@`hostname` (`pid`). For an Administrator's Beacon, the tab color is set to red, while for a standard user's Beacon, the tab color is set to green.

![Beacon-Tab-Name-Colors-Example](/Pictures/Beacon-Tab-Name-Colors-Example.png)

### CS All Tabs Bold

This CNA file makes all Cobalt Strike client tabs bold.

![CS-All-Tabs-Bold-Example](/Pictures/CS-All-Tabs-Bold-Example.png)

### CWD Beacon Bar

This CNA file enhances Beacon console status bar to display the Beacon's last known working directory path.

![CWD-Beacon-Bar-Example](/Pictures/CWD-Beacon-Bar-Example.png)

Additionally, improves the 'cd' command to support restoring the previous directory path seamlessly (Usage: `cd -`).

![CWD-Beacon-Bar-Example-2](/Pictures/CWD-Beacon-Bar-Example-2.png)

Finally, when you have an Administrator's Beacon, the hostname of the target machine changes from the CNA's default green (used for standard users) to red.

![CWD-Beacon-Bar-Example-Admin](/Pictures/CWD-Beacon-Bar-Example-Admin.png)

## Utils

These CNA files are used for general micro tasks during operations.

The following table illustrates the CNA files included in the Utils section:

| Name | Description |
|:-----------:|:-----------:|
| [Sonata.cna](/Utils/Sonata.cna) | This CNA file is a port of the [Sonata](https://github.com/nickvourd/Sonata) tool. Sonata is a file hash calculator that supports MD5, SHA1, SHA256, and SHA512 algorithms. The CNA port enhances functionality by supporting string hash calculations as well |
| [locate.cna](/Utils/locate.cna) | This CNA functions like the `locate` Linux command. Additionally, it performs case-insensitive keyword searches. This CNA requires a Linux CS client |

### Sonata

Hash calculator for local files and strings.

Usage: `Sonata -f/--file <local_filepath> OR Sonata -s/--string <string>`

#### Sonata File Example

![Sonata-Example-1](/Pictures/Sonata-Example-1.png)

#### Sonata String Example

![Sonata-Example-2](/Pictures/Sonata-Example-2.png)

#### Locate

This CNA functions like the `locate` Linux command. Additionally, it performs case-insensitive keyword searches. This CNA requires a Linux CS client

![locate-example](/Pictures/locate-example.png)