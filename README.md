# Deploying a Static Web Application on Apache Web Server

This guide provides step-by-step instructions for deploying a static web application on an Apache Web Server. 
Follow these steps to ensure a successful deployment.

### Prerequisites

Before you start, make sure you have the following:

- A linux server. (e.g. Redhat or CentOS)
- SSH access to the server.
- Open Port 22 and 80.
- Basic knowledge of the command line.
- A local terminal. (e.g gitbash)

### Step 1: Install Apache

```
sudo yum install httpd
```

### Step 2: Start and Enable Apache

```
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Step 3: Confirm Apache is running

```
sudo systemctl status httpd
```

### Step 4: Deploy Your Application

#### 4.1: Allow appropriate permissions

Allow read, write and execute permissions for successful file transfer.

```
cd /var/www/
```

Allow necessary permissions for "html" directory

```
sudo chmod 777 "html"
```

#### 4.2: Configure your local terminal to transfer files

Configure your local terminal (e.g gitbash) to enable smooth file transfer to remote server.

```
eval "$(ssh-agent -s)"
```
Add ssh private key.

```
ssh-add Directory/example.pem
```

#### 4.3: Transfer application files

Tranfer your application files (HTML, CSS and Javascript) into the /var/www/html/ directory.

```
scp <path to files>/* ec2-username@I.p address:/var/www/html
```
### Step 5: Access your application

Access your web application with the public IP address of your server.





