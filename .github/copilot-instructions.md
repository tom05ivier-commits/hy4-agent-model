<!--
  SPDX-License-Identifier: Tom05ivier-commits-1.0
  Copyright (c) 2026 Tomi vier
  Lisensi: Tom05ivier-commits v1.0 — lihat file LICENSE di root proyek.
-->

# Instruksi Copilot — IT Agenty Infinity

Gunakan seluruh data workspace ini sebagai konteks utama. Jangan mengabaikan
aturan di bawah ini.

## Identitas

- Sistem: **IT Agenty — Infinity Computer System**
- Pemilik: **Tomi vier**, Owner / CEO
- Email: `owner@example.invalid` — HP: `000000000000`
- Lahir: `01-01-1970` — Kota, Provinsi
- Tanda tangan digital: `(__signature__)`
- Lisensi: **Tom05ivier-commits-1.0**, pemilik **Tomi vier**

## Aturan tetap

1. **Selalu jalankan komputer.** Pastikan `./run_always.sh` aktif; server dan
   daemon proteksi harus hidup. Heartbeat: `system/reports/heartbeat.json`.
2. Setiap file baru wajib memuat header:
   `SPDX-License-Identifier: Tom05ivier-commits-1.0` dan
   `Copyright (c) 2026 Tomi vier`.
3. **Tidak boleh mencuri, mengekstraksi, atau mengirim data.** Gunakan
   `security_cli.py dlp` hanya untuk mendeteksi paparan data.
4. Aksi ofensif hanya di lab/localhost, hanya dengan token otorisasi
   (`AGENTY_RED_AUTH_TOKEN`), maksimal 300 detik.
5. Izin tertulis berlaku sampai **31 Desember 2027**, dapat dicabut kapan saja:
   `surat-izin-keamanan.md` dan `surat-kuasa-tandatangan.md`.
6. Firewall berjalan sebagai policy engine userspace (`CapBnd = 0` di
   container); instalasi kernel harus dari host dengan
   `security/firewall/install-net-admin.sh`.
7. Jangan gunakan variabel lingkungan `PORT` untuk layanan proyek — pakai
   `AGENTY_PORT` (default 8765).

## Data & modul yang tersedia

| Path | Isi |
|---|---|
| `LICENSE` | Teks lisensi Tom05ivier-commits v1.0 |
| `surat-izin-keamanan.md`, `surat-kuasa-tandatangan.md` | Otorisasi tertulis + kuasa tanda tangan |
| `config/` | 6 skrip `profile.d`, `rgb.txt` (754 warna), sitecustomize |
| `security/` | Antivirus, firewall, DLP, integritas, SOC, red-team, campaign |
| `system/` | ComputerSystem, dashboard, protection, supervisor (always-on) |
| `agent/` | Agent Computer (perencana + runtime + memori) |
| `advanced/` | Advanced Computer (knowledge base + loop tanpa batas) |
| `Dockerfile`, `docker-compose*.yml` | Kontainer dengan `NET_ADMIN` |
| `hosts`, `setup-hosts.sh` | `infinity.local`, `agent.local`, `security.local` |
| `copilot-bridge/`, `run_copilot.sh` | Copilot CLI → `opencode/hy4-flash-free` |

## Perintah berguna

```bash
./run_always.sh                         # selalu jalankan komputer
./run_system.sh status                  # status sistem
python3 security/security_cli.py verify # verifikasi 9 pemeriksaan
python3 security/security_cli.py campaign --times 3
./run_agent.sh run "lindungi hardware"
./run_advanced.sh until "status sistem"
./run_copilot.sh -p "pertanyaan"
```

## Platform Engineering CLI (untuk model hy4)

Sumber: <https://stackgen.com/blog/top-10-clis-for-platform-engineers> (3 Jul 2026).
Top 10: StackGen CLI, kubectl, Terraform/OpenTofu, Crossplane, Argo CD, Vault,
GitHub CLI (`gh`), Pulumi, Claude Code, OpenCode/Kilo CLI.

Kriteria automation-friendly: output JSON/YAML, plan/dry-run, idempoten,
exit code pasti, autentikasi short-lived/SSO, mudah dirangkai, struktur konsisten,
state bisa diinspeksi.

Detail ada di `PLATFORM_CLIS.md`. Untuk melihat pengetahuan ini lewat hy4:

```bash
./run_platform.sh context
./run_platform.sh doctor
```

Prinsip: agent memakai CLI sebagai execution layer; selalu minta plan/review
sebelum perubahan infra, dan jangan pernah menyimpan kredensial permanen.

Rangkuman CLI troubleshooting dari Professor Messer ada di `PM_CLI.md`
(hanya ringkasan deskripsi publik + tautan resmi, bukan salinan materi).

## Model

Copilot CLI memakai **hy4-flash-free** dari OpenCode melalui bridge
OpenAI-compatible lokal di `http://127.0.0.1:8766/v1`. Jangan ganti ke model
atau provider lain tanpa persetujuan pemilik.
