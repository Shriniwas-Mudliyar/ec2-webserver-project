# 📝 Detailed Setup Guide for EC2 Web Server

This guide provides step-by-step instructions to reproduce the project.

---

## 1️⃣ Launch EC2 Instance
1. Log in to the **AWS Management Console**.  
2. Navigate to **EC2 → Launch Instance**.  
3. Configure the following:
   - **AMI**: Amazon Linux 2 (Free Tier)  
   - **Instance Type**: t2.micro  
   - **Key Pair**: Create a new key pair and download the `.pem` file  
   - **Security Group**:
     - SSH (22) → My IP  
     - HTTP (80) → Anywhere (0.0.0.0/0)  
4. Under **Advanced Details → User Data**, paste the script from [`scripts/user-data.sh`](../scripts/user-data.sh).  
5. Launch the instance 🚀  

---

## 2️⃣ Connect via Windows (PuTTY)
1. Convert `.pem` to `.ppk` using PuTTYgen.  
2. Open PuTTY → Enter **Public IPv4 DNS** → Auth → Select `.ppk` → Open.  
3. Login as `ec2-user`.  

---

## 3️⃣ Web Server Setup
The User Data script ensures:
- Apache (`httpd`) installed  
- Web server starts immediately and on reboot  
- Default homepage created at `/var/www/html/index.html`  

---

## 4️⃣ Verify Web Server
1. Copy the **Public IPv4 DNS** of your instance.  
2. Open in browser: `http://<public-dns>`  
3. You should see:  
