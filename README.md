<div align="center">

# 💜 Valentine 26

### Kartu Valentine interaktif bertema ungu dengan efek *glassmorphism*

*Satu halaman web kecil, dibuat dengan penuh cinta untuk orang tersayang.* 🌷

<br>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-8A2BE2?style=for-the-badge&logo=github&logoColor=white)
![Tema](https://img.shields.io/badge/Tema-Ungu%20%F0%9F%92%9C-c2a5ff?style=for-the-badge)
![Tahun](https://img.shields.io/badge/Valentine-2026-ff4ddd?style=for-the-badge)

<br>

[✨ Fitur](#-fitur) •
[🎬 Alur Halaman](#-alur-halaman) •
[🛠️ Teknologi](#️-teknologi) •
[📁 Struktur](#-struktur-proyek) •
[🚀 Menjalankan](#-cara-menjalankan) •
[🌐 Deploy](#-deploy-ke-github-pages) •
[✏️ Kustomisasi](#️-cara-kustomisasi)

</div>

---

## 💌 Tentang Proyek

**Valentine 26** adalah halaman web statis berisi kejutan Valentine yang interaktif. Penerima akan diajak memilih jawaban, lalu mendapat **buket bunga animasi**, **kado** yang bisa dibuka, dan **surat cinta** yang bisa disalin.

Seluruh proyek hanya satu file HTML (`v.html`) tanpa framework dan tanpa dependensi apa pun, jadi ringan dan mudah diubah.

> 💡 **Ide utamanya:** tombol **"Moh"** (tidak) akan *kabur* setiap kali didekati kursor, sementara tombol **"Mw"** (ya) terus membesar. Jadi satu-satunya pilihan yang masuk akal hanyalah *ya*. 😼

---

## ✨ Fitur

| | Fitur | Keterangan |
|:-:|---|---|
| 💜 | **Floating Hearts** | Emoji hati ungu transparan melayang naik tanpa henti dengan ukuran dan kecepatan acak |
| 🪟 | **Glassmorphism** | Kartu dan panel berbahan kaca buram (`backdrop-filter: blur`) dengan border putih lembut |
| 😼 | **Tombol "Moh" Kabur** | Tombol penolakan berpindah posisi acak saat kursor mendekat (`onmouseover`) |
| 📈 | **Tombol "Mau" Membesar** | Tombol persetujuan otomatis membesar dan bercahaya tiap tombol "Moh" kabur |
| 💬 | **Pesan Usil** | Muncul teks jahil saat penerima mencoba menekan tombol penolakan |
| 💐 | **Buket Animasi** | Lima bunga (💐 🌷 🌸 🌹 🌼) bergoyang lembut dengan animasi bergelombang |
| 🎁 | **Kado Interaktif** | Kado yang bisa dibuka dan ditutup, berisi kejutan emoji |
| 💌 | **Surat Cinta** | Amplop yang bisa dibuka, lengkap dengan tombol **copy surat** ke clipboard |
| 😿 | **Panel "No"** | Halaman khusus jika penerima nekat memilih tidak, lengkap dengan tombol kembali |
| 📱 | **Responsif** | Tampilan menyesuaikan layar HP maupun desktop |

---

## 🎬 Alur Halaman

```mermaid
flowchart TD
    A([🌐 Halaman dibuka]) --> B{💜 Mau jadi Valentine-ku?}
    B -- "💜 Mau" --> C[💐 Panel Buket Bunga]
    B -- "😿 Moh" --> D[😿 Panel No]
    B -. "kursor mendekat" .-> E[🏃 Tombol Moh kabur<br/>+ tombol Mau membesar]
    E -.-> B
    D -- "kembali" --> B
    C --> F[🎁 Panel Kado]
    C --> G[💌 Panel Surat]
    F <--> G
    F -- "buka kado" --> H[🧸 Isi kado terbuka]
    G -- "buka surat" --> I[💜 Isi surat terbuka]
    I -- "copy surat" --> J[📋 Tersalin ke clipboard]
```

---

## 🛠️ Teknologi

| Teknologi | Kegunaan |
|---|---|
| **HTML5** | Struktur halaman dalam satu file (`v.html`) |
| **CSS3** | Gradien, glassmorphism, `@keyframes` animasi, dan layout flexbox |
| **JavaScript (Vanilla)** | Navigasi antar panel, animasi tombol kabur, hati melayang, dan Clipboard API |
| **GitHub Actions** | Deploy otomatis ke GitHub Pages setiap push ke `main` |

### 🎨 Palet Warna

| Warna | Kode | Penggunaan |
|:-:|---|---|
| ![#d9c2ff](https://img.shields.io/badge/-%20%20%20-d9c2ff?style=flat-square) | `#d9c2ff` | Gradien background (awal) |
| ![#c2a5ff](https://img.shields.io/badge/-%20%20%20-c2a5ff?style=flat-square) | `#c2a5ff` | Gradien background (tengah) |
| ![#e5d5ff](https://img.shields.io/badge/-%20%20%20-e5d5ff?style=flat-square) | `#e5d5ff` | Gradien background (akhir) |
| ![#be96ff](https://img.shields.io/badge/-%20%20%20-be96ff?style=flat-square) | `rgba(190,150,255)` | Tombol utama |
| ![#4e2d62](https://img.shields.io/badge/-%20%20%20-4e2d62?style=flat-square) | `#4e2d62` | Warna teks |

---

## 📁 Struktur Proyek

```text
valentine26/
├── 📂 .github/
│   └── 📂 workflows/
│       └── ⚙️ static.yml     # Workflow deploy otomatis ke GitHub Pages
└── 💜 v.html                  # Halaman utama (HTML + CSS + JS)
```

---

## 🚀 Cara Menjalankan

### Opsi 1 — Langsung di Browser
```bash
git clone https://github.com/NabilSuryaa/valentine26.git
cd valentine26
```
Lalu **double-click** file `v.html`. Tidak perlu instalasi apa pun.

### Opsi 2 — Dengan Local Server
```bash
# Python
python -m http.server 8000

# atau Node.js
npx serve .
```
Buka **http://localhost:8000/v.html** di browser.

---

## 🌐 Deploy ke GitHub Pages

Proyek ini sudah dilengkapi workflow `static.yml` yang akan men-deploy seluruh isi repo secara otomatis setiap kali ada **push ke branch `main`**.

**Aktifkan sekali saja:**
1. Buka repository di GitHub → **Settings → Pages**
2. Pada **Build and deployment → Source**, pilih **GitHub Actions**
3. Push perubahan ke `main`, lalu pantau prosesnya di tab **Actions**
4. Setelah hijau ✅, halaman bisa dibuka di:

```text
https://nabilsuryaa.github.io/valentine26/v.html
```

> 📌 **Catatan:** karena file utamanya bernama `v.html` (bukan `index.html`), alamat dasar `https://nabilsuryaa.github.io/valentine26/` akan menampilkan *404*. Untuk membuka langsung dari alamat dasar, ubah nama `v.html` menjadi `index.html`.

### Rangkuman Workflow `static.yml`

| Langkah | Fungsi |
|---|---|
| **Checkout** | Mengambil isi repository |
| **Setup Pages** | Menyiapkan konfigurasi GitHub Pages |
| **Upload artifact** | Mengunggah seluruh repo (`path: '.'`) |
| **Deploy to GitHub Pages** | Mempublikasikan situs |

Workflow juga bisa dijalankan manual lewat **Actions → Run workflow** (`workflow_dispatch`).

---

## ✏️ Cara Kustomisasi

Semua isi ada di `v.html`. Cari bagian berikut untuk menyesuaikannya:

| Ingin mengubah… | Cari di `v.html` |
|---|---|
| Pertanyaan utama | Elemen `.ngeselin-text` |
| Teks tombol Ya / Tidak | Tombol `#yesBtn` dan `#noBtn` |
| Pesan jahil saat "Moh" ditekan | Variabel `msg.innerHTML` di fungsi `runAway()` |
| Bunga di buket | Elemen `.flower-emoji` di dalam `.flower-arrangement` |
| Isi kado | Elemen `.gift-open-content` |
| Isi surat | Elemen `.message-paper` |
| Teks yang disalin | Variabel `text` di fungsi `copyMessage()` |
| Warna tema | Nilai `rgba(...)` dan gradien pada `body` di bagian `<style>` |
| Kecepatan hati melayang | Interval `setInterval(createHeart, 300)` (makin kecil, makin banyak) |

> 💡 **Tips:** teks surat di layar (`.message-paper`) dan teks yang disalin (`copyMessage()`) ditulis terpisah. Ubah keduanya supaya isinya sama.

---

## 📸 Pratinjau

> Tambahkan screenshot supaya README makin menarik:
> 1. Simpan gambar di folder `screenshots/`
> 2. Tampilkan dengan baris berikut:
>
> ```markdown
> <img src="screenshots/preview.png" alt="Preview Valentine 26" width="600">
> ```

---

<div align="center">

<br>

**Dibuat dengan 💜 oleh [NabilSuryaa](https://github.com/NabilSuryaa)**

*Valentine 2026*

</div>
