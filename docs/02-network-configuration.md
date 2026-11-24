# Virtual network configuration

## Objective
Prepare an initially offline laboratory with separate WAN and LAN interfaces.

## Procedure
| Adapter | Mode | Cable | Purpose |
|---|---|---|---|
| 1 | NAT | Disconnected | Future WAN |
| 2 | Internal Network: LAB-LAN | Connected | Private LAN |
| 3 | Disabled | N/A | Unused |
| 4 | Disabled | N/A | Unused |

Both enabled adapters use Intel PRO/1000 MT Desktop (82540EM), with promiscuous mode set to Deny. The NAT port forwarding list is empty.

## Rationale and security
Internal networking permits communication among VMs on the same named network without direct host or physical LAN attachment. NAT alone does not prevent outbound access to the host or domestic network. Keep the WAN cable disconnected during offline preparation; any temporary installer connectivity must be reviewed separately. Avoid bridged networking and port forwarding.

## Validation
Adapters 1 and 2 and the empty forwarding list were inspected in VirtualBox settings. Adapters 3 and 4 were confirmed disabled by the operator. Saving and runtime isolation have not been independently verified. pfSense interface assignment and client connectivity tests remain pending.

## Lessons learned
Virtual adapter configuration is not the same as firewall policy or verified network isolation.

## References
- [Oracle VirtualBox networking](https://www.virtualbox.org/manual/ch06.html)
- [Netgate pfSense documentation](https://docs.netgate.com/pfsense/en/latest/)
