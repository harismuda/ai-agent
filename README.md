# Simple AI Coding Assistant (Versi Gratis) 🤖

Proyek ini adalah contoh sederhana bagaimana membuat AI Coding Assistant berbasis Command Line Interface (CLI) menggunakan Python. Versi ini menggunakan API dari **Google Gemini** karena memiliki *Free Tier* (kuota gratis) yang sangat besar dan selamanya (tanpa perlu kartu kredit).

Aplikasi ini akan membaca file kode sumber Anda dan memberikan review, termasuk deteksi bug, saran perbaikan, dan *best practice*.

## Daftar Isi
1. [Persiapan dan Prasyarat](#persiapan-dan-prasyarat)
2. [Cara Mendapatkan API Key Google Gemini](#cara-mendapatkan-api-key-google-gemini)
3. [Instalasi](#instalasi)
4. [Konfigurasi Keamanan (Environment Variable)](#konfigurasi-keamanan-environment-variable)
5. [Cara Menjalankan](#cara-menjalankan)
6. [Langkah Selanjutnya (Pengembangan Lanjutan)](#langkah-selanjutnya)
7. [Kontribusi](#kontribusi)

---

## Persiapan dan Prasyarat
Sebelum mulai, pastikan Anda sudah menginstal:
- **Python** (versi 3.9 atau lebih baru disarankan). Bisa diunduh di [python.org](https://www.python.org/).

---

## Cara Mendapatkan API Key Google Gemini (GRATIS)
Agar program ini bisa berkomunikasi dengan AI Gemini, Anda memerlukan kunci rahasia. Berikut cara mendapatkannya:
1. Buka situs [Google AI Studio](https://aistudio.google.com/app/apikey) dan login menggunakan akun Google/Gmail Anda.
2. Di menu sebelah kiri, klik **"Get API key"**.
3. Klik tombol biru **"Create API key"** > pilih proyek yang ada atau buat proyek baru.
4. **Salin (Copy)** kunci yang muncul (biasanya berawalan `AIza...`). 
   > **PENTING:** Simpan kunci ini baik-baik. Jangan pernah membagikannya ke orang lain atau mengunggahnya ke GitHub/internet secara publik!

---

## Instalasi
Buka terminal (Command Prompt / PowerShell) di komputer Anda, lalu jalankan perintah berikut untuk menginstal library (pustaka) yang dibutuhkan:

```bash
pip install google-generativeai python-dotenv
```
*Penjelasan:*
- `google-generativeai`: Library resmi untuk berkomunikasi dengan server AI Google Gemini.
- `python-dotenv`: Library untuk membaca file `.env` yang akan kita gunakan menyimpan API Key dengan aman.

---

## Konfigurasi Keamanan (Environment Variable)
Kita tidak boleh menaruh API Key langsung di dalam file kode Python (hardcode). Sebagai gantinya, kita gunakan file `.env`.

1. Di dalam folder proyek yang sama dengan script Python, buatlah sebuah file baru bernama `.env` (tanpa nama depan, langsung `.env`).
2. Buka file `.env` tersebut dengan text editor (Notepad, VS Code, dll), lalu isi dengan:

```env
GEMINI_API_KEY=masukkan_api_key_anda_disini_tanpa_tanda_kutip
```

---

## Cara Menjalankan
1. Siapkan script Python utama (`assistant.py`).
2. Siapkan file kode yang ingin direview (saya sudah sediakan file `contoh.py` yang sengaja dibuat ada sedikit bug).
3. Buka terminal dan arahkan ke folder proyek Anda.
4. Jalankan perintah ini:

```bash
python assistant.py contoh.py
```
5. Tunggu beberapa saat, dan hasil review dari AI akan muncul di terminal!

---

## Langkah Selanjutnya
Jika Anda sudah memahami alur kerja dasar dari program ini, Anda bisa mencoba menambahkan fitur-fitur keren lainnya:
- **Auto-Fix Kode:** Minta AI untuk mengembalikan kode yang sudah diperbaiki, lalu gunakan Python untuk langsung menulis/menimpa file asli dengan kode baru tersebut.
- **Dukungan Banyak Bahasa:** Menambahkan kemampuan membaca berbagai macam file (misal `.js`, `.html`, `.cpp`) dengan membaca ekstensi file.
- **Aplikasi Web:** Mengubah CLI menjadi aplikasi web menggunakan framework sederhana seperti [Streamlit](https://streamlit.io/) atau [Flask](https://flask.palletsprojects.com/) agar memiliki tampilan antarmuka yang ramah pengguna.
- **Percakapan Berkelanjutan (Chat):** Menambahkan loop `while` agar setelah file direview, Anda bisa bertanya lebih lanjut tentang review tersebut tanpa harus mengulang dari awal.

---

## Kontribusi
Proyek ini bersifat **Open Source**. Jika Anda menemukan bug, memiliki ide untuk fitur baru, atau ingin memperbaiki dokumentasi, kontribusi Anda sangat dinantikan! 

Cara berkontribusi:
1. **Fork** repository ini.
2. Buat branch baru untuk fitur atau perbaikan Anda (`git checkout -b fitur-baru-saya`).
3. Lakukan **Commit** perubahan Anda (`git commit -m 'Menambahkan fitur auto-fix'`).
4. **Push** ke branch tersebut (`git push origin fitur-baru-saya`).
5. Buat **Pull Request (PR)** agar bisa kami review.

Jangan ragu untuk ikut serta mengembangkan AI Coding Assistant ini bersama-sama!
