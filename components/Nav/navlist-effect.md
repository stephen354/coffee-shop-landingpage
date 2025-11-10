🧩 custom={[index * 0.04, (name.length - index) * 0.01]}

Kamu mengirim array berisi dua nilai ke setiap huruf:

custom = [index * 0.04, (name.length - index) * 0.01]

Artinya:

i[0] = delay saat masuk (enter)
→ berdasarkan posisi huruf (index \* 0.04), jadi huruf pertama muncul dulu, lalu berikutnya menyusul.

i[1] = delay saat keluar (exit)
→ berdasarkan panjang nama dikurangi posisi ((name.length - index) \* 0.01), jadi huruf terakhir keluar dulu, baru yang pertama — efeknya seperti “wave balik”.

💡 Contoh konkret

Misal:

name = "HELLO" // length = 5

Index Huruf custom i[0] (enter delay) i[1] (exit delay)
0 H [0, 0.05] 0s 0.05s
1 E [0.04, 0.04] 0.04s 0.04s
2 L [0.08, 0.03] 0.08s 0.03s
3 L [0.12, 0.02] 0.12s 0.02s
4 O [0.16, 0.01] 0.16s 0.01s

➡️ Jadi efeknya:

Saat masuk: huruf muncul dari kiri ke kanan (delay makin besar).

Saat keluar: huruf hilang dari kanan ke kiri (delay makin kecil).

✨ Ringkasnya:

custom → data unik dikirim ke variant.

i → nilai custom di dalam variant.

i[0] → digunakan buat delay animasi masuk.

i[1] → digunakan buat delay animasi keluar.
