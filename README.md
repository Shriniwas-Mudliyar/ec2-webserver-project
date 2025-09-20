# 🚀 EC2 Web Server Project (with SSH & User Data)

## 📌 Project Overview
This project demonstrates how to launch an **Amazon EC2 instance**, connect securely using **PuTTY from Windows**, and set up a simple **Apache web server** using **EC2 User Data**.  

It highlights key AWS skills:
- Launching EC2 instances  
- SSH connectivity from Windows (PuTTY)  
- Automating setup with User Data scripts  
- Hosting a basic web application  

---

## 🛠️ Steps Implemented

1. Launch EC2 instance (Amazon Linux 2, t2.micro)  
2. Configure security group (allow SSH & HTTP)  
3. Connect via PuTTY using `.ppk` key  
4. Run User Data script to auto-install Apache  
5. Access public DNS → Web page live 🎉  

---

## 📂 Repository Structure
- [scripts/user-data.sh](scripts/user-data.sh) → EC2 User Data script  
- [docs/setup-steps.md](docs/setup-steps.md) → Detailed setup instructions  

---

## 📚 Skills Demonstrated
- AWS EC2 basics  
- Networking & Security Groups  
- SSH with PuTTY (Windows)  
- Infrastructure automation with User Data  
- Web hosting on Apache  
