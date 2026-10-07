# Frontend SDM RAG

Frontend satu halaman yang bersih dan profesional untuk percakapan Q&A SDM: riwayat pesan, pertanyaan contoh, input pertanyaan, tombol Kirim, indikator status knowledge base, confidence, dan sumber dokumen.

Frontend memanggil backend pada `http://localhost:3000` secara default. Untuk deployment, set `window.SDM_API_URL` sebelum `app.js` dijalankan atau ubah konstanta API di `src/app.js`.

## Jalankan

```bash
npx serve src -l 4173
```
