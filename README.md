# 🔐 SecurePass – Random Strong Password Generator

![Cyber Security](https://img.shields.io/badge/Cyber%20Security-Capstone%20Project-7c3aed?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Web Crypto API](https://img.shields.io/badge/Web%20Crypto%20API-00f5c4?style=for-the-badge)

> A cryptographically secure, fully client-side password generator built for the **Lenovo × BharatCares Cyber Security Capstone Project**.

---

## 🌐 Live Demo

👉 **[https://yourusername.github.io/SecurePass](https://yourusername.github.io/SecurePass)**

---

## 📌 Problem Statement

**Area:** Password Management

**Problem:** Users create weak and predictable passwords repeatedly, making their accounts vulnerable to brute-force attacks, dictionary attacks, and credential stuffing.

**Solution:** SecurePass — a web-based random strong password generator that uses the browser's built-in **Web Crypto API** to generate cryptographically secure passwords instantly, with zero data stored or transmitted.

---

## ✨ Features

| Feature | Description |
|---|---|
| ⚡ **Password Generator** | Generate strong passwords with full customization |
| 📏 **Length Control** | Slider from 8 to 32 characters |
| 🔠 **Character Options** | Uppercase, Lowercase, Numbers, Symbols |
| 🚫 **Exclude Ambiguous** | Remove confusing chars like `l`, `1`, `O`, `0` |
| 📊 **Strength Indicator** | Real-time visual strength meter (Weak → Excellent) |
| 📋 **One-Click Copy** | Copy password to clipboard instantly |
| 🔁 **Batch Generation** | Generate 1, 3, 5, or 10 passwords at once |
| 📜 **Session History** | View your last 10 generated passwords |
| 🔍 **Strength Checker** | Analyze the strength of any existing password |
| 💡 **Security Tips** | Built-in cybersecurity awareness panel |

---

## 🛠️ Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | HTML5 | Page structure |
| Frontend | CSS3 | Responsive styling & animations |
| Frontend | JavaScript (Vanilla) | Password logic & DOM manipulation |
| Security | **Web Crypto API** | Cryptographically secure random generation |
| Fonts | Google Fonts (Syne + Space Mono) | UI typography |
| Hosting | GitHub Pages | Free deployment |

> **No backend. No database. No tracking.** All processing happens 100% in your browser.

---

## 🚀 How to Run Locally

### Option 1 – Direct Open
```bash
# Clone the repository
git clone https://github.com/yourusername/SecurePass.git

# Open index.html in your browser
cd SecurePass
open index.html      # macOS
start index.html     # Windows
xdg-open index.html  # Linux
```

### Option 2 – Live Server (VS Code)
1. Install the **Live Server** extension in VS Code
2. Right-click `index.html` → **Open with Live Server**
3. App opens at `http://127.0.0.1:5500`

---

## 📁 Project Structure

```
SecurePass/
│
├── index.html          # Main HTML – app structure
├── style.css           # CSS – dark theme, animations, responsive
├── script.js           # JS – password logic, strength analysis, UI
├── README.md           # Project documentation
└── screenshots/        # App screenshots (proof of work)
    ├── homepage.png
    ├── strength-meter.png
    ├── batch-generator.png
    └── password-checker.png
```

---

## 🔒 Security Approach

SecurePass uses the **[Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API)** (`crypto.getRandomValues()`) instead of `Math.random()`.

| Method | Type | Safe for Passwords? |
|---|---|---|
| `Math.random()` | Pseudo-random | ❌ No – predictable |
| `crypto.getRandomValues()` | Cryptographically secure | ✅ Yes – unpredictable |

This ensures generated passwords have **true entropy** and cannot be predicted or reproduced.

---

## 📊 Password Strength Scoring

The strength checker evaluates passwords on multiple criteria:

- ✅ Length (8 → 12 → 16 → 20+ characters)
- ✅ Uppercase letters present
- ✅ Lowercase letters present
- ✅ Numbers present
- ✅ Symbols present
- ✅ Character uniqueness ratio
- ❌ Deductions for repeated characters
- ❌ Deductions for single character type only

**Strength Levels:** Weak → Moderate → Strong → Very Strong → Excellent

---

## 🔭 Future Scope

- [ ] Browser extension (Chrome / Firefox)
- [ ] Password breach checker (HaveIBeenPwned API)
- [ ] Encrypted local password vault
- [ ] Mobile app (Android / iOS)
- [ ] Multi-language support (Hindi, Tamil, Bengali)
- [ ] AI-powered password suggestions
- [ ] Enterprise dashboard with policy enforcement

---

## 👨‍💻 Author

**[Your Name]**
Cyber Security Program – Lenovo × BharatCares

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- **Lenovo** and **BharatCares** for the Capstone Project framework
- [MDN Web Docs](https://developer.mozilla.org) for Web Crypto API documentation
- [HaveIBeenPwned](https://haveibeenpwned.com) for breach awareness inspiration
