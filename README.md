# OWASP Juice Shop Login Form

A deliberately vulnerable login form built for CSCE 703 HW3.

## How to Run

Open `login.html` in any browser. No server or dependencies needed.

## Credentials

- Email: `sampleuser123@gmail.com`
- Password: `password123`

## XSS Attack

Paste this into the email field and click Log in:
<img src=x onerror="document.getElementById('secretPanel').style.display='block'">@x


This bypasses client-side validation and exploits an unsafe `innerHTML` call to expose a hidden `secret.txt` panel.

## Fix

Replace `innerHTML` with `textContent` in the `serverValidate` function.
