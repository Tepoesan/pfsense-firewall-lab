# Environment setup

## Objective
Prepare a virtual firewall laboratory on a Windows host using Oracle VirtualBox and pfSense CE.

## Procedure and configuration
- Install Oracle VirtualBox (confirmed by the operator).
- Create the `pfSense-Lab` virtual machine.
- Select FreeBSD (64-bit), 2 GiB RAM, 2 virtual CPUs and a 20 GiB virtual disk.
- Attach the Netgate installer ISO (v1.2, amd64).

## Rationale and security
Virtualization separates the guest from the host but is not an absolute security boundary. Use official installation media, verify integrity where publisher checksums are available, and keep the hypervisor patched. Installer integrity and installed software versions have not yet been verified.

## Validation
VirtualBox manager inspection confirmed the VM and attached ISO. pfSense installation and boot have not yet been verified.

## Lessons learned
Creating a VM is distinct from installing its operating system.

## References
- [Oracle VirtualBox documentation](https://www.virtualbox.org/manual/)
- [Netgate installation documentation](https://docs.netgate.com/pfsense/en/latest/install/index.html)
