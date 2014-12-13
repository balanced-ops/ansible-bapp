# KNOX

## Knox [![Build Status](https://magnum.travis-ci.com/balanced-ops/ansible-bapp.svg?token=ykTaJtscxcuMJxYq2Nt5&branch=master)](https://magnum.travis-ci.com/balanced-ops/ansible-knox)

### Local Development of Knox

```bash
~/code/balanced/ops $ git clone git@github.com:balanced-ops/ansible-knox.git
~/code/balanced/ops $ git clone git@github.com:balanced-ops/vagabond.git
~/code/balanced $ git clone git@github.com:balanced/knox.git
~/code/balanced/knox $ ln -s ~/code/balanced/ops/vagabond/Vagrantfile Vagrantfile
~/code/balanced/knox $ echo "# -*- mode: yaml -*-
ansible_playbook: ~/code/balanced/ops/ansible-knox/site.yml
synced_folders:
- ~/code/balanced/knox" > .vagrantuser
~/code/balanced/knox $ vagrant up
```

