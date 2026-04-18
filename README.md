# 🔐 RABE - Revoke Access Without Delay

[![Download RABE](https://img.shields.io/badge/Download-RABE-6f42c1?style=for-the-badge&logo=github)](https://github.com/Comprehendible-genuslobelia764/RABE/releases)

## 📥 Download RABE

Visit this page to download the Windows release files:

https://github.com/Comprehendible-genuslobelia764/RABE/releases

1. Open the link above in your browser.
2. Find the latest release at the top of the page.
3. Download the Windows file if one is listed there.
4. Save the file to a folder you can find again.

If the release includes a setup file or package file, download that file and use it as your main app file.

## 🖥️ What RABE Does

RABE is a tool for revocable attribute-based encryption. In simple terms, it helps control who can read protected data and lets you remove access when needed.

It is built for cases where access rules must change over time. The app supports:

- User access rules based on attributes
- Immediate revocation of user access
- Time-based key updates
- Secure data protection with policy checks
- Structured access control for encrypted data

## 🪟 Windows Requirements

Before you run RABE on Windows, make sure your system has:

- Windows 10 or Windows 11
- Python 3.8 or later
- A working internet connection for the first setup
- About 200 MB of free disk space
- Permission to install local tools on your PC

RABE also uses these Python packages:

- Charm-Crypto 0.5
- pyparsing

Charm-Crypto depends on GMP and PBC libraries, which may need to be installed first.

## 📂 Files in the Repository

These files help build and test the app:

- `FABEO.py` — base CP-ABE flow with setup, key generation, encrypt, and decrypt
- `Rabe.py` — revocable ABE logic with user revocation, time rules, and key updates
- `Msp.py` — access structure support
- `policytree.py` — policy parsing
- `secretutil.py` — key helper tools

## 🚀 Run the App on Windows

Use these steps after you download the release or clone the repo.

1. Install Python 3.8 or later.
2. Open Command Prompt.
3. Go to the folder that contains the project files.
4. Install the Python packages the project needs.
5. Run the main test file.

Example commands:

```bash
python --version
pip install pyparsing
python Rabe.py
```

If your system uses `python3` instead of `python`, use:

```bash
python3 Rabe.py
```

## 🧩 Install Required Python Tools

If you need to set up the package files by hand, install the Python package first:

```bash
pip install pyparsing
```

Charm-Crypto needs extra system libraries. If you run into install issues, install GMP and PBC before you try again.

A common setup path on Windows is:

1. Install Python.
2. Install the required build tools.
3. Install GMP and PBC support.
4. Install Charm-Crypto 0.5.
5. Install pyparsing.
6. Run `Rabe.py`.

## 🔐 How RABE Works

RABE uses a few clear steps:

- **Setup** creates the base system values
- **KeyGen** creates a user key from access attributes
- **Encrypt** locks data to a rule set
- **Decrypt** checks if the key matches the rule
- **Revocation** removes a user’s access
- **Key update** refreshes keys as time changes

This makes it useful when you need access control that can change after a key is issued.

## 🧪 Test the Program

To check that the app runs, use the test command in the project folder:

```bash
python3 Rabe.py
```

If that does not work on your PC, use:

```bash
python Rabe.py
```

A successful run should finish without errors and print the test output in the terminal.

## 🛠️ Common Setup Problems

If the app does not start, check these items:

- Python is installed and added to PATH
- You are in the correct folder
- The required packages are installed
- Charm-Crypto installed without errors
- GMP and PBC are present on your system

If Windows blocks the file, right-click it and choose to run it with Python from Command Prompt.

## 📁 Suggested Folder Layout

Keep the project files in one folder like this:

- `RABE`
  - `FABEO.py`
  - `Rabe.py`
  - `Msp.py`
  - `policytree.py`
  - `secretutil.py`

This makes it easier to run the test file and find each module.

## 🔎 When to Use This Project

Use RABE when you need:

- Controlled access to encrypted data
- User revocation without changing everything by hand
- Time-based access updates
- Attribute-based rules for file access
- A Python project for encryption testing and research

## ⚙️ Basic Workflow

A simple use flow looks like this:

1. Set up the system.
2. Create user keys with selected attributes.
3. Encrypt data under a policy.
4. Share the encrypted file.
5. Revoke access when needed.
6. Update keys for the next time period.
7. Decrypt only if the policy matches

## 📄 License

Check the repository for license details before use.