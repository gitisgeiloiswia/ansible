# Ansible exercise (Topic 5)
---
#### Write an ansible role to configure an CentOS 7.4 System with following state:
- ##### OpenSSH Server in latest version should be installed (3 PTS)
  - SSH Protocol Version 1 MUST be disabled
  - SSH Protocol Version 2 MUST be enabled
  - no root login should be allowed
- ##### Install following packages in latest version (0.5 PTS)
  - vim, nano, git, vi, tree, rsyslog
- ##### Deploy a message of the day (1 PTS)
  - must be done via template
  - your group name, configurable via attribute
  - your group members (Surname delimited by -). fe. KAPPEL-NIMMERVOLL, configurable via attribute array
  - The name of your lecturer (FIRSTNAME,SURNAME), configurable via attribute
  - The Date (MM.DD.YYYY) of the last tool-run (automatic, not configurable) a String “Change me”, which must be configurable via attribute
  - Example:
	> GROUP2
	> ALABA-ARNAUTOVIC-PROEDL
	> KAPPEL,CHRISTOPH
	> 01.01.2011
	> Change me
- ##### User ckappel must be on the system (2 PTS)
  - He wants to use a bash shell
  - He must be a sudo user
  - His public ssh key must be deployed
  - He must be able to login via ssh
  - His home must be /home/linuxguru
- ##### User animmervoll must not be on the system (0.5 PTS)
  - He wants to use a bash shell
  - He must not be a sudo user
  - He must be able to login via ssh
  - His home must be /home/nimm
  - He must be a group member of lecturer
- ##### NGINX (6 PTS)
  - 1.12.1 version
  - listen on port 8080, 8443
  - serve TLS
  - TLS 1.2 is allowed
  - RC4 is not allowed
  - serves a index.html under /var/www/nginx/index.html
  - with your group name 
  - your group members
  - the name of the lecturer
  - the date of the last run,
  - Example:
	> GROUP2
	> ALABA-ARNAUTOVIC-PROEDL
	> KAPPEL,CHRISTOPH
	> 01.01.2011
	> Change me
- ##### Service nginx must be running (1 PTS)

## Anleitung
Jedes Playbook kann eigenständig laufen. Um alles durchlassen zu lassen kann die main.yml benutzt werden.
```
$ ansible-playbook main.yml --ask-become-pass --become
```
ssh keys für ckappel werden aus einen File geholt das zufinden sein sollte unter

> /opt/ansibleuser/.ssh/ckappel/ckappel_rsa.pub

 
  
Das Homeverzeichnis meines Users ist in diesem Fall:
> /opt/ansibleuser 
