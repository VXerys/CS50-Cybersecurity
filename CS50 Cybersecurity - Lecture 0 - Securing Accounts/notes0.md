# 🔒 Securing Accounts: A Comprehensive Guide

## 📚 Table of Contents
- [🔒 Securing Accounts: A Comprehensive Guide](#-securing-accounts-a-comprehensive-guide)
  - [📚 Table of Contents](#-table-of-contents)
  - [🌟 Introduction to Account Security](#-introduction-to-account-security)
  - [🔑 Authentication vs. Authorization](#-authentication-vs-authorization)
  - [🛡️ Password Security](#️-password-security)
    - [Brute Force \& Dictionary Attacks](#brute-force--dictionary-attacks)
      - [Password Math](#password-math)
    - [Password Complexity \& Length](#password-complexity--length)
  - [🛠️ NIST Recommendations](#️-nist-recommendations)
  - [🔒 Multi-Factor Authentication (MFA)](#-multi-factor-authentication-mfa)
  - [🎣 Common Threats](#-common-threats)
    - [Credential Stuffing](#credential-stuffing)
    - [Phishing \& Social Engineering](#phishing--social-engineering)
  - [🛠️ Solutions \& Best Practices](#️-solutions--best-practices)
    - [Password Managers](#password-managers)
    - [Passkeys \& Future Technologies](#passkeys--future-technologies)
  - [📚 References](#-references)

---

## 🌟 Introduction to Account Security
Modern accounts (websites, apps, devices) face numerous threats. This guide explores **authentication**, **authorization**, and practical defenses to secure accounts effectively. We’ll cover technical attacks (brute force, phishing) and solutions (password managers, MFA).

[🔙 Back to TOC](#-table-of-contents)

---

## 🔑 Authentication vs. Authorization
- **Authentication**: Proving your identity (e.g., username + password).
- **Authorization**: Determining access rights after authentication (e.g., admin vs. user privileges).

Example:  
🔐 A building key (authentication) grants entry, but authorization defines which rooms you can access.

[🔙 Back to TOC](#-table-of-contents)

---

## 🛡️ Password Security

### Brute Force & Dictionary Attacks
- **Dictionary Attack**: Uses precomputed lists of common words/passwords.
- **Brute Force Attack**: Tries **all possible combinations** systematically.

#### Password Math
- **4-digit PIN**: Only 10,000 combinations (cracked in <1 second).
- **4-letter password (A-Z)**: 7 million combinations (cracked in seconds).
- **8-character password (A-Z, a-z, 0-9, symbols)**: ~6 quadrillion combinations (practically uncrackable).

💡 **Key Insight**: Longer passwords exponentially increase attack difficulty.

[🔙 Back to TOC](#-table-of-contents)

---

### Password Complexity & Length
- **Avoid**: Dictionary words, repetitive sequences (e.g., `1234`, `aaaa`).
- **Use**: 12+ characters with mixed cases, numbers, and symbols.
- **NIST Guidelines**:  
  - Minimum 8 characters (64+ recommended).  
  - Allow spaces and Unicode characters.  
  - **No periodic forced changes** (leads to weak incremental passwords).

[🔙 Back to TOC](#-table-of-contents)

---

## 🛠️ NIST Recommendations
1. **Block Common Passwords**: Reject passwords from breach databases.
2. **No Password Hints**: Avoid questions like "first pet’s name."
3. **Rate Limiting**: Lock accounts after repeated failed attempts.
4. **No Arbitrary Changes**: Forced resets increase weak password reuse.

[🔙 Back to TOC](#-table-of-contents)

---

## 🔒 Multi-Factor Authentication (MFA)
Three factors for robust security:
1. **Knowledge**: Password/PIN.
2. **Possession**: Physical device (e.g., phone, YubiKey).
3. **Inherence**: Biometrics (fingerprint, face ID).

⚠️ **Avoid SMS-based 2FA** (SIM-swapping risk). Use authenticator apps (Google Authenticator, Authy) instead.

[🔙 Back to TOC](#-table-of-contents)

---

## 🎣 Common Threats

### Credential Stuffing
- **Risk**: Reusing passwords across sites.  
- **Solution**: Unique passwords for every account.

### Phishing & Social Engineering
- **Phishing**: Fake emails/sites mimicking trusted entities (e.g., "Reset your PayPal password").  
- **Social Engineering**: Manipulating users into revealing secrets (e.g., "Write your password on paper" trick).

🛡️ **Defense**:  
- Verify URLs before logging in.  
- Never share credentials via email/phone.  
- Use password managers to auto-fill **only on legitimate sites**.

[🔙 Back to TOC](#-table-of-contents)

---

## 🛠️ Solutions & Best Practices

### Password Managers
- **Benefits**:  
  - Generate/store unique, complex passwords.  
  - Auto-fill credentials on verified sites.  
  - Sync across devices (e.g., iCloud Keychain, Google Password Manager).  
- **Primary Password**: Use a **strong, memorable phrase** (e.g., `CorrectHorseBatteryStaple`).

### Passkeys & Future Technologies
- **Passkeys**: Cryptographic keys stored on devices (no passwords needed).  
- **Advantages**:  
  - Immune to phishing.  
  - Sync securely via Apple/Google/Microsoft ecosystems.

[🔙 Back to TOC](#-table-of-contents)

---

## 📚 References
1. [CS50 Cybersecurity Lecture 0: Securing Accounts](https://www.youtube.com/watch?v=kUovJpWqEMk)
2. [NIST Password Guidelines](https://pages.nist.gov/800-63-3/sp800-63b.html)
3. [Have I Been Pwned?](https://haveibeenpwned.com) (Check breached passwords)
4. [Password Manager Comparison](https://www.consumerreports.org/password-managers)

[🔙 Back to TOC](#-table-of-contents)