# Problem Statement 5 — Password Strength Indicator

You are creating a **Password Strength Indicator** for a new website.  
The goal is to set up correct logic for checking password strength and displaying appropriate messages.

However, the project is not yet complete, and you need to finish it.

---

## 🎯 Objectives

- Add a **placeholder** attribute with value:  
  **"Enter your password"**  
  to the input element with `id="passwordInput"`

- Fill logic to **check password strength** and **update the strength indicator** when password changes.

- Set color to **#e74c3c** for the strength indicator when class is `"weak"`.

---

## 🧩 Output (Expected UI)

A card-like design showing:

- Password Strength heading  
- Password input field  
- Strength message such as:  
  **Weak Password** (in red background)

---

## 📄 HTML Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Strength</title>
    <link rel="stylesheet" href="index.css">
</head>
<body>
    <div class="main-container">
        <div class="container">
            <h1>Password Strength</h1>
            <input type="password" id="passwordInput" class="password-input" placeholder="Enter your password">

            <div id="strengthIndicator" class="strength_indicator">
                <span id="strengthText">Enter a password</span>
            </div>
        </div>
    </div>

    <script src="index.js"></script>
</body>
</html>
```

---

## 🎨 CSS Code — `index.css`

```css
body {
    font-family: Arial, sans-serif;
}

.main-container {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #f6f6f6;
}

.container {
    background: white;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0px 0px 10px rgba(0,0,0,0.1);
}

.password-input {
    width: 100%;
    padding: 10px;
    margin-top: 10px;
    font-size: 16px;
    border: 2px solid #ccc;
    border-radius: 8px;
}

.strength_indicator {
    margin-top: 15px;
    padding: 12px;
    border-radius: 8px;
    text-align: center;
    font-weight: bold;
}

.weak {
    background-color: #e74c3c;
    color: white;
}

.medium {
    background-color: #f1c40f;
    color: white;
}

.strong {
    background-color: #2ecc71;
    color: white;
}
```

---

## ⚙️ JavaScript Code — `index.js`

```javascript
const passwordInput = document.getElementById("passwordInput");
const strengthIndicator = document.getElementById("strengthIndicator");
const strengthText = document.getElementById("strengthText");

passwordInput.addEventListener("input", checkStrength);

function checkStrength() {
    const pwd = passwordInput.value;

    if (pwd.length === 0) {
        strengthIndicator.className = "strength_indicator";
        strengthText.textContent = "Enter a password";
        return;
    }

    let strength = getStrengthLevel(pwd);

    if (strength === "weak") {
        strengthIndicator.className = "strength_indicator weak";
        strengthText.textContent = "Weak Password";
    } 
    else if (strength === "medium") {
        strengthIndicator.className = "strength_indicator medium";
        strengthText.textContent = "Medium Password";
    } 
    else {
        strengthIndicator.className = "strength_indicator strong";
        strengthText.textContent = "Strong Password";
    }
}

function getStrengthLevel(password) {
    let hasLetters = /[a-zA-Z]/.test(password);
    let hasNumbers = /[0-9]/.test(password);
    let hasSpecial = /[^a-zA-Z0-9]/.test(password);

    if (password.length < 4) return "weak";

    if ((hasLetters && hasNumbers) || (hasLetters && hasSpecial) || (hasNumbers && hasSpecial)) {
        if (password.length >= 8) return "strong";
        return "medium";
    }

    return "weak";
}
```

---

## ✅ What This Solves

✔ Adds placeholder  
✔ Implements strength checking  
✔ Updates UI dynamically  
✔ Applies red color (`#e74c3c`) for weak passwords  

---

## 📥 Download File

This `.md` file is generated automatically.

