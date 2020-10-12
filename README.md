1. Check if Python is installed
```
python --version
```
2. Install pip
```
sudo easy_install pip
```
3. Install ansible & virtualenv
```
sudo pip install ansible virtualenv
```
4. Clone repo to desired direcotry and open it
5. Install ansible-galaxy roles
```
ansible-galaxy install geerlingguy.homebrew
ansible-galaxy install fubarhouse.macdock
```
6. In `localhost.yml`:
  - change local_user_name
  - change github_org_name
  - change bitbucket_org_name
7. `config` role is by default disabled
  - **Be sure that copied files are correct (check present config, copy them and add the new config data)**
  - ssh keys and aws credentials (if needed) should be generated manually
8. Update repositories names in `group_vars/localhost/repositories.yml`
9. Install needed software which could not be installed using homebrew (i.e. WebStorm)
10. Check if chromedriver and geckodriver versions are correct (in `group_vars/localhost/drivers.yml` file)
11. Run ansible scripts
```
ansible-playbook localhost.yml --ask-become-pass
```
