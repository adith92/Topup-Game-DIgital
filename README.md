# 🌟 FitBite - Healthy Food-Tech Demo untuk Indonesia 🇮🇩🍲💪

**FitBite** adalah aplikasi demo inovatif yang menggabungkan **AI + makanan sehat khas Indonesia**! 
Pilih goal tubuh kamu, masukkan bahan makanan yang ada di dapur, dapatkan **rekomendasi resep sehat berbasis AI**, estimasi nutrisi lengkap, dan simulasi workflow catering dalam hitungan detik! ⚡🥗

![FitBite Preview](public/fitbite-preview.svg)

## 🗺️ Alur Kerja Aplikasi (Flowchart)

```mermaid
flowchart TD
    A[🎯 Pilih Goal Tubuh<br/>💪 Weight Loss / Muscle Gain / Balance] 
    --> B[🛒 Input Bahan Makanan Tersedia<br/>Tempe • Kangkung • Ayam Kampung dll]
    B --> C[🧠 AI Pantry Wizard<br/>🤖 atau Fallback Lokal Database]
    C --> D[📊 Estimasi Nutrisi Lengkap<br/>Kalori • Protein • Karbo • Lemak]
    D --> E[🍱 Simulasi Catering Workflow<br/>Pesan • Jadwal • Porsi]
    E --> F[🎉 Rekomendasi Resep Siap Masak!<br/>Ayam Sambal Matah • Protein Bowl dll]
```

## ✨ Fitur Utama

| Fitur                  | Status             | Keterangan |
|------------------------|--------------------|------------|
| **Landing Page**       | ✅ **Done**        | Hero section keren + CTA |
| **Body Check**         | ✅ **Done**        | Pilih goal tubuh |
| **Ingredient Input**   | ✅ **Done**        | Input bahan lokal Indonesia |
| **AI Pantry Wizard**   | ✅ **Done**        | Rekomendasi resep berbasis AI |
| **Nutrition Estimate** | ✅ **Done**        | Estimasi nutrisi akurat |
| **Catering Workflow**  | ✅ **Done**        | Simulasi catering lengkap |
| **Admin Dashboard**    | 🔄 **In Progress** | Kelola resep & analytics |
| **AI Health API**      | ✅ **Done**        | Ready untuk integrasi |

## 🛣️ Route Demo

| Route                | Fungsi |
|----------------------|--------|
| `/`                  | Landing Page + Hero |
| `/body-check`        | Body Goal Selection |
| `/ingredients`       | Input Bahan Makanan |
| `/recommend`         | AI Pantry Wizard + Hasil |
| `/nutrition`         | Detail Estimasi Nutrisi |
| `/catering`          | Simulasi Catering |
| `/admin`             | Admin Dashboard (demo) |

## 🔌 API Routes

| Method | Endpoint                  | Fungsi |
|--------|---------------------------|--------|
| `POST` | `/api/recommend`          | Generate resep AI |
| `POST` | `/api/nutrition`          | Estimasi nutrisi |
| `GET`  | `/api/ingredients`        | Daftar bahan lokal |
| `POST` | `/api/catering`           | Simulasi catering workflow |

## 📌 Contoh Use Case

**Bahan yang tersedia:** `dada ayam, nasi merah, tempe, kangkung, telur` 🐔🍚🥬

**Hasil Rekomendasi AI:**
- 🍛 **Ayam Sambal Matah Brown Rice** (High Protein)
- 🥬 **Tumis Tahu Tempe Sayur Hijau** (Balanced)
- 💪 **Protein Bowl Catering** (Meal Prep Ready)

## 🛠️ Tech Stack

- **Next.js 15** + App Router ⚡
- **TypeScript** 🔷
- **Tailwind + shadcn/ui** (Responsive)
- **OpenRouter-ready AI** 🤖
- **Local Nutrition Database** (Indonesia-focused)
- **Vercel** Deployment ☁️

## 🚀 Cara Menjalankan Lokal

```bash
git clone https://github.com/adith92/Fitbite.git
cd Fitbite
npm install
npm run dev
```

Buka [http://localhost:3000](http://localhost:3000)

## ☁️ Deployment

- **Platform**: Vercel
- **Project**: `fitbitedemo`
- **Branch**: `main`
- **Build Command**: `npm run build`

## 📈 Current Version & Roadmap

**Version**: **v0.1.0 MVP Demo** 🟢 (Mei 2026)

**Roadmap**:
- ✅ v0.1.0 – Core AI + Nutrition + Catering
- 🔄 v0.2.0 – Auth, Save Resep, Sharing
- 🚀 v1.0.0 – Full Catering Marketplace + PWA
- 🌟 v2.0.0 – AR Scanner + Integrasi Delivery

## 📊 Hasil Analisa & Rekomendasi Pengembangan

**Potensi**: Sangat tinggi di pasar food-tech Indonesia 🇮🇩
- Fokus bahan lokal + AI personalisasi = Unique Selling Point kuat
- Cocok untuk tren healthy eating + meal prep

**Rencana Pengembangan Cepat**:
1. Tambah autentikasi user
2. Integrasi OpenRouter production
3. Dark mode + PWA
4. Export resep ke PDF/WhatsApp
5. Database nutrisi yang lebih lengkap

## 🛡️ Quality & Safety Notes

- Estimasi nutrisi bersifat **approximate** dan untuk referensi saja
- Bukan pengganti konsultasi dokter / ahli gizi
- Privacy-first

## 💖 Final Words

**Mari sehatkan Indonesia satu piring demi satu piring!** 🇮🇩💪🥗

Terima kasih telah mencoba **FitBite**!

Ada ide atau feedback? Langsung buka **Issue** atau **Pull Request** ya!

**#SehatBersamaFitBite** 🍛🚀

Made with ❤️ for a healthier Indonesia
