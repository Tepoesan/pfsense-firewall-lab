# VirtualBox hardening

## Objective
Reduce unnecessary host–guest interactions and the virtual machine attack surface.

## Security controls
| Feature | Status | Rationale |
|---|---|---|
| Shared clipboard | Disabled (operator confirmed) | Limit host–guest data exchange |
| Drag and drop | Disabled (operator confirmed) | Limit file transfers |
| Shared folders | None (settings inspected) | Avoid guest access to host files |
| USB controller | Pending confirmation | Avoid unnecessary physical device access |
| Remote display | Pending final verification | Avoid unnecessary remote access |

## Procedure
Inspect General > Features, Shared Folders, USB, and Display > Remote Display. Disable unnecessary integrations. Save settings and recheck before booting.

## Security considerations
Apply least privilege and defense in depth. These settings reduce exposure but do not guarantee isolation. Keep VirtualBox and the host updated. Do not publish credentials, raw firewall configuration backups, or identifying screenshots.

## Validation
The first three controls have been checked. USB and remote display require final confirmation; runtime security has not been tested.

## Lessons learned
Network isolation alone is insufficient: host–guest integration features also deserve review.

## References
- [Oracle VirtualBox security guide](https://www.virtualbox.org/manual/ch13.html)
