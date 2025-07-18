# 🔍 Path Payloads Collection

Selamat datang di repositori **Path Payloads** — kumpulan payload lengkap yang dirancang khusus untuk kebutuhan **bruteforce path** dan **directory discovery** dalam kegiatan **penetration testing** maupun **bug bounty**.

## 📂 Isi Repositori

Berisi berbagai file wordlist yang disusun berdasarkan jenis target dan teknik serangan:
- `common-paths.txt` → Path umum ditemukan di berbagai server
- `admin-panels.txt` → Panel login dan dashboard admin
- `upload-points.txt` → Path terkait file upload
- `backup-and-config.txt` → Path backup, konfigurasi, dan credential
- `cms-specific/` → Folder berisi path khusus CMS (WordPress, Joomla, Laravel, Moodle, dll)
- `api-endpoints.txt` → Endpoint umum untuk REST API dan backend
- `dev-debug-paths.txt` → Path development dan debugging (misal: `/test`, `/debug`, `/old`, dll)

## 🎯 Tujuan

- Mempermudah proses bruteforce dan fuzzing path tersembunyi
- Mempercepat identifikasi endpoint sensitif
- Menyediakan wordlist terfokus untuk bypass dan reconnaissance

## ⚔️ Tools yang Direkomendasikan

- [Gobuster](https://github.com/OJ/gobuster)
- [FFUF](https://github.com/ffuf/ffuf)
- [Dirsearch](https://github.com/maurosoria/dirsearch)
- [Wfuzz](https://github.com/xmendez/wfuzz)

## 🧠 Contoh Penggunaan

```bash
# Menggunakan ffuf
ffuf -w wordlists/admin-panels.txt -u https://target.com/FUZZ -mc 200,403

# Menggunakan gobuster
gobuster dir -u https://target.com/ -w wordlists/common-paths.txt -t 50 -x php,html,zip
