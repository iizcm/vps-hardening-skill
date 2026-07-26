# Vps Hardening — Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-blue)](LICENSE)
[![Universal AI Agent Skill](https://img.shields.io/badge/Universal-AI_Agent_skill-orange)](#)
[![Category: Devops](https://img.shields.io/badge/Category-Devops-purple)](#)

| Field | Value |
| --- | --- |
| **Name** | `vps-hardening-skill` |
| **Description** | description: Secure a freshly provisioned Ubuntu VPS (RackNerd, DigitalOcean, Vultr, Hetzner, etc. |
| **Category** | devops |
| **Version** | `1.0.0` |
| **Author** | Community |
| **License** | MIT |
| **Platforms** | Linux, macOS, Windows |

---

## What it is

description: Secure a freshly provisioned Ubuntu VPS (RackNerd, DigitalOcean, Vultr, Hetzner, etc.

This is a universal AI agent skill — platform-agnostic and usable inside any modern agent runtime that supports the skill file format. It lets your agent perform a focused task set with proper configuration, reproducible outputs, and safe defaults.

**Important:** Use only on targets you own or have explicit permission to work with. Do not use for unauthorized system access, data scraping, or activities that violate applicable laws or terms of service.

---

## 🇬🇧 English

### Requirements

- A compatible AI agent runtime that supports skills (Hermes, OpenClaw, etc.)
- Python 3.10+ (for skills that delegate to scripts)
- Network access if the skill requires remote data fetching
- Write permissions to your project/output folder

### Installation

```bash
# Copy skill directory into your agent's skills folder (~/.hermes/skills/)
cp -r devops/vps-hardening ~/.hermes/skills/devops/vps-hardening/

# Or install directly from SKILL.md URL (if your runtime supports it)
<agent-cli> skills install https://raw.githubusercontent.com/iizcm/vps-hardening-skill/main/SKILL.md
```

### Step-by-step usage

**Step 1** — Create a project folder:

```bash
mkdir -p ~/projects/example
cd ~/projects/example
```

**Step 2** — Invoke the skill from your agent:

```text
skill_view(name="devops/vps-hardening")
```

Replace the exact syntax with whichever your agent supports (skill loading command varies by runtime).

**Step 3** — Run a task:

```text
Use the vps-hardening skill to do its primary task.
```

Wrap the task in a clear, single-sentence instruction so the agent routes it to the right skill.

**Step 4** — Inspect outputs:

```bash
ls -la out/
```

Most skills write outputs under an `out/` folder by default. Check logs, files, and printable artifacts here.

**Step 5** — Customize for your use case:

- Edit the skill's frontmatter if you want to change its name or add tags.
- Modify pathway defaults inside the skill if you want permanent behavior changes.
- Combine with other skills for compound automation (for example, an HTML generation skill plus a screenshot skill).

### Troubleshooting

| Symptom | Likely cause | Fix |
| --- | --- | --- |
| Skill not found | Not installed in the active skills directory | Re-run the install command above |
| Network timeout | Internet blocked or proxy misconfigured | Check `curl` / `wget` connectivity; configure proxy if needed |
| Permission denied | Output folder not writable | `chmod` / run from a user-owned folder |
| No output produced | Input format unsupported | Validate input matches the skill's expected format |

### Security & safety notes

- Do not embed private keys, seed phrases, or API tokens in outputs or chat logs.
- Placeholders in this README use `<YOUR_*>` notation — replace them before use in production.
- Always simulate or validate outputs before acting on them, especially for write actions.

---

## 🇮🇩 Bahasa Indonesia

### Persyaratan

- Runtime AI agent yang mendukung format skill (Hermes, OpenClaw, dll.)
- Python 3.10+ untuk skill yang menggunakan script eksternal
- Koneksi internet jika skill perlu mengambil data dari luar
- Izin tulis ke folder project/output Anda

### Instalasi

```bash
# Salin folder skill ke direktori skills agent (~/.hermes/skills/)
cp -r devops/vps-hardening ~/.hermes/skills/devops/vps-hardening/

# Atau pasang langsung dari URL SKILL.md yang diverifikasi
<agent-cli> skills install https://raw.githubusercontent.com/iizcm/vps-hardening-skill/main/SKILL.md
```

### Langkah penggunaan

Sama seperti bagian EN, tapi dalam bahasa sehari-hari:

- **Langkah 1** Buat folder proyek
- **Langkah 2** Panggil skill di chat / CLI agent Anda
- **Langkah 3** Jalankan contoh pertama
- **Langkah 4** Cek hasil di folder `out/`
- **Langkah 5** Sesuaikan sesuai kebutuhan

### Troubleshooting (ID)

| Gejala | Kemungkinan penyebab | Solusi |
| --- | --- | --- |
| Skill tidak ditemukan | Belum terpasang | Jalankan ulang perintah install |
| Timeout jaringan | Terblokir / proxy salah | Cek koneksi, atur proxy |
| Permission ditolak | Folder output tidak bisa ditulis | Ubah folder ke milik user Anda |
| Tidak ada output | Format input salah | Sesuaikan input dengan yang diharapkan skill |
| Error API | Token / kunci salah | Ganti credential dengan yang valid |

### Keamanan

- Jangan masukkan private key, mnemonic, atau token API ke dalam output atau chat log.
- Tempat yang disiapkan untuk contoh di README menggunakan format `<YOUR_*>` — ganti sebelum dipakai.
- Selalu validasi output sebelum digunakan, terutama untuk aksi yang berisiko.

---

## Notes

- Update this README when the skill's interface, options, or behavior changes.
- If you fork this repo, keep the MIT license and attribution line intact.
- Report bugs via GitHub Issues on the original repo.

---

## License

MIT — free to use, modify, and distribute.
