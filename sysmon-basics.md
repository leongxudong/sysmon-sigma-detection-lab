# Sysmon Basics

Sysmon provides additional Windows telemetry that can support endpoint monitoring and investigation.

## Common Event IDs

| Event ID | Event | Monitoring Use |
|---:|---|---|
| 1 | Process creation | Review command execution and parent-child process relationships |
| 3 | Network connection | Review outbound network activity by process |
| 7 | Image loaded | Review DLL or module loading where configured |
| 10 | Process access | Review process access activity where configured |
| 11 | File created | Review file creation activity |
| 13 | Registry value set | Review registry modification activity |
| 22 | DNS query | Review domain lookups by process |

## Key Fields

- Image
- CommandLine
- ParentImage
- ParentCommandLine
- User
- Hashes
- DestinationIp
- DestinationHostname
- QueryName

## Notes

Sysmon generates useful telemetry, but configuration quality matters. Logging too much can create noise; logging too little can miss important context.
