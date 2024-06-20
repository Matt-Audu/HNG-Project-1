# Deploying a Static Web Application on Apache Web Server

This guide provides step-by-step instructions for deploying a static web application on an Apache Web Server. 
Follow these steps to ensure a successful deployment.

### Prerequisites

Before you start, make sure you have the following:

- A linux server. (e.g. Redhat, Ubuntu, CentOS)
- SSH access to the server.
- Open Port 22, 443 and 80.
- Basic knowledge of the command line.

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

#### 4.1: Transfer Application files

Copy and paste your application files (HTML and CSS) into the /var/www/html directory by creating the same files.

```
sudo cd /var/www/html
sudo vi index.html
sudo vi styles.css
```

### Step 5: Access your application

Access your web application with the public IP address of your server.





