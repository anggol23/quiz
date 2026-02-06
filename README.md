<<<<<<< HEAD
# QuizMaster - Platform Kuis Interaktif

Platform kuis online yang memungkinkan guru membuat kuis dan siswa mengerjakan dengan soal pilihan ganda dan essay.

## Fitur

- ✅ **Guru (Teacher)**
  - Buat kuis dengan soal pilihan ganda dan essay
  - Generate soal dari dokumen teks
  - Acak urutan soal
  - Kelola dan hapus kuis
  - Lihat hasil peserta

- ✅ **Siswa (Student)**
  - Join kuis dengan kode
  - Isi data diri (nama, nomor absen)
  - Jawab soal pilihan ganda dan essay
  - Lihat hasil dan review jawaban

- ✅ **Fitur Umum**
  - Desain modern dengan glassmorphism
  - Responsive design (desktop, tablet, mobile)
  - Penyimpanan data di localStorage
  - Mode gelap/terang otomatis

## Cara Menggunakan

### Untuk Guru
1. Buka aplikasi dengan `?role=teacher` atau klik tombol "Guru"
2. Klik "Buat Kuis Baru"
3. Isi judul, deskripsi, dan soal
4. Pilih tipe soal (Pilihan Ganda atau Essay)
5. Centang "Acak urutan soal" jika ingin
6. Klik "Simpan Kuis"

### Untuk Siswa
1. Buka aplikasi dengan `?role=student` atau klik tombol "Siswa"
2. Masukkan kode kuis
3. Isi nama lengkap dan nomor absen
4. Jawab semua soal
5. Klik "Selesai" untuk submit
6. Lihat hasil dan review

## Teknologi

- HTML5
- CSS3 (Tailwind CSS)
- JavaScript Vanilla
- LocalStorage API

## Instalasi & Deployment

### Local
1. Clone atau download repository
2. Buka file `quiz.html` di browser

### Vercel
1. Push repository ke GitHub
2. Buka [Vercel](https://vercel.com)
3. Klik "New Project"
4. Connect GitHub repository
5. Deploy otomatis

### Netlify
1. Push repository ke GitHub
2. Buka [Netlify](https://app.netlify.com)
3. Click "New site from Git"
4. Connect GitHub repository
5. Deploy otomatis

## URL Akses

```
# Mode Guru (Default)
https://yourdomain.com
https://yourdomain.com?role=teacher

# Mode Siswa
https://yourdomain.com?role=student
```

## Struktur Data

### Quiz
```json
{
  "type": "quiz",
  "quiz_id": "quiz_1234567890",
  "quiz_title": "Kuis Matematika",
  "quiz_description": "Bab 1 - Bilangan",
  "quiz_questions": "[{...}]",
  "quiz_shuffle": true,
  "quiz_created_at": "2026-02-06T..."
}
```

### Question
```json
{
  "text": "Pertanyaan?",
  "type": "multiple|essay",
  "options": {"a": "...", "b": "...", "c": "...", "d": "..."},
  "correct": "a"
}
```

### Result
```json
{
  "type": "result",
  "result_id": "result_1234567890",
  "result_quiz_id": "quiz_1234567890",
  "result_participant_name": "John Doe",
  "result_participant_number": "15",
  "result_score": 8,
  "result_total": 10,
  "result_answers": "[...]",
  "result_completed_at": "2026-02-06T..."
}
```

## Catatan

- Data disimpan di localStorage browser (max ~5-10MB)
- Untuk production, gunakan backend database
- Soal essay tidak dihitung otomatis, perlu review manual

## Lisensi

MIT

## Author

Created with ❤️ for education
=======
# quiz
>>>>>>> c38b032d3a034f0ee74540b77b3477800aa42bfa
