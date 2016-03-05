# Server Guidelinecould

In this file I will collect several guidelines - preferences for bootstraping new servers and
maintaining old up to date.

## Operating System

Stick with latest Debian stable, at this time Debian 8.3 Jessie.

Take preference for 64 bits hardware and distributions.

## Configuration Management

Will use Ansible for keeping inventory and configurations up to date. Avoid ssh
to a machine and do hand-made changes which will be overriden on next Ansible
run.

Use git for keeping playbooks and settings.

## Security concerns

It's a tradeoff between security and usability. I would like to keep secure
systems from the most frequent attacks while keeping administration simple.

Won't use shared accounts. What happens if someone wins the lottery and leaves
CodingStones?

### Security checklist:

This checklist should be automated with Ansible, and will be common to all our
nodes.

1. Change root password
2. Update & Upgrade systems
3. Install fail2ban
4. Require public key authentication for users
5. Enable sudo
6. Disable SSH password authentication
7. Disable SSH login for root
8. Firewall. Allow access only to SSH port
9. Automatic unattended upgrades for security origins
10. System wide monitoring with Munin
11. Install logwatch | Other intrussion system

There are extra points that could be implemented in a near future:

1. Install ClamAV
2. NTP time client

Other to be considered:

1. Apticron

### Security stuff

http://www.stefan-seelmann.de/wiki/debian-security
