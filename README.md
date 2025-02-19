# Hackathon Email Automation

## Overview

This project automates the process of sending emails for the hackathon. Given a CSV file containing recipient email addresses and a message, the system will automatically BCC all recipients while ensuring a daily limit of 500 emails.

## Features

- Accepts a CSV file with email addresses.
- Allows input of a custom email message.
- Automatically BCCs recipients to avoid exposing email addresses.
- Ensures a maximum of 500 emails are sent once. (Do not send more than this in 24hrs)
- Provides logging to track sent emails.
**CSV Input:**  
  Accepts a CSV file with email addresses. The CSV should include headers `Name:` and `Email:`.

- **Custom Message:**  
  Allows you to input a custom email message. If not provided, a default invitation message is used.

- **BCC Functionality:**  
  Automatically BCCs recipients to hide their email addresses.

- **Daily Limit:**  
  Ensures that no more than 500 emails are sent in a single day.

- **Banner Image:**  
  Supports embedding an inline banner/cover image within the email.

- **Logging:**  
  Provides detailed logging (saved in `email_log.txt`) to track sent emails and any errors.

## Running the code

```bash
python send_invitations.py --csv emails_test.csv --banner banner.png --sender contact@sachacks.io

--subject : Customize the email subject (default: "SacHacks Invitation").
--message : Provide a custom email message. If omitted, a default message is used.
--smtp : Specify the SMTP server (default: smtp.gmail.com).
--port : Specify the SMTP port (default: 587)
## Prerequisites

- **Python 3.x**  
  Ensure you have Python 3 installed on your machine.

- **SMTP Access:**  
  Use an email account that supports SMTP (e.g., Gmail). Note that if you're using Gmail, you may need to set up an App Password if you have two-factor authentication enabled.

- **CSV File:**  
  Prepare your CSV file (e.g., `emails_test.csv`) with the following format:
  ```csv
  Name:,Email:
  
