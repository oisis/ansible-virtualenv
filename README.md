### Ansible 2.2.0 and Python 2.7.12

#### How to setup virtual env with Ansible:

* Install packages(Debian/Ubuntu)

``apt install python-virtualenv libssl-dev``

* Create python virtual environment

``virtualenv ansible``

* Make virtualenv relocatable

``virtualenv --reloacatable ansible``

* Use python virtual environment

``source venv/bin/activate``

* install Ansible(latest)

``pip install ansible``

* Exit python virtual environment

``deactivate``

* Compress directory with ours portable Ansible version:

``tar vxfc ansible.tar.xz ./ansible/*``

* Move package to another server

* Change virtualenv path in `bin/activate` file

``sed -i -e 's|/tmp/ansible|/tmp/ansible-2.2.0.0|' /tmp/ansible-2.2.0.0/bin/activate``
