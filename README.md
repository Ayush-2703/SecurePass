# 🔐 SecurePass – Random Strong Password Generator

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.0-000000?style=for-the-badge&logo=flask&logoColor=white)
![Cyber Security](https://img.shields.io/badge/Cyber%20Security-Capstone-7c3aed?style=for-the-badge)

> Cyber Security Capstone Project — Lenovo × BharatCares  
> Password generation powered entirely by **Python's `secrets` module** via a **Flask** web server.

---

## 📌 Problem Statement
**Area:** Password Management  
**Problem:** Users create weak and predictable passwords repeatedly.  
**Solution:** SecurePass generates cryptographically secure passwords server-side using Python's `secrets` module — far stronger than `Math.random()` in JavaScript.

---

## 🏗️ Project Structure
```
SecurePass/
│
├── app.py                  ← Flask app + ALL password logic (Python)
├── requirements.txt        ← Python dependencies
├── README.md
├── templates/
│   └── index.html          ← Jinja2 template (UI + fetch calls to Flask)
└── screenshots/            ← App screenshots
```

### Why Python instead of JavaScript?
| Feature | JavaScript `Math.random()` | Python `secrets` module |
|---|---|---|
| Randomness | Pseudo-random (predictable) | Cryptographically secure |
| Security | ❌ Not safe for passwords | ✅ Designed for security |
| Backend control | Client-side only | Full server-side logic |

---

## ✨ Features
- ⚡ Cryptographically secure generation via `secrets.choice()`
- 📏 Length control: 8–32 characters
- 🔠 Uppercase, Lowercase, Numbers, Symbols toggle
- 🚫 Exclude ambiguous characters (l, 1, O, 0)
- 📊 Server-side strength analyser (score 0–100)
- 📋 One-click copy to clipboard
- 🔁 Batch generation: 1, 3, 5, or 10 passwords
- 🔍 Real-time password strength checker
- 💡 Cybersecurity awareness tips panel

---

## 🛠️ Technology Stack
| Layer | Technology |
|---|---|
| Backend | **Python 3** + **Flask** |
| Password Generation | **`secrets` module** (cryptographically secure) |
| Strength Analysis | **Pure Python** logic |
| Template Engine | **Jinja2** |
| Frontend | HTML5 + CSS3 (inline) |
| API | JSON REST (`/generate`, `/check`) |

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/Ayush-2703/SecurePass.git
cd SecurePass

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the Flask app
python app.py

# 4. Open in browser
# http://127.0.0.1:5000
```

---

## 🔗 API Endpoints

### `POST /generate`
```json
// Request
{
  "length": 16,
  "uppercase": true,
  "lowercase": true,
  "numbers": true,
  "symbols": true,
  "no_repeat": false,
  "exclude_ambiguous": false,
  "count": 3
}

// Response
{
  "passwords": [
    { "password": "X9#mK2$vQp", "strength": { "label": "Very Strong", "percent": 88, ... } }
  ]
}
```

### `POST /check`
```json
// Request  → { "password": "mypassword" }
// Response → { "label": "Weak", "percent": 20, "score": 18, "criteria": {...} }
```

---

## 🔭 Future Scope
- [ ] Deploy to Render / Railway (free Python hosting)
- [ ] Password breach checker (HaveIBeenPwned API)
- [ ] Encrypted session vault
- [ ] Mobile app with Flask API backend

---

## 👨‍💻 Author
**AYUSH KUMAR SINGH** — Cyber Security Program, Lenovo × BharatCares

## 📄 License
MIT License
