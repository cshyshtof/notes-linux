---
type: zettel
---

```meta-bind-button
label: Set next review
hidden: false
id: review
style: primary
actions:
  - type: command
    command: review-obsidian:future-review
  - type: input
    str: "next 7 days"
```

# Ansible

- Prepare OS for Ansible management

Generate temporary password, which will be used only to upload an SSH key to remote host (template)

```bash
sudo useradd ansible -m -c "Ansible" -s /bin/bash -G wheel
sudo passwd ansible

sudo su -
echo "ansible ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers.d/ansible
```

