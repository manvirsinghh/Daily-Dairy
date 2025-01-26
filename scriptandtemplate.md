## Live report                                                                                              
## DATE.26-01-2025

**Start time:-10:30 am**
#####Task:-automation script of installation of frappe on virtual environment
System does not work get stopped working 
#### script :-

```bash
#!/bin/bash

sudo apt-get update -y
sudo apt-get upgrade -y

sudo apt-get install -y \
	cron \
	curl \
	gnupg \
	libssl-dev \
	libmysqlclient-dev \
	libjpeg-dev \
	zlib1g-dev \
	libffi-dev \
	libxml2-dev \
	libxslt1-dev \
	build-essential \
	libjpeg8-dev \
	libsasl2-dev \
	libldap2-dev \
	redis-server
sudo apt-get install -y python3.10 python3.10-dev python3.10-venv
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 1
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
sudo apt-get install -y python3-pip
sudo pip3 install --upgrade pip==20.3.4
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo npm install -g yarn
sudo apt-get install -y wkhtmltopdf
sudo apt-get install -y software-properties-common
sudo add-apt-repository "deb http://mariadb.mirror.somersettechsolutions.co.uk/repo/10.6/ubuntu focal main"
sudo apt-get update -y
sudo apt-get install -y mariadb-server
sudo apt-get install -y redis-server
sudo apt-get install -y libmysqlclient-dev
sudo pip3 install frappe-bench
bench init frappe-bench --frappe-branch version-15
cd frappe-bench
bench new-site library.localhost --db-password '2Gn4BCATEo8QkObj' --admin-password '123456' --no-mariadb-socket
bench get-app erpnext --branch version-15
bench --site library.localhost install-app erpnext
bench start
echo "Frappe 15 has been installed and the server is running on http://localhost:8000"
```

**End time:-1:00pm** 

**Start time:-1:05pm**
#####Task:-Web templates
Paused at:-4:45pm
Resumed At :-5:30pm
I have tried to login frappe couple of times but doesn’t work

**End time:-9:40pm**

