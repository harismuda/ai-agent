# Proyek AI Agent dengan Python 🤖

Proyek ini bertujuan untuk membangun sebuah **AI Agent** berbasis Command Line Interface (CLI) menggunakan Python. Berbeda dengan AI Assistant biasa yang hanya bisa membaca dan membalas chat, **AI Agent** adalah sistem yang memiliki kemampuan untuk *bertindak (take action)*, memanggil fungsi eksternal (seperti search internet, akses file, dll), dan mengambil keputusan secara mandiri untuk menyelesaikan suatu tugas.

Proyek ini menggunakan API dari **Google Gemini** karena memiliki *Free Tier* (kuota gratis) yang sangat besar dan selamanya (tanpa perlu kartu kredit).

## Daftar Isi
1. [Persiapan dan Prasyarat](#persiapan-dan-prasyarat)
2. [Cara Mendapatkan API Key Google Gemini](#cara-mendapatkan-api-key-google-gemini)
3. [Instalasi](#instalasi)
4. [Konfigurasi Keamanan (Environment Variable)](#konfigurasi-keamanan-environment-variable)
5. [Cara Menjalankan](#cara-menjalankan)
6. [Kontribusi](#kontribusi)

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

## Kontribusi
Proyek ini bersifat **Open Source**. Jika Anda menemukan bug, memiliki ide untuk fitur baru, atau ingin memperbaiki dokumentasi, kontribusi Anda sangat dinantikan! 

Cara berkontribusi:
1. **Fork** repository ini.
2. Buat branch baru untuk fitur atau perbaikan Anda (`git checkout -b fitur-baru-saya`).
3. Lakukan **Commit** perubahan Anda (`git commit -m 'Menambahkan fitur auto-fix'`).
4. **Push** ke branch tersebut (`git push origin fitur-baru-saya`).
5. Buat **Pull Request (PR)** agar bisa kami review.

Jangan ragu untuk ikut serta mengembangkan AI Coding Assistant ini bersama-sama!
