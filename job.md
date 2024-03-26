JOB CONTROL
SISTEM OPERASI

WIDYA ANGGRAINI(09030582226025)
<img width="363" alt="image" src="https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/30e95a74-30fd-4478-a4ee-08ec064a74ba">

Tugas 
1. Eksekusi seluruh profile yang ada :  
a.  Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :  
echo “Profile dari /etc/profile”
 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/b9a836f3-3244-4cc9-baed-5a380d5d889b)
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/e6c36123-c496-43da-9060-94a0fcd7635e)

b.  Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  
echo “Profile dari .bash_profile”  
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/8525ffa9-d283-4458-b9ca-3aae10f20c45)
/home/stD02001/.bash_profile  
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/94b26367-9d0e-4cea-85bd-3f9da68a5aa8)
/home/. stD02001/.bash_login  
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/60577bc2-4484-449b-868f-f23fc6c0117d)
/home/mahasiswa/.profile  
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/0f5fdd72-5066-4127-a42a-7d99aafbe34f)
/home/mahasiswa/.bashrc  
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/747cc105-f8f9-4caa-8e1e-bad97d0c0238)

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: Merubah file-file menjadi file executeable
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/86fc538e-c3be-449b-bedb-13620bce5bfc)

$ su mahasiswa  
$ exit  
kemudian gunakan opsi – sebagai berikut :  
$ su – mahasiswa  
$ exit  
Jelaskan perbedaan kedua utilitas tersebut.:
Perbedaan kedua utilitas tersebut yaitu menampilkan isi dari file-file yang dibuat pada direktori yang berbeda. Untuk direktori yang memiliki banyak file, hanya akan ditampilkan satu buah filenya saja.
su: Beralih ke akun superuser atau root tanpa mengubah lingkungan.
su -: Beralih ke akun superuser atau root dengan mengatur ulang lingkungan menjadi lingkungan superuser secara lengkap.
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/a63ef077-ced0-406d-b9d3-ea57faa96fea)
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/c86eb3dc-dc50-4655-b77f-4c6214c37ff7)

2.Prompt String (PS)
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’.
Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell $ PS1=“\! > “   81 > PS1=”\d > “ Sen Mar 25 > PS1=”\t > “ 11:38:14 > PS1=”Saya=\u > “ Saya=mahasiswa > PS1=”\w >”   ~ > PS1=\h >”
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/534f2f5c-b42d-4053-984f-4e19ef1ea0b6)
syntax diatas berfungsi untuk menampilkan informasi sesuai dengan option perintah seperti d adalah data (tanggal), t adalah time (waktu), u adalah user (pengguna).

3. Logout  
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  
Echo “Terima kasih atas sesi yang diberikan”  
Sleep 5  
clear
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/5ebb61a8-7319-445f-b4bb-01e874dbf61f)

4. Bash script
 a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
 p1.sh #! /bin/bash echo “Program p1” ls –l 
 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/7eb74e70-fdfd-4e38-a3af-70d5ebf2d70f)

p2.sh #! /bin/bash echo “Program p2” who
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/b4068649-71ae-47e5-ad76-b43e269ec13f)
 
 p3.sh #! /bin/bash echo “Program p3” ps x 
 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/09612839-bece-4c14-8060-987df3b4048f)

 
b. Jalankan script tersebut sebagai berikut : 
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/9cec1afa-b108-4ff1-a4ac-bf499861f297)

$ ./p1.sh ; ./p3.sh ; ./p2.sh  
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/c28c81d6-4039-467a-81f6-935dff8080ca)

$ ./p1.sh & $ ./p2.sh & ./p3.sh & 
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/5adc6e44-a75f-4cb6-9af1-5cb0e7af7bd5)

$ ( ./p1.sh ; ./p3.sh ) &
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/d2576353-f790-4268-98ba-ba1b2ad4e0ab)

 5.Jobs a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.
 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/3b1c24ea-2732-481f-9515-ec34b088e5ba)

b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :

 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/d82c5c13-551d-4f23-94a0-21940c05d61f)

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/e15bf24b-05af-48e8-80cf-53b08a556922)

d. Stop program background dengan utilitas kil
 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/97ff3e87-b768-4397-a837-b36d37c57251)


$ kill [Nomor PID]
History
a. Ganti nilai HISTSIZE dari 1000 menjadi 20
 ![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/84ec362d-eb73-4740-958b-6645dccbdf93)

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/c33a6dac-1d02-4b25-962e-bd1f9e786040)

c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer 
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/bc39fabc-20fc-4631-b0bf-56a7c7ba8a36)

d. Ulangi instruksi pada history bufer nomor 150
e. Ulangi instruksi dengan prefix “ls”
![image](https://github.com/Widyaanggra/JOB-CONTROL/assets/126336053/6dfd8b34-65a8-407d-88f0-8206f37bc7d1)

 

Kesimpulan alternatif dari eksperimen ini adalah bahwa keberhasilan dalam menjalankan percobaan terkait dengan profile, history, dan kontrol pekerjaan sangat tergantung pada tingkat ketelitian yang diterapkan. Kesalahan kecil, bahkan seperti kesalahan dalam formatasi spasi, dapat menghasilkan hasil yang sangat berbeda, bahkan menyebabkan akses ke direktori yang tidak diinginkan. Selain itu, langkah penting setelah menyelesaikan pengembangan program adalah memastikan bahwa file dieksekusi dengan benar untuk memperoleh izin yang diperlukan agar program dapat berjalan dengan lancar.
