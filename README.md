# 🖥️ AssistHub — Remote Support & Screen Sharing

A modern **remote-support web application** that lets technicians create support sessions and customers join using a short code. AssistHub combines **WebRTC screen sharing, real-time chat, authentication, and file sharing** in one application.

## ✨ Features

- 🔐 User registration, login and secure password hashing
- 🔢 Unique 6-digit support session codes
- 🖥️ Peer-to-peer screen sharing with WebRTC
- 💬 Real-time chat with Socket.IO
- 📁 Secure session-based file sharing
- 📊 Dashboard with active and previous sessions
- 🛑 Session ending and 30-day session history
- 📱 Responsive web interface

## 🛠️ Tech Stack

**Backend:** Python, Flask, Flask-SocketIO  
**Real-time:** WebRTC, Socket.IO  
**Database:** SQLite, SQLAlchemy  
**Authentication:** Flask-Login, Werkzeug  
**Frontend:** HTML, CSS, JavaScript

## 🏗️ How It Works

```text
Technician → Create Session → 6-Digit Code
                                  ↓
Customer → Join Session → WebRTC Screen Sharing
                         ↕
                    Live Chat + Files
```

## 🚀 Getting Started

### Requirements

- Python 3.9+

### Installation

```bash
git clone https://github.com/Vileka06/AssistHub.git
cd AssistHub
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

Open `http://localhost:5002` in your browser.

## 🎯 Usage

1. Create two accounts using separate browsers or an incognito window.
2. Technician logs in and creates a support session.
3. Share the generated 6-digit code with the customer.
4. Customer joins the session using the code.
5. Customer explicitly approves screen sharing through the browser permission dialog.
6. Use chat and file sharing during the support session.
7. End the session when support is complete.

## 🔒 Security Notes

- Passwords are hashed rather than stored as plain text.
- Session pages require authentication and membership validation.
- Uploaded files are validated and stored with randomized names.
- Screen sharing requires explicit browser consent.
- Production deployments should use a strong `SECRET_KEY`, HTTPS, a production WSGI server, and a TURN server for reliable internet-wide WebRTC connectivity.

## 📁 Project Structure

```text
AssistHub/
├── app.py
├── config.py
├── extensions.py
├── models/
├── routes/
├── templates/
├── static/
├── uploads/
├── database/
├── requirements.txt
└── README.md
```

## 📌 Future Improvements

- Production-ready deployment configuration
- TURN server integration for wider WebRTC connectivity
- Improved session analytics
- Notifications and support-ticket workflow

**Built with Python, Flask, WebRTC and JavaScript.**