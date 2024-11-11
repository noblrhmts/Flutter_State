**Nama: Nobel Rahmat Sani**
**Kelas: 2A TRPL**
**NIM: 362358302075**

Praktikum 1
1. ![1](https://github.com/user-attachments/assets/589775b4-f5a3-41b9-89f7-60efe592fe21)
2. Langkah 4 ini bertujuan untuk menyederhanakan proses impor file model pada proyek Flutter. Dengan membuat file data_layer.dart yang berisi beberapa export, kita dapat mengelompokkan dan mengimpor beberapa model (dalam hal ini, plan.dart dan task.dart) melalui satu file saja.
3. - Mengapa Perlu Variabel plan?
     plan adalah variabel yang merepresentasikan satu objek Plan yang berisi detail rencana (misalnya, daftar tugas yang ingin dibuat atau diselesaikan oleh pengguna). Plan akan memuat daftar tasks, dan setiap kali pengguna menambah atau memperbarui tugas, widget ini bisa langsung mengakses dan mengelola plan untuk mencerminkan perubahan tersebut di UI (User Interface).
   - Mengapa Dibuat Konstanta?
     Menggunakan const pada inisialisasi awal membantu Dart mengoptimalkan penggunaan memori, karena objek kosong ini hanya dibuat sekali dan tidak berubah. Kemudian, ketika plan diperbarui dengan tugas, variabel ini tidak lagi berupa konstanta, dan setState() akan mengubahnya menjadi objek Plan baru yang memuat daftar tugas.
4. ![image](https://github.com/user-attachments/assets/d19a9b0d-e7e9-4b23-811f-89c7fa714afb)
5. - Langkah 11
     initState() adalah metode pertama yang dipanggil saat widget diinisialisasi, sebelum widget ditampilkan di layar. Metode ini biasanya digunakan untuk konfigurasi awal atau pengaturan yang hanya perlu dilakukan sekali, seperti inisialisasi variabel, mendeklarasikan controller, atau menambahkan listener.
   - Langkah 13
     dispose() adalah metode terakhir yang dipanggil dalam siklus hidup widget. Metode ini digunakan untuk membersihkan resource atau melepaskan objek yang tidak lagi diperlukan setelah widget dihapus dari tree (misalnya, ketika pengguna keluar dari halaman atau widget di-destroy).

Praktikum 2
1. ![image](https://github.com/user-attachments/assets/0be97b37-6cd4-45b0-9a4b-903342955e3e)
2. InheritedNotifier digunakan di sini untuk mempermudah pembaruan otomatis pada UI saat Plan diperbarui, memberikan efisiensi dan kemudahan dalam penggunaan data yang berubah-ubah. Ketika ada perubahan dalam ValueNotifier<Plan>, maka setiap widget yang tergantung pada PlanProvider (yang mengambil data Plan dari ValueNotifier<Plan>) akan dibangun ulang secara otomatis.
3. - Getter completedCount
     Berfungsi untuk menghitung jumlah tugas yang telah selesai (bernilai complete == true). Digunakan untuk memudahkan akses jumlah tugas selesai secara langsung, mengurangi pengulangan perhitungan di berbagai tempat dalam aplikasi.
   - Getter completenessMessage
     Berfungsi untuk menghasilkan pesan progres seperti "3 out of 5 tasks." Digunakan untuk memudahkan UI menampilkan progres tugas secara informatif, meningkatkan pengalaman pengguna.

Praktikum 3
1. Diagram tersebut menunjukkan bahwa ketika pengguna berpindah dari PlanCreatorScreen ke PlanScreen, tampilan dan struktur widget berubah. Navigator.push memicu perpindahan layar dan memberikan akses ke layar dengan informasi baru, memungkinkan penggunaan PlanScreen sebagai tempat menampilkan progres tugas atau rencana yang telah dibuat di PlanCreatorScreen.
2. ![3](https://github.com/user-attachments/assets/5db28c9b-2fdc-48ed-8e1d-748311f10a00)

