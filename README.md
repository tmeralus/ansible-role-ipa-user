Ansible Role IPA User
=========
Ansible role used for creating, deleting, and modifying
FreeIPA users.

Role Variables
--------------
* test_user: "test_user"
* test_email: "test_email"
* ipa_host: "host.example.com"
* ipa_user: "admin"
* ipa_pass: "pass"
* mail: testuser@example.com
* telephonenumber: '+555123456'
* uidnumber: '1001'
* gidnumber: '100'
* homedirectory: /home/test

Example Playbook
----------------
#### Run playbook to create a new user
* ansible-playbook -l <hostname> ansible-role-ipa-user/tasks/enabled_user.yml

#### Run playbook to disable a new user
* ansible-playbook -l <hostname> ansible-role-ipa-user/disable_user.yml

#### Run playbook to disable 10 test users
* ansible-playbook -l <hostname> ansible-role-ipa-user/tasks/disable_loop.yml

#### Run playbook to enable 10 test users with an expiration date  
* ansible-playbook -l <hostname> ansible-role-ipa-user/tasks/enabled_loop.yml
