 █████╗ ██╗   ██╗██████╗ ██╗████████╗██████╗ 
 ██╔══██╗██║   ██║██╔══██╗██║╚══██╔══╝██╔══██╗
 ███████║██║   ██║██║  ██║██║   ██║   ██║  ██║
 ██╔══██║██║   ██║██║  ██║██║   ██║   ██║  ██║
 ██║  ██║╚██████╔╝██████╔╝██║   ██║   ██████╔╝
 ╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚═╝   ╚═╝   ╚═════╝ 
                    Harden your Unix   

This repository provides a valuable resource for enhancing system security by implementing comprehensive auditd rules and verifying their effectiveness through automated testing. The applied rules are based on my learnings to get deeper into the topic for hardening my Linux machines.

## Auditd Rules

The `auditd.rules` file contains a collection of auditd rules that monitor various system events, including:

* User logins and logouts
* File access and modifications
* Process executions
* Privilege escalation attempts
* Suspicious activity

## GitHub Action

The `auditd-syntax-check.yml` GitHub Action file defines a workflow that tests all the auditd rules defined in the `auditd.rules` file. The action utilizes a Docker container to simulate a Linux environment and executes auditd commands to verify that the rules are functioning correctly.

## Usage

To utilize this repository, follow these steps:

1. Clone the repository to your local machine.
2. Copy the `auditd.rules` file to your Linux system's `/etc/audit/rules.d` directory.
3. Restart the auditd service to apply the new rules.
5. Commit and push your changes to the repository as a Pull Request if you like to contribute

The GitHub Action will automatically run upon each push to the repository, testing the auditd rules and reporting any potential issues.
