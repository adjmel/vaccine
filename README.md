/!\ In progress /!\

# 💉 Vaccine — SQL Injection Detection & Exploitation Tool

## 📌 Description

**Vaccine** is a tool designed to detect and exploit SQL injection vulnerabilities on web applications by analyzing the responses from a given URL. It performs 2 SQL injection tests ( `UNION`, `Boolean`) and supports both `GET` and `POST` requests.

---

## ⚠️ Disclaimer

> ❗ This tool is intended for educational purposes and **must not** be used on websites without **explicit permission**.
> Always test only on labs, deliberately vulnerable applications, or systems you own.

---

## ✅ Features

* 🧠 Detect database engine:

  * MySQL / MariaDB
  * Oracle
    
* 🗂️ Retrieve:

  * Vulnerable parameters
  * Payloads used
  * Database names
  * Table names
  * Column names
  * Extracted data
    
* 📁 Auto-saves results into an archive file (default or user-defined)
* ⚙️ Handles both `GET` and `POST` requests

---

## 🧪 Example Usage

```bash
# Basic usage with default archive and GET method
./vaccine https://example.com/vulnerable?page=1

# Specify archive file to save results
./vaccine https://example.com/vulnerable?page=1 -o result.txt

# Use POST method for injection testing
./vaccine https://example.com/login -X POST
```

---

## ⚙️ Command-line Options

| Option | Description                                                     |
| ------ | --------------------------------------------------------------- |
| `-o`   | Archive file name to save results (default: `archive_file.txt`) |
| `-X`   | HTTP method (`GET` or `POST`). Default is `GET`.                |
| `URL`  | Target URL with vulnerable parameter                            |

---

## 🛠️ Installation & Setup

### Python version (recommended)

* Requires: `Python 3.7+`
* Dependencies: `requests`, `beautifulsoup4`
  Install them via:

```bash
pip install -r requirements.txt
```

### Run

```bash
chmod +x vaccine.py
./vaccine.py URL [OPTIONS] 
```

---

## 🧪 Testing & Labs

* [PortSwigger Web Security Academy](https://portswigger.net/web-security/sql-injection) : 
  
  - SQLi UNION - GET : 
    Oracle : https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-oracle & MySql : https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-mysql-microsoft
  
  - SQLI BOOLEAN - GET : 
    https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data
  
  - SQLI BOOLEAN - POST : 
    https://portswigger.net/web-security/sql-injection/lab-login-bypass

* [DVWA (Damn Vulnerable Web Application)](http://www.dvwa.co.uk/)
* [bWAPP](https://sourceforge.net/projects/bwapp/)
* Your own sandbox environment


