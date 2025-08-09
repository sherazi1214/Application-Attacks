# Application-Attacks

## What is an Application Attack?
**English:**
An application attack targets flaws or vulnerabilities in software, websites, or apps to steal data, gain control, or disrupt services.
**Urdu:**
Application attack wo hota hai jab attacker software, website ya app ke bugs ya flaws ka faida uthata hai data churaane, control lene ya service disrupt karne ke liye.

## Common Application Attacks

### Attack Type ---------------------------------------	English Meaning

SQL Injection (SQLi)------------------------	Injecting malicious SQL code into input fields to access/modify databases.

Cross-Site Scripting (XSS)-----------------------	Injecting malicious scripts into a website to run in other users’ browsers.	

Command Injection------------------------------	Running OS-level commands via vulnerable app.	

File Inclusion-------------------------------------	Loading malicious files into a web app (LFI/RFI).	

CSRF (Cross-Site Request Forgery)-----------------------	Tricking logged-in users into making unwanted requests.	

## SQL Injection – Process
**Identify Input Point** – Attacker finds form/search box not properly validated.

**Inject Malicious SQL** – Example: ' OR '1'='1 -- in username field.

**Database Executes Query** – Server runs injected SQL instead of safe query.

**Data Theft/Modification** – Attacker reads, updates, or deletes data.

**Impact**: Data breach, admin access, full DB control.
**Mitigation**: Input validation, prepared statements (parameterized queries).

## Persistent XSS – Process
**Definition:**
Malicious script is permanently stored on the server (e.g., in database, comment, profile).

Attacker submits script in input field.

Script saved in server/database.

Any user loading the page runs the malicious script in their browser.

**Impact**:

Cookie theft, account takeover, spreading malware.

**Mitigation:**

Output encoding, input sanitization, Content Security Policy (CSP).

## Reflective XSS – Process
**Definition:**
Malicious script is reflected off the server immediately via a URL or request — not stored.

Attacker crafts a malicious link with script.

Victim clicks the link.

Server response sends back the script in page output.

Script runs in victim’s browser instantly.

**Impact:**

Same as persistent XSS, but needs victim to click crafted link.

**Mitigation:**

Input sanitization, escaping special characters, CSP.

##  Application Attacks – Quick Summary 


### SQL Injection (SQLi)

**Process** Inject malicious SQL into input fields to manipulate database queries.

**Impact** Data theft, data modification, admin access.	

**Mitigation** Input validation, parameterized queries, stored procedures.

### Persistent XSS	

**Process** Malicious script is stored in the database and served to users.

**Impact** Cookie theft, account takeover, malware spread.

**Mitigation** Output encoding, input sanitization, Content Security Policy (CSP).

### Reflective XSS

**Process** Malicious script is sent via a crafted URL and reflected in server response.

**Impact** Same as persistent XSS, requires victim to click link.	

 **Mitigation**Input sanitization, escaping characters, CSP.

### Command Injection

**Process** Inject OS commands into app input to run on server.

**Impact** Full system compromise, data loss.	

**Mitigation** Input validation, least privilege execution.

### File Inclusion (LFI/RFI)	

**Process** Include local/remote files via manipulated paths/URLs.	

**Impact** Code execution, sensitive file exposure.

**Mitigation** Input validation, disable remote file inclusion.

### CSRF

**Process** Trick user into submitting unwanted requests while logged in.

**Impact** Unauthorized transactions, account changes.

**Mitigation**Anti-CSRF tokens, same-site cookies.
