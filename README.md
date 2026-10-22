#  pfSense Firewall Lab

### Virtualized Network Security Laboratory

A hands-on cybersecurity project focused on building, configuring, and securing a virtual network using **pfSense Community Edition** and **Oracle VirtualBox**.

##  Project Objectives

The goal of this project is to develop practical skills in network administration and cybersecurity by creating a controlled virtual laboratory.

The laboratory will be used to:

- Understand network architecture and communication protocols.
- Install and configure a pfSense firewall.
- Configure WAN and LAN interfaces.
- Explore IP addressing, DHCP, routing, and NAT.
- Create and test firewall rules.
- Monitor network traffic and analyze firewall logs.
- Practice network segmentation and troubleshooting.

##  Technologies

| Technology | Purpose |
|---|---|
| pfSense CE | Firewall and network routing |
| Oracle VirtualBox | Virtualization environment |
| Linux | Client machine for network testing |
| Windows | Host operating system |
| Git & GitHub | Documentation and version control |

##  Planned Network Architecture

```text
       VirtualBox NAT
             |
          WAN |
       +-----------+
       |  pfSense  |
       |  Firewall |
       +-----------+
          LAN |
             |
     Internal Network
             |
      +-------------+
      | Linux Client|
      +-------------+
```

The laboratory will initially operate offline using an isolated internal network. Internet access through VirtualBox NAT will be enabled later for controlled experiments.

##  Security Principles

- Use an isolated virtual network.
- Avoid bridged networking.
- Do not expose laboratory services to the public Internet.
- Do not publish passwords, private keys, or sensitive configurations.
- Perform security tests only on authorized laboratory systems.
- Document configuration changes and test results.

##  Learning Progress

- [x] Create GitHub repository.
- [ ] Install Oracle VirtualBox.
- [ ] Create pfSense virtual machine.
- [ ] Install and configure pfSense.
- [ ] Configure the internal network.
- [ ] Create a Linux client virtual machine.
- [ ] Configure firewall rules.
- [ ] Test network connectivity and filtering.
- [ ] Analyze firewall logs.
- [ ] Document results and lessons learned.

##  Project Status

**Status:** Planning and environment preparation.

This repository documents an ongoing personal cybersecurity learning project. Configurations, experiments, and results will be added progressively.
