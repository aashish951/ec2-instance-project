# EC2 Instance - Static Website Deployment

**Project URL**: https://roadmap.sh/projects/ec2-instance

## 🌐 Live Website
http://13.233.66.86

## 📋 Project Description
Successfully deployed a custom animated website on AWS EC2 using Ubuntu Server and Nginx web server. This project demonstrates cloud computing skills, Linux server administration, and web deployment on AWS infrastructure.

## 🎯 Features
- ✅ BGMI-style animated banner with gradient effects
- ✅ Responsive design for mobile and desktop
- ✅ Glowing particles and smooth animations
- ✅ Real-time server deployment on AWS EC2
- ✅ Nginx web server configuration

## 🛠️ Technologies Used
- **AWS EC2** - Cloud Computing Platform
- **Ubuntu Server 22.04 LTS** - Operating System
- **Nginx** - High-performance Web Server
- **HTML5 & CSS3** - Frontend with animations

## 📸 Screenshots

### EC2 Instance Running
![EC2 Instance](screenshots/ec2-instance.png)

### Security Group Configuration
![Security Group](screenshots/security-group.png)

### Website Live
![Website Live](screenshots/website-live.png)

### SSH Connection
![SSH Terminal](screenshots/ssh-connection.png)

## 🚀 Deployment Steps

### 1. AWS Account Setup
- Created AWS Free Tier account
- Verified email and completed phone verification

### 2. EC2 Instance Configuration
- **AMI**: Ubuntu Server 22.04 LTS
- **Instance Type**: t2.micro (Free Tier eligible)
- **Region**: ap-south-1 (Mumbai)
- **Security Group Rules**:
  - **SSH (Port 22)**: My IP only (for secure access)
  - **HTTP (Port 80)**: 0.0.0.0/0 (public access)
- **Key Pair**: Created and securely stored `.pem` file
- **Public IP**: Assigned automatically

### 3. Server Connection
```bash
# Set proper permissions for key file
chmod 400 ec2ashishWeb.pem

# Connect via SSH
ssh -i ec2ashishWeb.pem ubuntu@13.233.66.86
```

### 4. Server Configuration
```bash
# Update system packages
sudo apt update && sudo apt upgrade -y

# Install Nginx web server
sudo apt install nginx -y

# Start and enable Nginx service
sudo systemctl start nginx
sudo systemctl enable nginx

# Verify Nginx is running
sudo systemctl status nginx
```

### 5. Website Deployment
```bash
# Remove default Nginx page
sudo rm /var/www/html/index.html

# Create custom HTML file
sudo nano /var/www/html/index.html

# Paste custom HTML code and save

# Set proper permissions
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
```

### 6. Testing & Verification
- ✅ Accessed website via public IP
- ✅ Verified Nginx service status
- ✅ Tested responsive design on mobile
- ✅ Confirmed animations working properly

## 📚 Learning Outcomes

Through this project, I gained hands-on experience in:

✅ **AWS EC2**: Creating and managing cloud instances  
✅ **Linux Administration**: Ubuntu server management via SSH  
✅ **Web Server Configuration**: Installing and configuring Nginx  
✅ **Security**: Configuring security groups and firewall rules  
✅ **Networking**: Understanding public IPs and port configuration  
✅ **Cloud Deployment**: Deploying static websites to cloud infrastructure  

## 🎯 Stretch Goals (Future Enhancements)

- [ ] Custom domain setup using Amazon Route 53
- [ ] HTTPS implementation with Let's Encrypt SSL certificate
- [ ] CI/CD pipeline using AWS CodePipeline
- [ ] Portfolio website deployment

## 👨‍💻 Author
**Ashish**

## 📝 Project Status
✅ **Completed** - Website successfully deployed and running live on AWS EC2

---


*This project is part of the [roadmap.sh](https://roadmap.sh) DevOps learning path.*
