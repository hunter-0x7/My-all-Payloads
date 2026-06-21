# 🎯 Blind XSS Hunting Notes

## What is Blind XSS?

Blind XSS occurs when a payload executes somewhere other than where it was injected.

Unlike Stored XSS, you cannot immediately see the execution.

The payload may trigger when:

* An admin views your profile
* A support agent opens a ticket
* A moderator reviews a report
* A dashboard renders logged data
* An email client displays user input

**Mindset:**

Inject anywhere that another human or system may eventually read your input.

---

## 👤 User Input Fields

### Registration Forms

* Username
* Email
* Phone Number
* Address

### Profile Updates

* Bio
* Display Name
* Job Title
* Custom Fields

### User Generated Content

* Comments
* Reviews
* Forum Posts
* Feedback Forms

### Support Systems

* Ticket Descriptions
* Attachment Names
* User Messages

---

## 📧 Email Workflows

### Registration

* Verification Emails
* Welcome Emails

### Password Reset

* Email Address
* Reset Request Logs

### Subscription Systems

* Newsletter Signups
* Unsubscribe Requests

### Why?

User input is often rendered inside:

* CRM Systems
* Support Dashboards
* Admin Portals
* Internal Mail Systems

---

## 🛡️ Administrative Panels

This is usually the most valuable Blind XSS target.

### Common Areas

* User Management
* Moderation Queues
* Support Dashboards
* Audit Logs
* Security Logs
* Internal Notifications

### Why Important?

Administrators usually have:

* Elevated privileges
* Access to sensitive information
* Access to internal systems

---

## 📋 Headers & Metadata

### HTTP Headers

* User-Agent
* Referer
* Accept-Language
* Origin
* X-Forwarded-For

### API Headers

* Custom Headers
* Tracking Headers
* Correlation IDs

### File Metadata

* EXIF Data
* ZIP Comments
* PDF Author
* ID3 Tags

---

## 🔄 Application Workflows

Look for workflows where data is stored and reviewed later.

Examples:

* Password Reset
* Account Recovery
* Event Registration
* Subscription Management
* Approval Workflows

---

## 📂 File Uploads

### Injection Points

* Filename
* Description
* Metadata
* MIME Information

### Review Locations

* Moderation Panels
* Support Dashboards
* Internal Review Systems

---

## 🔔 Notifications & Alerts

Common Targets:

* Email Notifications
* User Reports
* Feedback Alerts
* Admin Warnings
* System Messages

---

## 🟠 Burp Suite Opportunities

### Parameter Testing

* GET Parameters
* POST Parameters
* JSON Values
* XML Values
* Multipart Forms

### Header Testing

* User-Agent
* Referer
* Origin
* X-Forwarded-For
* Custom Headers

### Repeater Strategy

Test the same payload in:

* Parameters
* Headers
* Metadata
* Hidden Fields

---

## ✅ High Value Checklist

* Registration Forms
* Login Logs
* Support Tickets
* Contact Forms
* Feedback Forms
* User Profiles
* File Uploads
* Audit Logs
* Admin Dashboards
* Email Workflows
* Moderation Panels
* Internal Tools

---

## 🎯 Final Thought

Blind XSS is not about where you inject.

Blind XSS is about where your data will be viewed later.
