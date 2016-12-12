### Ansible 2.2.0 and Python 2.7.12

#### How to setup virtual env with Ansible:

* Install packages(Debian/Ubuntu)

``apt install python-virtualenv libssl-dev``

* Create python virtual environment

``virtualenv ansible-2.2.0-x86_64``

* Make virtualenv relocatable

``virtualenv --reloacatable ansible-2.2.0-x86_64``

* Use python virtual environment

``source venv/bin/activate``

* install Ansible(latest)

``pip install ansible``

* Exit python virtual environment

``deactivate``

* Compress directory with ours portable Ansible version:

``tar cfJ ansible-2.2.0-x86_64.tar.xz ./ansible-2.2.0-x86_64/*``

* Move package to another server

* Change virtualenv path in `bin/activate` file

``sed -i -e 's|/tmp/ansible|/tmp/ansible-2.2.0.0|' /tmp/ansible-2.2.0.0/bin/activate``
