# Balanced Apps

## [![Build Status](https://travis-ci.org/balanced-ops/ansible-bapp.svg)](https://travis-ci.org/balanced-ops/ansible-bapp)

### Local Development of Knox|Precog|Balanced

```bash
~/code/balanced/ops $ git clone git@github.com:balanced-ops/ansible-bapp.git
~/code/balanced/ops/ansible-bapp $ ansible-galaxy install -r requirements.yml -p $(pwd)/roles --force
~/code/balanced/ops/ansible-bapp $ mkvirtualenv bapp
~/code/balanced/ops/ansible-bapp $ pip install -r requirements.txt
~/code/balanced/ops $ git clone git@github.com:balanced-ops/vagabond.git
~/code/balanced $ git clone git@github.com:balanced/knox.git
~/code/balanced/knox $ ln -s ~/code/balanced/ops/vagabond/Vagrantfile Vagrantfile
~/code/balanced/knox $ echo "# -*- mode: yaml -*-
ansible_playbook: `pwd`/code/balanced/ops/ansible-bapp/knox.yml
synced_folders:
- ~/code/balanced/knox" > .vagrantuser
~/code/balanced/knox $ vagrant plugin install nugrant
~/code/balanced/knox $ vagrant plugin install vagrant-cachier
~/code/balanced/knox $ vagrant plugin install vagrant-hostmanager
~/code/balanced/knox $ vagrant up
```
