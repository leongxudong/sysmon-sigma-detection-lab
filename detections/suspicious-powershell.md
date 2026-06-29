# Detection Note: PowerShell Activity Review

## Objective

Document how PowerShell-related activity can be reviewed using endpoint telemetry.

## Relevant Data Sources

| Source | Useful Events |
|---|---|
| Windows PowerShell logs | 4103, 4104 |
| Sysmon | Event ID 1 for process creation |
| Windows Security logs | Event ID 4688 if process creation logging is enabled |

## Useful Fields

- User
- Hostname
- Process name
- Command line
- Parent process
- Timestamp
- Script block content, where enabled

## Investigation Questions

- Which user ran PowerShell?
- Which parent process launched it?
- Was the command expected for administration?
- Was the host a user workstation or server?
- Is there a related ticket or approved change?

## Screenshot Placeholder

Add screenshot later:

```text
screenshots/sysmon-process-creation-event.png
```
