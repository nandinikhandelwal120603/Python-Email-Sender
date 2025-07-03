
# 📧 Python Email Sender

This Python script allows you to **send emails** using Gmail’s SMTP server, with support for:

✅ Sending to multiple recipients
✅ HTML or plain-text emails
✅ File attachments (any type)
✅ TLS encryption (secure)

---

## ⚡ Features

* Send emails via Gmail’s SMTP (with `smtplib` and `ssl`)
* Add multiple recipients
* Add one or more attachments
* Send HTML or plain-text email body
* Clean structure with error handling

---

## 🛠 Requirements

* Python 3.x
* Gmail account (app password if 2FA is enabled)

### Install required modules (if not already installed):

```bash
pip install --upgrade pip
```

(*All used libraries — `smtplib`, `ssl`, `email`, `mimetypes`, `os` — are from the Python standard library.*)

---

## 🚀 How to Use

### 1️⃣ Set up environment variable for your email password:

On Linux / macOS:

```bash
export EMAIL_PASSWORD='your-app-password'
```

On Windows (Command Prompt):

```bash
set EMAIL_PASSWORD=your-app-password
```

> ⚠️ **Note:** If your Gmail account has 2FA enabled, you must create and use an **App Password** instead of your main password.

---

### 2️⃣ Update the script:

```python
sender_email = "your-email@gmail.com"
sender_name = "Your Name"
password = os.environ.get("EMAIL_PASSWORD")

email_subject = "Good morning"
email_body = """
<h1>Good Morning!</h1>
<p>Hope you have a <strong>wonderful day</strong>.</p>
"""

receiver_emails = ["receiver1-email@gmail.com", "receiver2-email@gmail.com"]
attachments = ["path/to/attachment1.pdf", "path/to/attachment2.jpg"]

send_email(sender_email, sender_name, password, receiver_emails, email_body,
           email_subject, is_html=True, attachments=attachments)
```

---

### 3️⃣ Run the script:

```bash
python email_sender.py
```

---

## 📂 Example

The script sends an email like this:

**Subject:** Good morning
**Body:**

```
Good Morning!
Hope you have a wonderful day.
```

**Attachments:** `attachment1.pdf`, `attachment2.jpg`

---

## ⚠️ Important Notes

* Make sure **Less Secure Apps** is enabled, or use an **App Password** (recommended).
* Gmail may block sign-in attempts if it detects automation.
* Be cautious when sending bulk emails to avoid spam filters.

---

## 🤝 Contributions

Feel free to fork the repository and submit pull requests for enhancements!

---

## 📄 License

MIT License.

