# Hospital Management System Template

Template frontend statis untuk sistem manajemen rumah sakit berbasis HTML + Tailwind CSS.

## Project Overview
- Stack: HTML, Tailwind CSS (CDN), vanilla JavaScript, Google Fonts.
- Arsitektur: static multi-page templates (tanpa backend).
- Database: tidak ada DB/ORM di repo ini.
- Entry point: `index.html`.

## Menjalankan Project

### Opsi 1 (direkomendasikan): local server
Jalankan dari root project:

```bash
python3 -m http.server 5500
```

Lalu buka:
- `http://localhost:5500/index.html`

### Opsi 2: buka file langsung
Bisa buka `index.html` langsung di browser, tapi beberapa perilaku biasanya lebih stabil via local server.

## Struktur Folder

```text
.
├── index.html
├── templates
│   ├── landing-page.html
│   ├── pricing.html
│   ├── auth
│   │   ├── sign-in.html
│   │   └── sign-up.html
│   ├── dashboard-admin
│   │   ├── dashboard.html
│   │   ├── user-management.html
│   │   ├── patient-directory.html
│   │   ├── inventory-management.html
│   │   ├── financial-management.html
│   │   ├── schedule-ward-management.html
│   │   └── system-settings-security.html
│   ├── dashboard-patients
│   │   ├── overview.html
│   │   ├── my-appointments.html
│   │   ├── medical-records.html
│   │   ├── prescriptions.html
│   │   └── billing.html
│   └── dashboard-docter
│       ├── dashboard.html
│       ├── patiensts.html
│       ├── appointments.html
│       ├── schedules.html
│       ├── chats.html
│       ├── reports.html
│       └── settings.html
├── CODEX.md
└── CLAUDE.MD
```

## Alur Penggunaan
1. Buka `index.html`.
2. Klik **Login** untuk masuk ke halaman `templates/auth/sign-in.html`.
3. Gunakan akun demo di bawah untuk masuk ke dashboard sesuai role.

## Kredensial Demo Login
Di `templates/auth/sign-in.html`, login bersifat mock (client-side):

- Admin
  - Email: `admin@gmail.com`
  - Password: `password`
  - Redirect: `templates/dashboard-admin/dashboard.html`
- Patient
  - Email: `patient@gmail.com`
  - Password: `password`
  - Redirect: `templates/dashboard-patients/overview.html`
- Doctor
  - Email: `docter@gmail.com`
  - Password: `password`
  - Redirect: `templates/dashboard-docter/dashboard.html`

## Konvensi Kode yang Dipakai
- Penamaan file: lowercase + hyphen (`my-appointments.html`, `financial-management.html`).
- Setiap halaman biasanya punya:
  - Tailwind CDN
  - Google Fonts
  - `tailwind.config` inline
  - CSS dan JavaScript inline dalam file yang sama
- Navigasi antar halaman memakai link relatif (`href="..."`).
- Data bersifat statis/mock (tanpa API call).

## Reusable Patterns
- Sidebar dashboard per role (admin/patient/doctor).
- Card metrics, tabel, badge status, dan komponen form.
- Utility class Tailwind + variabel CSS custom di tiap halaman.
- Interaksi JS ringan: menu mobile, toggle password, filter tab, mock loading, chart sederhana.

## Hal yang Perlu Diperhatikan
- Tidak ada sistem auth backend; semua login hanya simulasi.
- Tidak ada validasi/penyimpanan data server-side.
- Ketergantungan CDN (Tailwind, Google Fonts, beberapa image URL) butuh koneksi internet.
- Ada typo naming yang sudah dipakai konsisten di repo:
  - folder `dashboard-docter`
  - file `patiensts.html`
  Ubah nama ini harus sekalian update semua link terkait.

## Menambah Halaman Baru
1. Simpan file baru di folder yang sesuai (`templates/...`).
2. Salin struktur `<head>` dari halaman serupa agar style tetap konsisten.
3. Tambahkan link navigasi di sidebar/navbar halaman terkait.
4. Pastikan semua `href` relatif tetap valid.

## Lisensi
Belum ada file lisensi khusus di repo ini.
