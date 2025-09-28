# 🚀 Nginx Setup on WSL (Windows Subsystem for Linux)

## 1. Check Installed Distros
```bash
wsl -l -v
```
- Lists all installed WSL distros.  
- Shows their **state** (Running/Stopped) and **version** (WSL1/WSL2).  
- The distro with `*` is your default one.  

---

## 2. Open a Specific Distro
```bash
wsl -d Ubuntu-22.04
```
- Opens the specified Linux distro (`Ubuntu-22.04` in this case).  
- If you just run `wsl`, it will open the default one.  

---

## 3. Update Package List
```bash
sudo apt update
```
- Refreshes package information.  
- Makes sure you’re installing the latest versions of software.  

---

## 4. Install Nginx
```bash
sudo apt install nginx -y
```
- Installs **Nginx web server**.  
- `-y` automatically confirms “yes” for prompts.  

---

## 5. Start Nginx Service
```bash
sudo service nginx start
```
- Starts the Nginx web server.  
- After this, go to **http://localhost** in your browser to check if it’s running.  

---

## 6. Stop Nginx Service
```bash
sudo service nginx stop
```
- Stops the Nginx web server.  
- Useful when you want to shut it down.  

---

## 7. Verify Nginx is Running
```bash
ps aux | grep nginx
```
- Shows processes related to Nginx.  
- Confirms if Nginx is running in the background.  

---
# Nginx Docker Installation Guide

This file contains all the steps to install and run Nginx inside a Docker container on Ubuntu.

---

## Step 1: Run Docker Ubuntu Image
```bash
docker run -it -p 8080:80 ubuntu
sudo apt-get update
sudo apt-get install nginx
sudo nginx -v
nginx
```

Now visit http://localhost:8080 and you would be able to see default nginx welcome page.
