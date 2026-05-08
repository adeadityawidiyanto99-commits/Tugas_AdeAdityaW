# Jawaban Refleksi
1. Mengapa fungsi power() harus dipanggil di dalam term(), bukan sebaliknya? Jelaskan kaitannya dengan Operator Precedence.
   - Karena fungsi power() dipanggil di dalam term() karena dalam matematika, pangkat dikerjakan sebelum perkalian. Dalam struktur kode,
     fungsi yang berada "lebih dalam" atau dipanggil lebih awal dalam hirarki rekursif akan menempati posisi yang lebih rendah di pohon AST,
     sehingga dieksekusi lebih dulu.

2. Apa yang terjadi pada fase Analisis Semantik jika variabel z digunakan dalam kode sumber tetapi tidak ada di symbol_table?
   - Jika variabel z tidak ada di symbol_table, compiler akan melempar ParserError (atau Semantic Error). Ini adalah tugas fase semantik
     untuk memastikan bahwa semua simbol yang digunakan sudah didefinisikan sebelumnya.

3. Jelaskan mengapa dalam TAC, instruksi untuk a ^ 2 harus muncul sebelum instruksi untuk +.
   - TAC adalah representasi kode yang menyederhanakan ekspresi kompleks menjadi maksimal tiga alamat (dua operan, satu hasil). Instruksi
     a^2 harus muncul duluan karena hasilnya dibutuhkan sebagai input untuk operasi penjumlahan berikutnya.
