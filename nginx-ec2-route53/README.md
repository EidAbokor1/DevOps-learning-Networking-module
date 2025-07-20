# EC2 + NGINX + Route 53 Domain Setup

## 🔧 What I Did

- Bought domain `eiddev.xyz` from GoDaddy
- Created a public hosted zone in Route 53
- Launched a free-tier EC2 instance (Ubuntu)
- Installed NGINX and opened port 80
- Pointed `nginx.eiddev.xyz` to EC2 public IP via A record
- Verified setup using `curl`, `dig`, and DNS checker

## 🌐 Live Example
http://nginx.eiddev.xyz

## 🖥️ Technologies Used
- AWS EC2
- NGINX
- AWS Route 53


## 🧠 Skills Practiced
- Linux server setup
- Web server hosting
- DNS management
- Debugging DNS propagation