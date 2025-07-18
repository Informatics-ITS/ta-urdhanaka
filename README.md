# 🏁 Tugas Akhir (TA) - Final Project

**Nama Mahasiswa**: Urdhanaka Aptanagi  
**NRP**: 5025211123  
**Judul TA**: Implementasi Multi-Tenancy Untuk Provisioning Klaster Kubernetes  
**Dosen Pembimbing**: Royyana Muslim Ijtihadie S.Kom., M.Kom., Ph.D.  
**Dosen Ko-pembimbing**: Prof. Ir. Ary Mazharuddin Shiddiqi S.Kom., M.Comp.Sc., Ph.D., IPM.  

---

## 📺 Demo Aplikasi  
Embed video demo di bawah ini (ganti `VIDEO_ID` dengan ID video YouTube Anda):  

[![Demo Aplikasi](https://i.ytimg.com/vi/zIfRMTxRaIs/maxresdefault.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)  
*Klik gambar di atas untuk menonton demo*

---

## 🛠 Panduan Instalasi & Menjalankan Software  

### Prasyarat  
- Daftar dependensi:
  - Komputer fisik worker:
    - libvirtd
    - Golang v1.24.5
  - Website server:
    - Golang v1.24.5
    - Postgresql container
    - Redis container

### Langkah-langkah  
1. **Clone Repository**  
   ```bash
   git clone https://github.com/Informatics-ITS/TA.git
   ```
2. **Instalasi Dependensi**  
   Sebelum memulai instalasi dependensi, diperlukan beberapa dependensi melalui package manager dari Linux.
   Dalam tugas akhir ini, distribusi Ubuntu digunakan, sehingga
   perintah command line di bawah merupakan perintah command line
   untuk Ubuntu. Untuk distribusi Linux lainnya, dapat mengikuti
   dokumentasi dari package manager distribusi tersebut. Pada
   komputer worker:
   ```bash
   apt install libvirt
   ```
   untuk sistem provisioning:  
   ```bash
   cd ta-urdhanaka # masuk ke root directory dari project
   cd nodes-grpc-local # untuk aplikasi provisioning
   go mod tidy
   ```
   untuk website server:  
   ```bash
   cd ta-urdhanaka # masuk ke root directory dari project
   cd nodes-grpc-frontend
   ```
3. **Konfigurasi**
- Salin/rename file .env.example menjadi .env
- Isi variabel lingkungan sesuai kebutuhan (database, API key, dll.)
4. **Jalankan Aplikasi**  
jalankan website server terlebih dahulu
   ```bash
   python main.py
   npm start      # Contoh untuk Node.js
   ```
5. Buka browser dan kunjungi: `http://localhost:8080`

---

## 📚 Dokumentasi Tambahan

- [![Dokumentasi API]](docs/api.md)
- [![Diagram Arsitektur]](docs/architecture.png)
- [![Struktur Basis Data]](docs/database_schema.sql)

---

## ✅ Validasi

Pastikan proyek memenuhi kriteria berikut sebelum submit:
- Source code dapat di-build/run tanpa error
- Video demo jelas menampilkan fitur utama
- README lengkap dan terupdate
- Tidak ada data sensitif (password, API key) yang ter-expose

---

## ⁉️ Pertanyaan?

Hubungi:
- Penulis: 5025211123@student.its.ac.id
- Pembimbing Utama: [email@pembimbing]
