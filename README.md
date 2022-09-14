# HOA4.1_CPE232_ADUCAL
Codes use for HOA 4.1 Ansible basics
for installing ansible:
sudo apt install ansible -y
To update cache in remote servers:
ansible all -m apt -a update_cache=true
ansible all -m apt -a update_cache=true --become --ask-become-pass

for local machine to instruct servers to install packages:
ansible all -m a name=vim-nox --become --ask-become-pass
which vim
apt seach vim-nox

for checking servers history log/installation logs:
cd /var/log
ls
cd apt
cat history.log

to check for latest installation package:
ansible all -m apt -a name=snapd --become --ask-become-pass
ansible all -m apt -a "name=snapd state=latest" --become --ask-become-pass

to commit all changes to GitHub:
git status
git add README.md
git commit -m "HOA 4.1 Task 1"
git push origin main
