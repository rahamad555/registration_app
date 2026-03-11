# Aplikasi Registrasi Event Flutter
Deskripsi
Aplikasi ini merupakan aplikasi registrasi event sederhana yang dibuat menggunakan Flutter.
Aplikasi ini memungkinkan pengguna untuk melakukan pendaftaran peserta event, melihat daftar peserta, serta melihat detail data peserta yang telah didaftarkan.

Aplikasi ini menggunakan Provider sebagai state management untuk mengelola data peserta.

# Fitur Aplikasi
Form registrasi peserta

Validasi input form

Input nama, email, password, jenis kelamin, program studi, dan tanggal lahir
Menyimpan data peserta sementara menggunakan Provider

Menampilkan daftar peserta

Menampilkan detail peserta

Menghapus peserta dari daftar

Badge jumlah peserta pada halaman utama

# Teknologi yang Digunakan
Flutter

Dart

Provider (State Management)


# Struktur Folder Project






<img width="654" height="415" alt="image" src="https://github.com/user-attachments/assets/d82afc42-f7a9-4c3f-b960-836b10804353" />







# Penjelasan Kode



# 1. main.dart
File ini merupakan file utama yang digunakan untuk menjalankan aplikasi Flutter.

Pada file ini digunakan ChangeNotifierProvider agar data dari RegistrationProvider dapat diakses oleh seluruh halaman aplikasi.

Contoh kode:





<img width="423" height="211" alt="image" src="https://github.com/user-attachments/assets/ad0fe4c0-19fa-4d41-b325-e24a990f39ea" />



Kode di atas berfungsi untuk menjalankan aplikasi Flutter dan menghubungkan RegistrationProvider sebagai state management.







# 2. registrant_model.dart


File ini berisi class Registrant yang digunakan sebagai model data peserta.

Contoh kode:







<img width="453" height="482" alt="image" src="https://github.com/user-attachments/assets/a0744c85-953a-4e9c-b9f7-32c74a8662f4" />






Class ini menyimpan seluruh informasi peserta yang melakukan registrasi.

Selain itu terdapat fungsi helper untuk menghitung umur peserta.

Contoh:







<img width="439" height="240" alt="image" src="https://github.com/user-attachments/assets/c232b4ca-3ae6-452b-93dc-5cfd7f7d2824" />






3. registration_provider.dart



File ini berfungsi sebagai state management menggunakan ChangeNotifier.

Provider ini menyimpan semua data peserta dalam bentuk list.

Contoh kode:







<img width="449" height="89" alt="image" src="https://github.com/user-attachments/assets/80ffdbfb-3d3e-4162-ae8f-6cfb51291ee3" />






Menambahkan peserta baru:






<img width="444" height="132" alt="image" src="https://github.com/user-attachments/assets/9ea18516-e864-4026-80f7-20cf449d6654" />




Kode notifyListeners() digunakan untuk memberi tahu UI bahwa data telah berubah sehingga tampilan akan diperbarui.





Menghapus peserta:




<img width="446" height="113" alt="image" src="https://github.com/user-attachments/assets/e753fa03-7de9-4ee9-887c-45b535d77429" />






# 4. registration_page.dart



Halaman ini merupakan form registrasi peserta.

Pada halaman ini pengguna mengisi data seperti:

nama

email

password

jenis kelamin

program studi

tanggal lahir




Contoh input field:








<img width="438" height="216" alt="image" src="https://github.com/user-attachments/assets/bd3d83da-d2c0-4f20-b620-66d5bc82aa90" />




Kode ini digunakan untuk membuat input field nama peserta.





Contoh validasi email:







<img width="434" height="314" alt="image" src="https://github.com/user-attachments/assets/afebb15a-b934-45af-ab46-c0d6ff07d3de" />






Kode ini digunakan untuk memvalidasi format email.






# 5. registrant_list_page.dart


Halaman ini menampilkan daftar peserta yang sudah melakukan registrasi.

Contoh kode:







<img width="451" height="324" alt="image" src="https://github.com/user-attachments/assets/0b4471cd-774d-4e69-8a65-61b9daff1db5" />





Kode ini digunakan untuk menampilkan data peserta dalam bentuk list.





# 6. registrant_detail_page.dart

Halaman ini digunakan untuk menampilkan detail informasi peserta.

Contoh kode:


_buildInfoCard(Icons.email, 'Email', registrant.email)



Widget ini digunakan untuk menampilkan informasi detail seperti email, gender, program studi, dan tanggal lahir peserta.




# Screenshot Aplikasi


# Halaman Form Registrasi






<img width="1293" height="993" alt="image" src="https://github.com/user-attachments/assets/c822b6a2-3622-4b2b-9138-9e492386ad76" />











Halaman ini merupakan halaman utama aplikasi yang berisi form pendaftaran peserta event. Pengguna diminta mengisi data seperti nama lengkap, email, password, jenis kelamin, program studi, dan tanggal lahir. Setelah semua data diisi, pengguna dapat menekan tombol Daftar Sekarang untuk melakukan registrasi atau Reset Form untuk menghapus semua input.




# Halaman ketika peserta berhasil mendaftar








<img width="1289" height="1004" alt="image" src="https://github.com/user-attachments/assets/aa4cc279-9823-4bbf-b199-469507c27df2" />






Gambar ini menunjukkan dialog notifikasi bahwa proses registrasi berhasil dilakukan setelah pengguna mengisi form dengan benar. Terdapat dua pilihan yaitu Daftar Lagi untuk kembali ke form pendaftaran dan Lihat Daftar untuk melihat daftar peserta yang sudah terdaftar.






# Halaman ketika email sudah pernah terdaftar






<img width="1295" height="1002" alt="image" src="https://github.com/user-attachments/assets/a1977b0f-151f-44fe-bebc-c05f3b3b290b" />






Gambar ini menunjukkan pesan peringatan ketika pengguna mencoba mendaftarkan email yang sudah pernah digunakan sebelumnya. Aplikasi menampilkan notifikasi bahwa email tersebut sudah terdaftar sehingga data peserta tidak dapat didaftarkan kembali.







# Halaman Detail peserta








<img width="1285" height="990" alt="image" src="https://github.com/user-attachments/assets/5cf51fc6-9696-41a9-bfcc-6a776961cb08" />








Halaman ini menampilkan informasi lengkap mengenai peserta yang dipilih dari daftar peserta, seperti nama, email, jenis kelamin, program studi, tanggal lahir, dan umur peserta.







# Halaman ketika ingin menghapus data






<img width="1298" height="995" alt="image" src="https://github.com/user-attachments/assets/3029dc2c-cbc8-4497-8a84-ff94445161df" />






Halaman ini menampilkan semua peserta yang telah didaftarkan. Setiap peserta ditampilkan dalam bentuk daftar yang berisi nama, program studi, dan email, serta terdapat tombol hapus untuk menghapus data peserta dari daftar.





# Kesimpulan

Aplikasi registrasi event ini berhasil dibuat menggunakan Flutter dengan menggunakan Provider sebagai state management.

Aplikasi ini dapat melakukan pendaftaran peserta, menampilkan daftar peserta, serta menampilkan detail peserta dengan tampilan yang sederhana dan mudah digunakan.




