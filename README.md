# MINPRO 3 PBO – SISTEM MANAJEMEN KLINIK HEWAN

## 1. Deskripsi Program

Sistem Manajemen Klinik Hewan merupakan program berbasis Java yang digunakan untuk mengelola data hewan pada sebuah klinik hewan.

Program dapat digunakan untuk menambahkan, menampilkan, mencari, mengubah, dan menghapus data hewan. Data yang disimpan meliputi data hewan, pemilik, pemeriksaan, serta informasi vaksin untuk hewan tertentu.

## 2. Struktur Package

Program menggunakan beberapa package untuk mengatur class berdasarkan fungsinya.

<img width="295" height="336" alt="image" src="https://github.com/user-attachments/assets/679c369f-6726-4896-8680-c2d54fb8300c" />

## 3. Alur Program

### 3.1 Menu Utama

<img width="303" height="229" alt="image" src="https://github.com/user-attachments/assets/7d13e7e4-fe88-4fd2-be8d-904d28553637" />

Saat program dijalankan, pengguna akan melihat menu utama yang terdiri dari:

1. Tambah Data Hewan
2. Tampilkan Data Hewan
3. Cari Data Hewan
4. Update Data Hewan
5. Hapus Data Hewan
6. Keluar

Pengguna dapat memilih menu sesuai dengan kebutuhan.

### 3.2 Tambah Data

<img width="303" height="644" alt="image" src="https://github.com/user-attachments/assets/09f5a410-4c7e-4521-ad3c-944c6244ee08" />

Pada menu tambah data, pengguna memasukkan:

- ID data
- Nama hewan
- Jenis hewan
- Umur
- Nama pemilik
- Nomor telepon
- Keluhan
- Hasil pemeriksaan

Untuk **Kucing**, program meminta status vaksin F3.

Untuk **Anjing**, program meminta status vaksin Rabies.

Untuk **Hewan Lain**, tidak terdapat input vaksin.

### 3.3 Tampilkan Data Hewan

Menu ini digunakan untuk menampilkan seluruh data hewan yang telah tersimpan.

<img width="290" height="841" alt="image" src="https://github.com/user-attachments/assets/db32e5e2-fbcc-4159-92f6-90f795de602e" />

### 3.4 Cari Data Hewan

Menu ini digunakan untuk mencari data berdasarkan:

- ID hewan
- Nama hewan

<img width="286" height="363" alt="image" src="https://github.com/user-attachments/assets/291e755d-29da-4de9-88d5-591ef753694a" />

### 3.5 Update Data Hewan

Menu update digunakan untuk mengubah data hewan yang sudah tersimpan.

<img width="287" height="445" alt="image" src="https://github.com/user-attachments/assets/91e92c21-5dc6-4066-b7fc-8483c5ad2921" />

Pengguna memilih data berdasarkan ID kemudian memasukkan data baru yang ingin diperbarui.

### 3.6 Hapus Data Hewan

Menu hapus digunakan untuk menghapus data hewan berdasarkan ID.

Jika ID ditemukan, data akan dihapus dari `ArrayList`.

<img width="288" height="291" alt="image" src="https://github.com/user-attachments/assets/b0d26e4c-9fac-4f80-a352-6d7ddf945c03" />

### 3.7 Keluar

Menu keluar digunakan untuk menghentikan program.

<img width="290" height="302" alt="image" src="https://github.com/user-attachments/assets/ae4c616c-6fa2-4c5e-968b-c674ba05d756" />

## 4. Konsep PBO yang Diterapkan

### 4.1 Encapsulation

Encapsulation diterapkan dengan menggunakan access modifier `private` pada atribut class.

Akses terhadap atribut dilakukan menggunakan method `getter` dan `setter`.

Contohnya terdapat pada class:

- `Hewan`
- `Pemilik`
- `Pemeriksaan`
- `Kucing`
- `Anjing`

Dengan encapsulation, data pada class tidak dapat diakses secara langsung dari luar class.

### 4.2 Inheritance

Inheritance diterapkan dengan menggunakan hubungan antara superclass dan subclass.

Class `Hewan` menjadi superclass, sedangkan:

- `Kucing` menjadi subclass dari `Hewan`
- `Anjing` menjadi subclass dari `Hewan`
- `HewanLain` menjadi subclass dari `Hewan`

Contohnya:

<img width="291" height="31" alt="image" src="https://github.com/user-attachments/assets/cfeee7b3-f2a6-42e6-adca-b9c08bb049b5" />

Dengan inheritance, subclass dapat menggunakan atribut dan method yang dimiliki oleh superclass.

### 4.3 Polymorphism

Polymorphism diterapkan dalam bentuk method overriding dan method overloading.

#### 4.3.1 Method Overriding

Method overriding diterapkan pada method:

<img width="290" height="51" alt="image" src="https://github.com/user-attachments/assets/00f24d54-6cc7-4dcf-88b8-11d6d3206600" />

Method tampilkanInfo() dideklarasikan sebagai abstract method pada class Hewan, kemudian diimplementasikan kembali oleh subclass Kucing, Anjing, dan HewanLain.

Contohnya:

<img width="711" height="115" alt="image" src="https://github.com/user-attachments/assets/03e4b691-c318-4b6a-b825-5f7545bd8d22" />

Setiap subclass dapat menampilkan informasi sesuai dengan jenis hewannya.

#### 4.3.2 Method Overloading

Pada class Service terdapat dua method cariHewan() dengan parameter yang berbeda.

<img width="293" height="36" alt="image" src="https://github.com/user-attachments/assets/a84c1934-937c-4591-9f7e-63ea974ff5e1" />

dan

<img width="350" height="24" alt="image" src="https://github.com/user-attachments/assets/97d60d49-8f4a-458c-8b43-30e9662eba90" />

Kedua method memiliki nama yang sama, tetapi parameter yang digunakan berbeda.

### 4.4 Abstraction
#### a. Abstract Class
Abstraction diterapkan dengan menjadikan class `Hewan` sebagai abstract class.

<img width="294" height="26" alt="image" src="https://github.com/user-attachments/assets/fd327351-7d0a-4d7f-b585-e73883712487" />

Karena `Hewan` merupakan abstract class, class tersebut tidak dapat dibuat menjadi objek secara langsung.
Objek dibuat melalui subclass seperti:
- `Kucing`
- `Anjing`
- `HewanLain`

#### b. Abstract Method

Pada class Hewan terdapat abstract method:

<img width="297" height="28" alt="image" src="https://github.com/user-attachments/assets/f15c047c-cea1-4430-8391-67cd5f95ea8d" />

Method tersebut tidak memiliki isi pada class `Hewan`.
Setiap subclass wajib memberikan implementasi method tampilkanInfo() sesuai dengan kebutuhan masing-masing.


## 5. Penerapan MVC

Program menggunakan struktur Model-View-Controller (MVC) untuk memisahkan bagian data, tampilan, dan proses program.

### 5.1 Model

Bagian Model digunakan untuk menyimpan data dan struktur objek.

<img width="225" height="207" alt="image" src="https://github.com/user-attachments/assets/0e39b3ad-6bb4-4976-8836-1903663d7655" />

Class yang termasuk Model:
- Hewan
- Kucing
- Anjing
- HewanLain
- Pemilik
- Pemeriksaan
- Vaksinable

### 5.2 View

Bagian View digunakan untuk menampilkan informasi kepada pengguna.

<img width="222" height="63" alt="image" src="https://github.com/user-attachments/assets/cd6abcae-36d7-4aaa-9108-e14e44def9db" />

Class yang digunakan:
- KlinikView
KlinikView digunakan untuk menampilkan detail data hewan.

### 5.3 Controller

Bagian Controller digunakan untuk mengatur proses pengolahan data.

<img width="225" height="70" alt="image" src="https://github.com/user-attachments/assets/814ba973-19be-4fba-afc7-c8cfd524e9f9" />

Class yang digunakan:
- Service
Service menangani proses tambah, tampil, cari, update, dan hapus data.

### 5.4 Main

Class Main digunakan sebagai titik awal program.

<img width="227" height="80" alt="image" src="https://github.com/user-attachments/assets/2d4f20ed-9515-4ed2-8a6e-dddd3b5972f1" />

## 6. Value Added

### 6.1 Interface Vaksinable

Interface tersebut memiliki method:

<img width="223" height="32" alt="image" src="https://github.com/user-attachments/assets/bae118eb-5ca9-4a6c-ad9b-505a5e835501" />

Interface Vaksinable diimplementasikan oleh:
- Kucing
- Anjing

Hal ini digunakan karena kedua jenis hewan tersebut memiliki informasi vaksin yang berbeda.
Kucing menggunakan vaksin F3, sedangkan Anjing menggunakan vaksin Rabies.


## 7. Validasi dan Data Awal

### 7.1 Validasi Input

Program memiliki beberapa validasi input untuk membantu memastikan data yang dimasukkan sesuai dengan kebutuhan program.
Validasi yang diterapkan antara lain:
- Input angka harus berupa angka.

  <img width="220" height="46" alt="image" src="https://github.com/user-attachments/assets/e39d9273-e562-473c-97c4-bc16c8562444" />

- ID dan umur tidak boleh bernilai negatif.

  <img width="214" height="38" alt="image" src="https://github.com/user-attachments/assets/89bd9ea0-2e19-4139-8b17-612980240e25" />

- Input teks tidak boleh kosong.

  <img width="209" height="53" alt="image" src="https://github.com/user-attachments/assets/9322f9c7-64e0-4cf0-83fc-6466f16e446b" />

- Nomor telepon harus berupa angka.

  <img width="215" height="33" alt="image" src="https://github.com/user-attachments/assets/ebb5e967-9708-4223-97f0-cd5b21c10194" />

- Nomor telepon memiliki panjang 10–13 digit.

  <img width="215" height="68" alt="image" src="https://github.com/user-attachments/assets/0c19574c-b96c-4350-aafa-fca5f2f05e79" />

- ID hewan tidak boleh sama dengan ID yang sudah tersimpan.

  <img width="268" height="53" alt="image" src="https://github.com/user-attachments/assets/fb775cc4-ce4f-49b0-b78f-55947e8b0b34" />


### 7.2 Dummy Data

Program menyediakan data awal atau dummy data yang dimasukkan ke dalam ArrayList.

<img width="488" height="94" alt="image" src="https://github.com/user-attachments/assets/aeac6ce1-b8f4-476f-89ec-9a52a0004288" />
