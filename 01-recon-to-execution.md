# Lab 01 — Recon to execution (ATT&CK mapping)

**Goal:** Take a simple lab attack path and map each step to MITRE ATT&CK.

## Scenario (lab)

An attacker on the lab network:

1. Scans for live hosts and open services
2. Identifies a vulnerable or misconfigured service
3. Gains a foothold and runs commands on the target

## Mapping

| Step | Activity | Tactic | Technique ID | Technique name |
| --- | --- | --- | --- | --- |
| 1 | Network scan for live hosts/ports | Reconnaissance / Discovery | T1595 / T1046 | Active Scanning / Network Service Discovery |
| 2 | Identify service versions | Discovery | T1046 | Network Service Discovery |
| 3 | Exploit weak service (lab) | Initial Access | T1190 | Exploit Public-Facing Application |
| 4 | Run shell commands on host | Execution | T1059 | Command and Scripting Interpreter |

## Defensive notes

- **Prevent:** Patch exposed services; close unused ports; network segmentation.
- **Detect:** Alert on internal scanning behaviour and unusual process creation after remote access.
- **Respond:** Isolate host, preserve logs, reset credentials if compromise is confirmed.

## What I learned

- ATT&CK is useful for explaining attacker behaviour without overclaiming.
- One lab path can touch several tactics — documenting each step keeps analysis clear.
- Detection ideas should stay practical (logs, alerts, patching), not tool-name shopping lists.
