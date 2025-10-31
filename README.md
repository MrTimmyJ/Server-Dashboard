# Server Dashboard Local
A web-based dashboard for monitoring and managing web servers.

Author: Timothy Johnson <br>
Date: October 2025 <br>

**Production Demo**: http://143.198.51.64/dashboard/

## Overview

Server Dashboard provides real-time system monitoring and Docker container management through an intuitive web interface.
Built for developers who need robust local server management capabilities without production dependencies.

## ✨ Features

### 🔍 System Monitoring
- **Real-time Metrics**: CPU, memory, storage, and network usage
- **Live Charts**: Interactive performance graphs with Chart.js
- **System Information**: OS details, kernel version, architecture, and hostname
- **Uptime Tracking**: Server uptime monitoring

### 🐳 Docker Management
- **Container Overview**: List all running/stopped containers
- **Container Controls**: Start, stop, restart containers via web interface
- **Container Status**: Real-time state monitoring

### 🔐 Security & Authentication
- **Secure Authentication**: BCrypt password hashing
- **Rate Limiting**: Protection against brute force attacks  
- **Session Security**: MemoryStore session management
- **Helmet.js**: Security headers protection
- **Environment-based Configuration**: Development-focused settings

### 🛠 Technical Features
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Real-time Updates**: Auto-refreshing dashboard
- **RESTful API**: Clean API design for system data
- **Error Handling**: Comprehensive error handling and logging

## 🆚 Development vs Production

| Feature | This Version (Development) | Production Version |
|---------|---------------------------|-------------------|
| **Session Storage** | MemoryStore | Redis |
| **Security Headers** | Basic CSP | Advanced CSP |
| **Deployment** | Local development | Automated CI/CD |
| **Dependencies** | Minimal | Production-ready |
| **Session Persistence** | Lost on restart | Persistent |


📁 Code Structure

.<br>
server-dashboard/<br>
├── server.js # Main application entry point<br>
├── create_admin.js # Admin configuration<br>
├── package.json # Dependencies and scripts<br>
├── .env # Environment configuration<br>
├── users.json # User database<br>
├── public/ # Frontend assets<br>
│ ├── index.html # Main dashboard interface<br>
│ ├── login.html # Authentication page<br>
│ ├── script.js # Frontend application logic<br>
│ └── style.css # UI styles and themes<br>
└── .github/workflows/ # CI/CD configuration<br>
└── deploy.yml # Automated deployment pipeline<br>

🖼️ Screenshots / Visuals

## 🧰 Technologies Used

### 🌐 Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **systeminformation** - System metrics
- **Dockerode** - Docker API integration

### 🔐 Security
- **bcrypt** - Password hashing
- **express-session** - Session management
- **Helmet.js** - Security headers
- **express-rate-limit** - API protection

### 🎨 Frontend
- **HTML5/CSS3** - Modern web standards
- **JavaScript ES6+** - Application logic
- **Chart.js** - Data visualization
- **Google Fonts** - Typography

### 📁 File Management
- **Storage Manager** - Integrated file management system
- **File operations** - Upload, download, delete capabilities
- **Directory navigation** - Folder exploration

🚀 Getting Started

    ### Prerequisites
    - Node.js 16+ 
    - PM2 - Production process manager
    - Docker (optional, for container management)
    
    ### Installation
    
    1. **Clone and setup**:
    ```bash
    git clone https://github.com/MrTimmyJ/server-dashboard-pro.git
    cd server-dashboard-pro
    npm install
    npm install -g pm2

    npm install express express-session bcrypt helmet cors systeminformation dockerode fs-extra dotenv express-rate-limit

    touch .env

    node create_admin admin password

    node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"

🪪 License

© 2025 Timothy Johnson. All Rights Reserved.<br>
This project and its code may not be copied, modified, or reused without permission.
