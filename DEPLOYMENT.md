# Deployment ke Vercel

## Langkah-Langkah Deployment

### 1. Siapkan GitHub Repository
```bash
# Initialize git (jika belum)
git init
git add .
git commit -m "Initial commit: QuizMaster"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/quizmaster.git
git push -u origin main
```

### 2. Deploy ke Vercel

#### Opsi A: Via GitHub (Recommended)
1. Buka https://vercel.com
2. Klik "New Project"
3. Pilih "Import Git Repository"
4. Cari repository `quizmaster`
5. Klik "Import"
6. Settings:
   - Framework: "Other" (bukan Next.js)
   - Build Command: (kosongkan)
   - Output Directory: (kosongkan)
   - Environment Variables: (tidak perlu)
7. Klik "Deploy"

#### Opsi B: Via Vercel CLI
```bash
# Install Vercel CLI
npm install -g vercel

# Login ke Vercel
vercel login

# Deploy
vercel --prod
```

#### Opsi C: Manual Upload
1. Buka https://vercel.com/new
2. Klik "Clone Template"
3. Pilih "HTML"
4. Upload file `quiz.html`
5. Klik "Deploy"

### 3. Custom Domain (Opsional)
1. Di dashboard Vercel, buka project
2. Pergi ke "Settings" → "Domains"
3. Tambah custom domain
4. Ikuti instruksi DNS

## Akses Aplikasi

```
URL: https://your-project-name.vercel.app
URL Guru: https://your-project-name.vercel.app?role=teacher
URL Siswa: https://your-project-name.vercel.app?role=student
```

## Troubleshooting

### File 404
Pastikan `vercel.json` sudah ter-upload dengan benar

### Fitur Tidak Berfungsi
- Clear localStorage: Dev Tools → Application → localStorage → Clear All
- Hard refresh: Ctrl+Shift+R (Windows) atau Cmd+Shift+R (Mac)

### Data Hilang Setelah Refresh
Data disimpan di localStorage, jika clear cache maka data hilang. Ini normal karena belum ada backend database.

## Upgrade ke Backend (Production)

Untuk production dengan data persistence:

1. Setup Node.js + Express backend
2. Setup Database (MongoDB, PostgreSQL, dll)
3. Deploy backend di Heroku/Railway/Digital Ocean
4. Update API calls di quiz.html

Hubungi developer untuk implementasi backend database.
