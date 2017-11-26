# ansible exercise
Jedes Playbook kann eigenständig laufen. Um alles durchlassen zu lassen kann
die main.yml benutzt werden.
command: ansible-playbook main.yml --ask-become-pass --become

ssh keys für ckappel werden aus einen File geholt das zufinden sein sollte unter
/opt/ansibleuser/.ssh/ckappel/ckappel_rsa.pub

/opt/ansibleuser ist in diesem Fall das Homeverzeichnis meines Users.

