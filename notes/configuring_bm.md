1. No elastic beanstalk like functionality so we are using VMs, monitoring is only available
via CentOS so we are using that.


Update the packages
```
sudo -s
yum update -y
```

Add monitoring

follow this guide

https://www.eu-gb.bluemix.net/docs/virtualmachines/vm_monitoring.html#vm_monitoring


# Python stuff

```
sudo yum install -y epel-release
sudo yum install -y python-pip
sudo yum group install "Development Tools"
sudo yum install python-devel
sudo pip install virtualenv
sudo pip install virtualenvwrapper
```

Now we need to configure virtualenv wrapper, append this to ~/.bashrc  

```
source /bin/virtualenvwrapper.sh
```

Next activate it with:

```
source ~/.bashrc
```


# Source Code Stuff

```
sudo yum install -y git
```

# Install postgresql 9.4 client

```
sudo yum localinstall http://yum.postgresql.org/9.4/redhat/rhel-6-x86_64/pgdg-centos94-9.4-1.noarch.rpm
sudo yum install postgresql94-server
sudo yum install postgresql94-devel
sudo yum install postgresql-devel
```

# Setting up the system

1. generate ssh key

```
ssh-keygen

2. add key to github

3. mkvirtualenv

```
mkvirtualenv hellodjango
mkdir -p ~/projects/
cd ~/projects/
git clone git@github.com:chrisking/hellodjango.git
cd hellodjango
pip install -r requirements.txt
```
