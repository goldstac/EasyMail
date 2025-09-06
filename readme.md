# Easymail

Easymail is a lightweight Python wrapper for the Gmail API that simplifies sending emails.  
It manages authentication, token storage, and message creation, allowing you to focus on writing your message instead of boilerplate code.

---

## Features
- Simple and intuitive API for sending Gmail messages
- Automatic Gmail OAuth2 authentication flow
- Local token storage for seamless reuse
- Dynamic message bodies with f-string support
- Minimal setup – authenticate once and send emails in seconds

---

## How It Works
Easymail uses the official Gmail API:
1. Provide your `client_secret.json` from the Google Cloud Console.
2. Easymail runs the OAuth2 flow and saves a `token.json` locally.
3. You set the subject, recipient, and body.
4. Your email is sent with just a few lines of Python.

---

## Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/goldstac/easymail.git
cd easymail
pip install -r requirements.txt
```

---

## Usage

```python
from easymail import easymail

# Authenticate with your client secret JSON file
easymail.credentials("client_secret.json")

# Configure email
easymail.sendmail.subject("Hello from Easymail!")
easymail.sendmail.recipient("example@gmail.com")

# Send it
easymail.sendmail("This is a test email sent using Easymail 🚀")
```

---

## Author
**Li Productions**

---

## License
This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

