# MITRE ATT&CK Lab Notes

Educational notes from threat-analysis labs. I map observed or simulated attacker activity to MITRE ATT&CK tactics and techniques, then outline defensive detections.

## What this repo shows

- Breaking an attack path into ATT&CK tactics
- Linking evidence to technique IDs
- Suggesting high-level detections and mitigations

## Sample mapping

See [`labs/01-recon-to-execution.md`](labs/01-recon-to-execution.md).

| Tactic | Technique (example) | Defensive idea |
| --- | --- | --- |
| Reconnaissance | Active Scanning (T1595) | Monitor unusual scan patterns; restrict external exposure |
| Discovery | Network Service Discovery (T1046) | Alert on internal port sweeps from unexpected hosts |
| Execution | Command and Scripting Interpreter (T1059) | Log script interpreters; review unusual process trees |

## Tools / references

- [MITRE ATT&CK](https://attack.mitre.org/)
- Lab notes from Kali / virtual environments
- NIST CSF concepts for organising defensive controls

## Disclaimer

Educational content only. No production systems were targeted.
