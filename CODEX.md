Project: Hospital Management System (static templates)

Ringkas:
- Repo ini berisi kumpulan halaman HTML statis di `templates/` untuk landing page, auth, pricing, dan dashboard dokter.
- Styling memakai Tailwind CSS via CDN dan font Google (Plus Jakarta Sans) langsung di tiap file HTML.
- Tidak ada backend, routing server, database, atau build system (tidak ditemukan `package.json`, `go.mod`, dsb).
- Struktur halaman dikelompokkan per area, misalnya `templates/dashboard-docter/`.

Konvensi yang ada:
- File HTML lowercase dengan hyphen.
- Setiap halaman memasukkan Tailwind CDN + font + CSS inline per halaman.
- Aset/komponen reusable belum dipisah; duplikasi kemungkinan ada antar halaman.

Tujuan sesi:
- Saat menambah/ubah UI, tetap konsisten dengan gaya Tailwind + font yang sudah dipakai.
- Jika membuat halaman baru, tempatkan di `templates/` atau subfolder yang sesuai.
