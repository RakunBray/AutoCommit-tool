# 🚀 AutoCommit Tool

Tool otomatisasi commit GitHub yang berjalan menggunakan GitHub Actions. Tool ini akan memperbarui file `TIMESTAMP.txt` secara berkala untuk menjaga aktivitas repository Anda tetap aktif.

## ✨ Fitur

- 🕒 **Scheduled Commit:** Berjalan otomatis setiap 6 jam.
- 🛠 **Manual Trigger:** Dapat dijalankan kapan saja melalui tab Actions di GitHub.
- 📝 **Random Messages:** Menggunakan pesan commit acak dengan emoji menarik.
- ⚡ **Zero Maintenance:** Setelah di-setup, semuanya berjalan otomatis di cloud GitHub.

## 🚀 Cara Setup

1. **Push ke GitHub:**
   Upload semua file ini ke repository Anda di GitHub. Pastikan branch utamanya adalah `master`.

2. **Aktifkan GitHub Actions:**
   - Pergi ke tab **Settings** di repository GitHub Anda.
   - Pilih **Actions** > **General**.
   - Pastikan **Workflow permissions** disetel ke **Read and write permissions**.
   - Klik **Save**.

3. **Setup GitHub Secrets (Opsional tapi Direkomendasikan):**
   - Di GitHub, buka repository Anda.
   - Klik **Settings** > **Secrets and variables** > **Actions**.
   - Klik **New repository secret**.
   - Name: `GH_TOKEN`
   - Secret: (Masukkan token `ghp_...` yang Anda miliki)
   - Klik **Add secret**.

4. **Verifikasi:**
   - Pergi ke tab **Actions**.
   - Pilih workflow **Automated Commit**.
   - Klik **Run workflow** untuk mencoba menjalankan secara manual.

## ⚙️ Kustomisasi

Anda dapat mengubah konfigurasi di file [auto-commit.yml](.github/workflows/auto-commit.yml):

- **Ubah Jadwal:** Ganti nilai `cron` (contoh: `'0 0 * * *'` untuk setiap hari sekali).
- **Ganti Identitas:** Ubah `user.email` dan `user.name` di bagian "Setup Git Configuration".
- **Edit Pesan:** Tambahkan atau ubah isi dari `commit_messages` di bagian "Prepare Commit".

---

Dibuat oleh [mysteria](https://github.com/mysteria223).
