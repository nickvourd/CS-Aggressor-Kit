# CS-Aggressor-Kit
Homemade aggressor scripts kit for Cobalt Strike

## Table of Contents
- [CS-Aggressor-Kit](#cs-aggressor-kit)
  - [Table of Contents](#table-of-contents)
  - [Alert](#alert)

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

The following table illustrates the CNA files included in this Alert section:

| Name | OS | App | Description |
|:-----------:|:-----------:|:-----------:|:-----------:|
|[slack-alerts_linux.cna](/Alert/Slack/slack-alerts_linux.cna)| Linux | Slack | Slack CNA file for Linux CS client |
|[slack-alerts_windows.cna](/Alert/Slack/slack-alerts_windows.cna)| Windows | Slack | Slack CNA file for Windows CS client |
|[discord-alerts_linux.cna](/Alert/Discord/discord-alerts_linux.cna)| Linux | Discord | Discord CNA file for Linux CS Client |
|[teams-alerts_linux.cna](/Alert/Teams/teams-alerts_linux.cna)| Linux | Teams | Teams CNA file for Linux CS Client |
