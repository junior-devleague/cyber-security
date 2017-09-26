# Windows Cyber Prep Challenge 01
You have been tasked with setting up new Windows machines for your organization. As a System Administrator your job is to comply with user requests for new systems but ensure that standard security best practices are in compliance.

**IMPORTANT:** Document all of the steps you took for the following tasks to turn in your audit to your supervisor in an encrypted format.

**IMPORTANT:** Any requests that are not compliant with secure best practices should be noted and a report provided to your supervisor as part of your report.

### Group Administration
1. The following user groups must be setup on the system:
  - Administrators
  - Managers
  - Operations
  - Auditors

### User Administration
1. The following users must be created on the system:
  - Name: Bob
    Password: Tr3ck3rs3!
    Group: Managers

  - Name: Maria
    Password: password
    Group: Managers

  - Name: Marifel
    Password: S3cure0n!y
    Group: Operations

  - Name: Natalie
    Password: G00dPw3d
    Group: Operations

  - Name: Eric
    Password: ?DudeIKnowSecurity!
    Group: Administrators

  - Name: Antonio
    Password: MyJobIsSuperB0ring!
    Group: Auditors

### Firewall Settings
1. The user's firewall must be enabled
1. The user firewall must block all incoming requests on a public network by default
1. The user firewall must allow all outgoing requests on a public network by default
1. The user firewall must block all incoming requests on a private network by default
1. The user firewall must allow all outgoing requests on a private network by default
1. The user firewall must all incoming requests to the following ports on a private network: 53, 80, 137, 443, 445
1. The user firewall must block outgoing requests from a program called C:\Program Files\Nmap\nmap.exe on a private network
1. The user firewall must block C:\Program Files\uTorrent\uTorrent.exe on all networks
1. Ensure that the user is shown a notification when a program is blocked
1. Ensure that all firewall events are logged and take note of the path that log files are stored on disk

### User Password Policy
1. Ensure that all users have the following password policy procedures enabled:
  - Passwords must not be able to be decrypted
  - Users must change their password every 90 days
  - Users must ensure their passwords are at least 10 characters long
  - Users must ensure their passwords meet certain complexity requirements
  - If a user attempts to login with an improper password they will be locked out from other attempts for a period of 15 minutes

### Auditing
1. Ensure that events are logged when a user logs in for both success and failure
1. Ensure that events are logged when account management settings are changed
1. Ensure that events are logged when security policy, user rights, or auditing settings are changed
1. Ensure that events are logged when program files are modified
1. Ensure that system events are logged when the computer shutsdown or restarts
1. Ensure that these events are being logged and document your steps to verify

### General Security Settings
1. Ensure that Automatic Updates are enabled
1. Ensure that the Guest account is disabled
1. Ensure that a user is prompted to change their password 10 days before it expires
1. Ensure that backups are performed every 7 days automatically


### Process Management
1. Document all of the processes currently running on this machine to record the base state of the machine
1. Disable Remote Desktop Services for this machine

### Audit Submission
Using Microsoft Word or 7-zip encrypt your report with a password and send the encrypted document to your supervisor

### Stretch Goals
See if you can find these setting in the Windows Registry
