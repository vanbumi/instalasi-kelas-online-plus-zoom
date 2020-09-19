# Setup SSH for Git on Windows

SSH Key adalah metode alternatif untuk autentikasi dalam hal ini ke Github.com

Jika anda pengguna Windows gunakan cara ini untuk membuat SSH Key saat anda menggunakan Git.

Secara default, sistem akan menambahkan key pada folder: 

```
/Users/<username>/.ssh directory.
```



### Setup SSH Key

Gunakan Git Bash Window (Yang otomatis terinstal saat menginstal Git di Windows lihat cara instal Git: )

#### Langkah 1. Men-generate public/private rsa key pair. 

Tulis commandline seperti dibawah ini: 

	ssh-keygen -t rsa



#### Langkah 2. Tekan enter untuk menerima default file path pada:

	Contoh: /c/Users/<username>/.ssh/id_rsa.



#### Langkah 3. Enter dan enter saja. 

Pada pertanyaan "passphrase", untuk membuat default identitas dari public dan private keys.



#### Langkah 4. Menampilkan konten folder ".ssh" untuk melihat "key files" nya:

Lakukan perintah ini pada Terminal Gitbash Anda:

	dir .ssh

hasilnya yang muncul adalah: 

	id_rsa dan id_rsa.pub



#### Langkah 5. Menambahkan key ke **ssh-agent**.

Jika anda tidak ingin mengetikan password setiap saat anda akses ke Github.com, Anda bisa menggunakan key, cara nya sbb:

1. Start agent:

	Ketikan pada Terminal Gitbash Anda:
	
		eval $(ssh-agent)
	
	Output yang muncul, contoh: 
	
		agent pid 9700
	
2. Ketikan perintah **ssh-add** dan path ke **private key** anda:

		```
		ssh-add ~/.ssh/id_rsa
	```
	



### Langkah 6. Menambahkan public key ke github anda

1. Buka public key file pada laptop/pc anda yang sudah tersimpan di  ~/.ssh/id_rsa.pub atau dengan perintah:

		```
		cat ~/.ssh/id_rsa.pub
	```

2. Copy semua teks yang ditampilkan, contoh 

   ```
   ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDgzlas;dkjfaslkjfaslkjdfa;sldk jfasdj as;ldjfa;sldkjfa sd;lkjasd;flkjasd;f a;skjasfkasdkjfgaks aksdghfakjsdghfakshgdfkasfasd fkajsghdfkajsghdfka sdfkahgsdfkj asdkfjagsdkf akjsdghfakkasdghfakskasdfhgakjhs dyo-medio@dyo-mac.local
   ```

3. Buka browser Anda dan buka github.com anda: 
   1. Login dengan username dan password Anda. 
   2. Klik Settings 
   3. Pilih SSH and GPG Keys 
   4. Buat key baru klik New SSH Key dan 
   5. Paste kan key tadi ke dalam kotak 
   6. Klik add SSH Key button, selesai.



### Langkah 7. Lakukan Testing apakah semua langkah diatas sudah berhasil.

Ketik perintah dibawah ini untuk menguji koneksi SSH ke Github:

	ssh -T git@github.com

HOREE..... Anda sudah berhasil **setup SSH KEY di laptop/pc** Anda, Jika berhasil pesannya yang muncul kurang lebih seperti dibawah ini:

	Hi, You've successfully authenticated, but Github does not provide shell acess.



**SELESAI**


