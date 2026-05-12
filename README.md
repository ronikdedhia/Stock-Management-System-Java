# Stock Management System — Java

![Java](https://img.shields.io/badge/Java-SE-ED8B00?logo=java)
![Swing](https://img.shields.io/badge/GUI-Java%20Swing-blue)
![MySQL](https://img.shields.io/badge/Database-MySQL%20%2F%20MariaDB-4479A1?logo=mysql)
![NetBeans](https://img.shields.io/badge/IDE-NetBeans-1B6AC6?logo=apache-netbeans-ide)
![License](https://img.shields.io/badge/License-MIT-yellow)

A desktop Java Swing application for tracking and managing stock inventory. Supports role-based login (Admin and User), add/edit/delete/search stock records, and persists data to a MySQL/MariaDB database.

---

## Features

- Secure login screen with Admin and User roles
- Add, edit, delete, and search stock items by name or ID
- Live clock display on the main dashboard
- Pop-up dialog for detailed stock record operations
- Pre-seeded sample stock data (beverages) for quick testing
- Full SQL dump included for easy database setup

---

## Tech Stack

| Component | Technology |
|---|---|
| Language | Java SE |
| GUI Framework | Java Swing (`javax.swing.JFrame`, `JPanel`, `JTable`) |
| Database | MySQL / MariaDB |
| DB Connectivity | JDBC |
| Build Tool | Apache Ant (NetBeans project) |
| IDE | Apache NetBeans |

---

## Database Schema

Two tables in the `stockdb` database:

| Table | Columns |
|---|---|
| `tblstock` | `id`, `stockname`, `quantity`, `date`, `person` |
| `tbluser` | `userid`, `username`, `password` |

Default admin credentials: **username** `admin` / **password** `admin`

---

## Getting Started

### Prerequisites

- JDK 8+
- MySQL or MariaDB server running locally
- NetBeans IDE (recommended) or any Java IDE

### 1. Set up the database

```bash
mysql -u root -p < stockdb.sql
```

### 2. Configure the JDBC connection

Edit `src/Source.java` (or the DB connection class) to match your MySQL host, username, and password.

### 3. Build and run

**Via NetBeans:**
1. Open the project folder in NetBeans
2. Right-click the project → **Clean and Build**
3. Click **Run**

**Via Ant CLI:**
```bash
ant clean build run
```

---

## File Structure

```
├── src/
│   ├── Login.java / Login.form      # Login screen
│   ├── Home.java  / Home.form       # Main dashboard
│   ├── pop_up.java / pop_up.form    # Stock record pop-up dialog
│   └── Source.java                  # DB connection helper
│   └── icon/                        # UI icons
├── stockdb.sql                       # MySQL database dump
├── build.xml                         # Ant build script
└── nbproject/                        # NetBeans project files
```

---

## Screenshots

> _Add screenshots of the Login, Home dashboard, and stock management dialogs here._

---

## License

This project is licensed under the [MIT License](LICENSE).
