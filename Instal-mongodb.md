## Cara Install MongoDB di Local Laptop/PC Anda

Install Mongodb di local anda adalah pililhan dan **TIDAK HARUS anda lakukan**, karena pada kelas ini kita menggunakan mongodb database remote server/cloud, tidak di local pc/laptop.



**Lakukan dengan Cermat dan Teliti Langkah-langkah Instalasi**



1. **Instal Mongodb untuk Windows**, download file installer disini https://www.mongodb.com/download-center/community, setelah download selesai doble click untuk proses instalasi hingga selesai. Note: "Jangan gunakan mongodb cloud!" dan install mongodb dulu, **mongodb compass** belakangan saja.

   * Pengguna windows 7 system 32 gunakan file installer khusus bisa download disini [https://www.mongodb.org/dl/win32/i386](https://www.mongodb.org/dl/win32/i386).

   * Pengguna windows 10 dan system 64 tidak akan ada masalah. 

2. Pada pilihan Choose Setup Type > pilih Complete.

   * Biasanya nanti aplikasi akan tersimpan di folder C:\Program Files\MongodDB\

   * Kemungkinan bisa berbeda pada versi windows lain. 

   * Silahkan cari folder bin berada pada file mongodb yang sudah tersimpan, kemudian copy path nya ya! Karena kita akan memasukannya ke dalam Path pada Environment Variable (Windows User).

3. Selanjutnya setting Environment supaya aplikasi mongoDB terbaca oleh command prompt :
   * Pada Windows 10 buka Start > Search > Ketik "env" > Pilih "Edit the system environement variables".
   * Klik button "Environment Variables".
   * Pada section "System Variables" > Pilih Path > Klik Edit > Ketikan Path letak folder "bin" berada pada folder mongodb di komputer anda, contoh " ..mongodb\..\..\bin

4. Lakukan Testing dengan Menjalankan Server Mongodb

   * Buka Terminal Command (gunakan **Gitbash** bagi pengguna Windows dengan administrator priviledge).

   * Kemudian ketikan ```mongod```

   * Apabila tidak ada error buka tab Terminal baru dan ketikan ```mongo``` untuk membuka mongodb console.

5. Bila ada error seperti ini: 

		```
	Data directory C:\data\db\ not found
	```
	
6. Solusi nya adalah  buat folder baru di folder C :

   ```
   	C:\data\db
   ```



SELESAI