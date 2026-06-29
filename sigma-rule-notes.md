# Sigma-Style Detection Notes

Sigma is a generic rule format used to describe detection logic in a platform-independent way.

## Basic Rule Sections

| Section | Purpose |
|---|---|
| Title | Short detection name |
| Status | Draft, test, experimental, or stable |
| Description | What the rule is trying to detect |
| Logsource | Where the log should come from |
| Detection | Matching conditions |
| False positives | Expected benign causes |
| Level | Severity or priority |
| Tags | Mapping to tactics, techniques, or internal categories |

## Example Structure

```yaml
title: Example Endpoint Activity
status: test
description: Detects a defined endpoint activity pattern for lab validation
logsource:
  product: windows
  service: sysmon
detection:
  selection:
    EventID: 1
  condition: selection
falsepositives:
  - Administrative activity
level: low
```

## Notes

- Detection logic should be tested against real logs.
- False positives should be documented.
- Rules should be mapped to investigation questions.
- Production use requires tuning and review.
