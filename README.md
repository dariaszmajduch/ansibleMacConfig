1. Check if Python is installed
`python --version`
2. Install pip
`sudo easy_install pip`
3. Install ansible & virtualenv
`sudo pip install ansible virtualenv`
4. Clone repo to desired direcotry and open it
5. Install ansible-galaxy roles
`ansible-galaxy install geerlingguy.homebrew
ansible-galaxy install fubarhouse.macdock`
6. Change local_user_name value in `localhost.yml`
7. Install needed software which is not possible to install using homebrew (i.e. WebStorm)
8. Run ansible scripts
`ansible-playbook localhost.yml --ask-become-pass`
