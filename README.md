# 🗳️ Online Voting System using Blockchain

A secure, fast, and transparent online voting platform powered by **Blockchain** and OTP-based **email verification**. This system leverages modern web technologies like **FastAPI** and **Flask**, with Python-based backend logic to ensure data integrity, voter authentication, and tamper-proof voting processes.

---

## 🚀 Features

- 🔐 **Email-based OTP Verification** for secure user authentication
- ⛓️ **Blockchain Integration** to ensure transparent and tamper-resistant vote storage
- ⚡ **FastAPI** for high-performance backend
- 🛡️ **Flask-based Registration Interface**
- 📁 Persistent storage using JSON files
- 🧪 Simple and modular codebase for easy extension

---

## 📂 Project Structure

```
OVS-Using-Blockchain/
│
├── main.py                        # FastAPI backend server
├── otp.py                         # Email OTP generator and verifier
├── user_data.py                   # Manages user credentials and data
├── utils.py                       # Helper models and org registration
├── requirements.txt               # Python dependencies
│
├── blockchainfolder/
│   └── chain.py                   # Custom blockchain implementation
│
├── Varified_gmail_and_password/
│   ├── server.py                  # Flask app for user registration
│   ├── otp.py                     # Duplicate OTP logic for registration
│   ├── users.json                 # Stores verified user data
│   └── templates/                 # HTML templates for register & verify
│       ├── register.html
│       └── verify.html
│
├── Procfile                       # Deployment configuration (Heroku)
└── README.md                      # Project documentation
```

---

## 🔧 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/glcrealm/OVS-Using-Blockchain.git
cd OVS-Using-Blockchain
```

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Setup environment variables

Create a `.env` file and add your Gmail credentials:

```
EMAIL_ADDRESS=your_email@gmail.com
EMAIL_PASSWORD=your_app_password
```

> Ensure 2FA is enabled and an App Password is used for Gmail.

### 5. Run the applications

- Start **Flask** server for registration:

```bash
cd Varified_gmail_and_password
python server.py
```

- Start **FastAPI** main server:

```bash
uvicorn main:app --reload
```

---

## 🔒 How it Works

1. ✅ **User Registration**:
   - Users enter email, name, age, password.
   - OTP is sent to email and verified.

2. 🗳️ **Voting**:
   - Verified users log in.
   - Votes are recorded onto a blockchain.

3. ⛓️ **Blockchain**:
   - Each vote is a block.
   - Blocks are mined and linked, preventing tampering.

---

## 📸 Screenshots

![Register Page](f)
![OTP Verification](f)
![Voting Dashboard](f)

---

## 🛠️ Tech Stack

- **Python 3**
- **FastAPI**
- **Flask**
- **Jinja2**
- **Blockchain (custom)**
- **SMTP (Gmail)**

---

## 🤝 Contributing

Feel free to fork the repository, create a feature branch and submit a pull request. Contributions are welcome!

