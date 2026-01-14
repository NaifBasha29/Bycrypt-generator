# BCrypt Generator

A powerful web-based tool for **generating, verifying, and recovering** BCrypt hashed passwords. Perfect for developers who need to work with bcrypt hashes or recover forgotten passwords from their projects.

![BCrypt Tool Screenshot](https://img.shields.io/badge/BCrypt-Password%20Tool-purple?style=for-the-badge&logo=lock)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## What is BCrypt?

BCrypt is a **one-way hashing algorithm** used to securely store passwords. Unlike encryption, hashing is **irreversible** — you cannot "decrypt" a bcrypt hash back to the original password. However, you can:

-  **Generate** a bcrypt hash from any password
-  **Verify** if a password matches a given hash
-  **Recover** weak/common passwords using dictionary attacks

---

## Features

### Generate Hash
Convert any plain text password into a secure bcrypt hash with adjustable salt rounds (cost factor).

### ✓ Verify Hash
Check if a password matches a bcrypt hash — useful for testing authentication systems.

### Password Recovery (Crack Hash)
Forgot the password for your project's database? This tool helps you recover it using:

| Attack Type | Description | Best For |
|-------------|-------------|----------|
| ** Wordlist Attack** | Upload a `.txt` file with passwords | Large password lists like `rockyou.txt` |
| ** Brute Force** | Try all character combinations | Short passwords (1-6 chars) |
| ** Custom List** | Enter guesses manually | Known password patterns |

---

## Usage

### Option 1: Open Directly
Simply open `index.html` in any modern browser — no server required!

### Option 2: Live Server
```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve
```

---

## How It Works

### Generating a Hash
1. Enter your password
2. Adjust salt rounds (higher = more secure but slower)
3. Click "Generate BCrypt Hash"
4. Copy the resulting hash

### Verifying a Password
1. Enter the plain text password
2. Paste the bcrypt hash
3. Click "Verify Password"
4. See if they match ✓ or ✗

### Recovering a Password
1. Paste the bcrypt hash you want to crack
2. Choose attack method:
   - **Wordlist**: Upload a `.txt` file (one password per line)
   - **Brute Force**: Select charset and length range
   - **Custom**: Type passwords manually
3. Click "Start Cracking"
4. Wait for results — if found, the password is revealed!

---

## Getting Wordlists

For effective password recovery, you'll need wordlists. Popular options:

- **[SecLists](https://github.com/danielmiessler/SecLists)** — Comprehensive security wordlists
- **[rockyou.txt](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt)** — 14 million leaked passwords
- **Custom lists** — Create your own based on known patterns

---

## Important Notes

- **BCrypt cannot be decrypted** — only weak/common passwords can be "cracked" via guessing
- **Salt rounds matter** — Higher rounds = exponentially slower to crack
- **Educational use only** — Only use on passwords you own or have permission to test
- **Browser-based** — All processing happens locally, no data sent to servers

---

## Technical Details

- **Library**: [bcrypt.js](https://github.com/dcodeIO/bcrypt.js) for browser-based bcrypt operations
- **No dependencies**: Single HTML file with embedded CSS/JS
- **Offline capable**: Works without internet after initial load
- **Modern UI**: Glassmorphism design with smooth animations

---

## Use Cases

1. **Forgot admin password** — Recover access to your own projects
2. **Testing security** — Verify password strength in your applications
3. **Development** — Generate test hashes for authentication systems
4. **Learning** — Understand how bcrypt hashing works

---

## Contributing

Feel free to submit issues and pull requests!

---

## License

MIT License — Use freely for personal and commercial projects.

---
