# Misi Pulang dari Masa Lampau: Kenali Sejarah, Cintai Negara

Permainan web 3D seorang pemain untuk murid Tahun 6 dalam Bahasa Melayu.

## Main terus
Buka `index.html` dalam Chrome, Edge, Firefox atau Safari yang menyokong WebGL 2. Fail ini mengandungi semua kod Three.js dan gaya paparan: tidak memerlukan CDN, pemasangan, akaun atau backend. Jika WebGL tidak tersedia, permainan memaparkan arahan pemulihan dan bukannya butang mula yang tidak bertindak balas.

## GitHub Pages sahaja
1. Muat naik `index.html` dan `LICENSE-three.txt` ke repositori awam GitHub.
2. Settings → Pages → Deploy from a branch → main → /(root) → Save.
3. Tunggu penerbitan GitHub Pages berjaya. Gunakan alamat yang dipaparkan oleh GitHub.

Repositori yang dikenal pasti: https://github.com/emylianuraffifah/misi-pulang
Laman permainan diterbitkan melalui GitHub Pages.

## Kandungan
- `index.html`: edisi kendiri untuk dimainkan dan dihoskan.
- `source/index.html`, `source/main.js`, `source/style.css`: kod sumber yang boleh diedit.
- `source/vendor/`: Three.js tempatan dan lesen MIT.
- `.nojekyll`: memastikan GitHub Pages menghidangkan fail statik.

Untuk menyunting versi sumber, jalankan pelayan statik dari `source/`, contohnya `python3 -m http.server 8080`. Untuk membina semula fail kendiri, gunakan esbuild untuk bundle main.js sebagai IIFE, kemudian inline CSS dan JavaScript dalam source/index.html.

## Kawalan
WASD/anak panah bergerak mengikut arah skrin; klik lantai menggunakan pencarian laluan di sekeliling halangan; Shift pecut; Space lompat; E interaksi; J jurnal; Esc jeda. Seret dunia untuk pusing kamera dalam julat kecil. Telefon mempunyai pad arah, lompat, interaksi dan menu jurnal/jeda.

## Misi
Bermula dalam Gua Cahaya selepas prolog, berjalan keluar menuju Jejak 1, bercakap dengan Penjaga Sejarah, baca dua petunjuk, jawab dua soalan NPC tentang tindakan dan sebab tindakan itu penting, kemudian berjalan ke portal. Urutan: Lembah Bujang → Perigi Hang Li Po → Muzium Matang → Bukit Malawati → pulang ke lawatan sekolah.

Petunjuk memberi 10 mata, setiap jawapan betul memberi 50 mata (dua soalan setiap misi). Maksimum 480 mata. Bacaan berulang tidak menggandakan ganjaran. Jawapan salah menolak 10 mata (minimum 0); jawapan betul memberi 50 mata sekali sahaja bagi setiap soalan. Markah untuk motivasi dan latihan, bukan pentaksiran rasmi. Kemajuan hanya untuk sesi semasa; muat semula mengosongkannya.

## Fakta dan rekaan
Nama lokasi dan fakta ringkas berpandukan Jabatan Muzium Malaysia serta Tourism Malaysia; pautan sumber ada dalam jurnal. Portal, perjalanan masa, watak dan dialog ialah rekaan. Model bangunan dan ilustrasi Ngah Ibrahim ialah gambaran ringkas, bukan rekonstruksi tepat atau foto tokoh. Kisah Hang Li Po dinyatakan sebagai cerita tradisi, bukan semua butirannya dianggap fakta terbukti.

Rujukan:
- https://www.jmm.gov.my/ms/content/muzium-arkeologi-lembah-bujang-0
- https://storage.ebrochures.malaysia.travel/storage/Melaka_Map_Guide_IDB_small.pdf
- https://www.jmm.gov.my/ms/content/muzium-matang-0
- https://www.malaysia.travel/explore/4-top-cultural-destinations-in-selangor

Kod permainan dan model procedural ditulis untuk projek ini. Kod/aset permainan rujukan tidak disalin. Three.js ialah perisian pihak ketiga berlesen MIT.

## Semakan
Lulus semakan sintaks dan simulasi aliran permainan: pembinaan empat lokasi, kedua-dua watak, butang mula, semua laluan ke petunjuk/NPC/portal, ganjaran unik, jawapan salah/betul, penamat 480 mata, reset dan jurnal.

Simulasi menggunakan renderer tiruan: ia menguji logik dan geometri, bukan GPU. Ujian visual WebGL dan sentuhan pada peranti sebenar belum disahkan. Laman tempatan tidak dapat dibuka oleh pelayar semakan; laman rujukan juga memaparkan kegagalan WebGL dalam pelayar itu.

## Kemas kini Unit 7
Skrin mula menggunakan Unit 7: Cinta Akan Negara — Pendidikan Moral Tahun 6. Tajuk cerita ialah Prolog. Pemain perlu berjalan keluar dari gua sebelum tiba di Lembah Bujang. Panel misi ringkas di kiri atas boleh dilipat; penerangan panjang ada dalam jurnal.
Semakan logik tambahan lulus untuk laluan keluar gua, pertukaran ke Jejak 1 dan fungsi lipat/buka panel. Paparan grafik sebenar belum disahkan.

## Dialog dan pakaian sekolah
Permulaan mempunyai perbualan dengan Penjaga Sejarah dan pilihan untuk keluar gua atau meneroka lagi. Watak pemain memakai pakaian sekolah; NPC mempunyai variasi pakaian dan topi. Setiap misi mempunyai dua soalan, dengan dialog Cuba semula untuk jawapan salah. Selepas portal terakhir, pemain berjalan menemui Hakim di sekolah dan berbual sebelum lencana dipaparkan. Papan Interpretif menggunakan butang E Baca Candi. Dialog menggunakan panel bawah yang seragam.

## Pengembaraan berdikari dan penceritaan
Bulatan objektif, bulatan kaki pemain dan jejak titik dibuang. Panel misi memaparkan jarak garis lurus ke objektif semasa dalam unit meter dunia permainan. Label tempat hanya muncul apabila berhampiran. NPC mempunyai latar, keperluan, maklum balas dan kaitan dengan misi seterusnya. Penamat mempunyai enam bahagian perbualan termasuk reaksi terkejut dan prihatin Hakim. Lapan soalan menggabungkan situasi, dialog dan sebab amalan; setiap soalan mempunyai satu jawapan terbaik serta petunjuk khusus selepas jawapan salah.

Muzik latar lo-fi ceria ialah gubahan procedural asal melalui Web Audio (86 BPM, kord lembut, bes, perkusi dan melodi). Bermula selepas butang Mula ditekan, diperlahankan semasa dialog, dimatikan apabila tab tersembunyi. Ikon muzik mengawal muzik dan bunyi ganjaran. Tiada audio luar, CDN atau muat turun tambahan. Semakan automatik meliputi penjadualan muzik, kawalan senyap dan kelantangan dialog. Kualiti audio secara pendengaran serta paparan GPU sebenar belum disahkan.

## Identiti, zum dan refleksi
Pemain memasukkan nama panggilan (maksimum 24 aksara) dan memilih Perempuan atau Lelaki. Penampilan pakaian sekolah asal dikekalkan. Butang +/− dan roda tetikus mengawal zum 70–180%; butang peratus menetapkan semula 100%. Dialog empat NPC menggunakan kamera dekat yang lembut serta gerak mulut dan tangan ringkas, tanpa suara latar dialog. Zum pilihan pemain dipulihkan selepas berbual. Penamat merangkum kesan bantuan kepada empat NPC, membolehkan pilihan tekad dan refleksi pilihan tanpa markah, kemudian memaparkan lencana peribadi. Nama dan refleksi tidak dihantar atau disimpan di pelayan.

Laman: https://emylianuraffifah.github.io/misi-pulang/

## Paparan tanpa skrol dan panduan buku teks
Gua mempunyai bahagian hadapan dan sisi kamera yang terbuka; batu melintang dan bumbung dibuang supaya Penjaga Sejarah jelas kelihatan. Semakan raycast mengesahkan muka dan badan tidak terlindung pada tiga sudut kamera. Dialog panjang dibahagikan kepada halaman dengan Kembali/Seterusnya; butang asal dan jawapan kekal berfungsi. Skrin mula dipadatkan dan menggunakan dua lajur pada skrin mendatar pendek. Penamat dipisahkan kepada pengajaran, pilihan tekad dan perasaan/sebab. Pilihan perasaan: bangga, cinta akan negara, bersyukur, terharu atau perasaan lain. Istilah permainan menggunakan tempat bersejarah dan Jejak Sejarah. Kandungan disesuaikan dengan aktiviti buku teks yang diberikan pengguna, bukan petikan jawapan buku teks.

## Dunia interaktif dan bunyi
Arjun menggantikan Amir. Penjaga Sejarah berada di hadapan pintu gua; bentuk gerbang batu dipulihkan dan batu hadapan menjadi lut sinar apabila pemain masih di dalam. E membolehkan pemain mengutip kertas, memasukkannya ke tong sampah, duduk/bangun dari bangku dan menaikkan Jalur Gemilang. Interaksi sampingan tidak memberi mata. Tepukan procedural dimainkan untuk jawapan betul; bunyi halaman, kutipan, tong sampah, portal, lompat dan jawapan salah ditambah. Ikon muzik turut mematikan kesan bunyi. Ikrar bersama merangkumi semua amalan, kemudian murid menyatakan perasaan dan sebab.

## Sekolah, haiwan dan refleksi pelbagai perasaan
Bumbung sekolah kini dua cerun rendah, dengan papan nama, pintu dan tingkap jelas. Arnab, burung, kucing, tupai dan anjing muncul mengikut lokasi; haiwan bergerak perlahan dan boleh didekati menggunakan E untuk mendapat respons. Kesan tepukan jawapan betul diperhalus menjadi beberapa tepukan lembut bersama nada kejayaan. Ikrar memberi pilihan bersedia atau mencuba sedikit demi sedikit, kemudian membolehkan murid memilih beberapa perasaan (bangga, gembira, sayang, sedih, kecewa) dan menyatakan sebabnya. Refleksi tidak dinilai sebagai betul atau salah.
