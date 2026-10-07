# Frontend SDM RAG

Frontend satu halaman yang bersih dan profesional untuk percakapan Q&A SDM: riwayat pesan, pertanyaan contoh, input pertanyaan, tombol Kirim, indikator status knowledge base, confidence, dan sumber dokumen.

## Kesesuaian dengan Tahap 2

Frontend menyediakan UI sederhana sesuai brief ujian: riwayat percakapan, textbox pertanyaan, dan tombol **Kirim**. Setiap jawaban menampilkan confidence serta sumber chunk yang dikembalikan backend agar proses RAG dapat didemokan dengan jelas.

## Arsitektur

```text
Browser → Frontend static app → Backend REST `/api/chat`
                              ← jawaban + confidence + sources
```

Struktur utama:

- `src/index.html` — halaman aplikasi
- `src/styles.css` — tampilan responsif
- `src/app.js` — state chat dan komunikasi API

Frontend memanggil backend pada `http://localhost:3000` secara default. Untuk deployment, set `window.SDM_API_URL` sebelum `app.js` dijalankan atau ubah konstanta API di `src/app.js`.

## Jalankan

```bash
npx serve src -l 4173
```

Pastikan backend berjalan pada port 3000, atau sesuaikan URL API di `src/app.js`.

## Demo yang disarankan

1. Ajukan pertanyaan tentang Faktor Generik atau SIPK dari PERPOL.
2. Tunjukkan jawaban, confidence, dan sumber chunk.
3. Ajukan pertanyaan di luar knowledge base untuk menunjukkan respons aman.
4. Jelaskan bahwa LLM menggunakan LiteLLM dengan Gemini melalui backend.
