# Cara menginstal Wireshark di Ubuntu 20.04
### Instal Wireshark di Ubuntu 20.04

<p>[STEP-1] Pertama-tama, Buka terminal dengan mencarinya secara manual di aktivitas, atau Anda juga dapat menekan 'CTRL+ALT+T' untuk melihat jendela terminal.</p><hr>
<p>[STEP-2] Sekarang perbarui daftar paket.</p>
<p>$ sudo apt-get update -y</p>
<p>Masukkan kata sandi Anda untuk mengizinkan pembaruan paket.</p><hr>
<p>[STEP-4] Gunakan repositori untuk menginstal Wireshark.</p>
<p>$ apt-get install wireshark</p><hr>
<h3>Mengkonfigurasi Wireshark di Ubuntu 20.04</h3>
<p>[STEP-1] Pilih opsi 'yes' untuk mengizinkan non-pengguna super menangkap paket.</p><hr>
<p>[STEP-2] Verifikasi keberadaan Wireshark dengan menggunakan perintah yang diberikan di bawah ini.</p>
<p>$ wireshark --version</p><hr>
<p>[STEP-3] Sekarang Anda harus menambahkan pengguna ke grup Wireshark untuk menangkap paket seperti yang dilakukan pengguna biasa.</p>
<p>$ sudo usermod -a -G wireshark $USER</p><hr>
<p>[STEP-4] Sekarang, kita akan mengubah izin file 'dumcap'.</p>
<p>$ sudo chgrp wireshark /usr/bin/dumpcap</p>
<p>$ sudo chmod 750 /usr/bin/dumpcap</p>
<p>$ sudo setcap cap_net_raw,cap_net_admin=eip /usr/bin/dumpcap</p>
<p>$ sudo getcap /usr/bin/dumpcap</p>
<p>$ sudo wireshark</p><hr>
<p>Anda juga dapat membuka Wireshark dengan mencarinya secara manual di bilah pencarian 'Aktivitas'.</p><hr>
<br>
<br>
<p>SEMOGA BERMANFAAT</p>







