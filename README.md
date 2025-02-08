# Hackathon Email Automation

## Overview

This project automates the process of sending emails for the hackathon. Given a CSV file containing recipient email addresses and a message, the system will automatically BCC all recipients while ensuring a daily limit of 500 emails.

## Features

- Accepts a CSV file with email addresses.
- Allows input of a custom email message.
- Automatically BCCs recipients to avoid exposing email addresses.
- Ensures a maximum of 500 emails are sent once. (Do not send more than this in 24hrs)
- Provides logging to track sent emails.
