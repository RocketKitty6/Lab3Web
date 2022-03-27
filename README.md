# LANGKAH - LANGKAH PRAKTIKUM 3
# A. Membuat LIST di HTML
### 1. Ordered List
Yang pertama kita harus lakukan adalah membuat file html dengan nama **lab3_list.html**.
Setelah itu masukan code seperti dibawah ini :
```
    <section id="order-list">
      <h2>Ordered List</h2>
      <ol>
        <li>Pemrograman Web</li>
        <li>Sistem Informasi</li>
        <li>Basis Data 2</li>
      </ol>
    </section>
```
![image](https://user-images.githubusercontent.com/101440705/160271676-28e80f8b-0cb9-4fe8-bd03-1625b7ee8068.png)

### 2. Unordered List
setelah membuat ordered list seperti di atas, kita lanjutkan dengan membuat Unordered list. tampilan code seperti dibawah ini :
```
    <section id="unorder-list">
      <h2>Unordered List</h2>
      <ul type="square">
        <li>Jaringan Komputer</li>
        <li>Struktur Data</li>
        <li>Algoritma &amp; Pemrograman</li>
      </ul>
    </section>

```
![image](https://user-images.githubusercontent.com/101440705/160271761-3a26efb6-0fa1-4314-9ef4-288ccb02bb94.png)

### 3. Description List
Kemudian tambahkan kode untuk membuat description list setelah deklarasi unorderd-list.
Cara membuat **Description List**, ikuti saja kode dibawah ini :
```
    <section id="description-list">
      <h2>Description List</h2>
      <dl>
        <dt>Fakultas Teknik</dt>
        <dd>Teknik Industri</dd>
        <dd>Teknik Informatika</dd>
        <dd>Teknik Lingkungan</dd>
        <dt>Fakultas Ekonomi dan Bisnis</dt>
        <dd>Akuntansi</dd>
        <dd>Manajemen</dd>
        <dd>Bisnis Digital</dd>
      </dl>
    </section>
```
![image](https://user-images.githubusercontent.com/101440705/160271884-3d94401d-d35e-4e8e-86b6-1692580f0cd2.png)
===========================================================================

# B. Membuat Tabel dan menggabungkan Sel data di HTML
Berikut adalah cara membuat Tabel.
### 1. Pertama adalah cara memmbuat tabel di HTML
ada beberapa element yang digunakan khusus untuk membuat tabel, contohnya :
- element `<table></table>` yang berguna unutk mendefinisikan sebuah tabel dalam dokumen HTML.
- element `<th></th>` yang berguna membuat judul pada kolom atas
- element `<tr></tr>` untuk mendefinisikan baris dalam tabel
- element `<td></td>` untuk mendefinisikan kolom tabel

berikut adalah hasil dari membuat tabel beserta code nya :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>HTML Lanjutan</title>
</head>
<body>
    <!-- Membuat table -->
    <h1>Membuat Tabel</h1>
    <table border="1" cellpadding="4" cellspacing="0">
      <!-- table header -->
      <thead>
        <tr>
          <th>No.</th>
          <th>Fakultas</th>
          <th>Program Studi</th>
        </tr>
      </thead>
      <!-- table body -->
      <tbody>
        <tr>
          <td>1.</td>
          <td>Teknik</td>
          <td>Teknik Informatika</td>
        </tr>
        <tr>
          <td>2.</td>
          <td>Teknik</td>
          <td>Teknik Industri</td>
        </tr>
        <tr>
          <td>3.</td>
          <td>Teknik</td>
          <td>Teknik Lingkungan</td>
        </tr>
      </tbody>
    </table>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/101440705/160272642-46245936-362f-4cc1-aedb-49e53213ee65.png)

### 2. menggabungkan Cell data.
ada dua atribut dalam element `<table>` yaitu : 
- `colspan` berguna untuk menggabungkan beberapa cell dalam satu baris
- `rowspan` berguna untuk menggabungkan beberapa cell dalam satu kolom

Cara menggunakannya yaitu `<td rowspan="3">Teknik</td>`

dan dibawah ini adalah code untuk penggabungan Cell Data : 
```
<table border="1" cellpadding="6" cellspacing="0">
        <thead>
          <tr>
            <th>No.</th>
            <th>Fakultas</th>
            <th>Program Studi</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1.</td>
            <td rowspan="3">Teknik</td>
            <td>Teknik Informatika</td>
          </tr>
          <tr>
            <td>2.</td>
            <td>Teknik Industri</td>
          </tr>
          <tr>
            <td>3.</td>
            <td>Teknik Lingkungan</td>
          </tr>
        </tbody>
      </table>
```
![image](https://user-images.githubusercontent.com/101440705/160273010-fa685e94-ffff-4530-a883-c79a4a41057e.png)
===========================================================================

# C. Membuat Form 
cara membuat Form harus menggunakan tag `<form></form>`, karena tag ini akan membungkus element input yang ada dialamanya dan juga berfungsi mengirim data ke server.
contoh element yang berada di dalam tag tersebut adalah :
- `<textfield>`
- `<password>`
- `<checkbox>`
- `<Radio>`
- `dll`

Dibawah ini adalah code pembuatan Form sesuai praktikum 3 : 
```
<!DOCTYPE html> 
<html lang="en"> 
    <head> 
        <meta charset="UTF-8"> 
        <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
        <title>HTML Lanjutan</title> 
    </head> 
    <body> 
        <header> 
            <h1>Membuat Form</h1> 
        </header>
        <form action="proses.php" method="post"> 
            <fieldset> 
                <legend>Data Pelanggan</legend> 
                <p> 
                    <label for="nama">Nama</label> 
                    <input type="text" id="nama" name="nama"> 
                </p> 
                <p> 
                    <label for="alamat">Alamat</label> 
                    <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea> 
                </p> 
                <p> 
                    <label>Jenis Kelamin</label> 
                    <input id="jk_l" type="radio" name="kelamin" value="L" />
                    <label for="jk_l">Laki-laki</label>
                    <input id="jk_p" type="radio" name="kelamin" value="P" />
                    <label for="jk_p">Perempuan</label> 
                </p> 
                <p><input type="submit" value="Login"></p> 
            </fieldset> 
        </form>
    </body> 
</html>
```
![image](https://user-images.githubusercontent.com/101440705/160273266-bd743479-cd13-46cd-b280-1ad6f7cf9c96.png)

### menambah Style Pada Form
Agar tampilan lebih menarik, kita akan tambahkan seditik style di form ini. untuk element `<style>`, kita akan taruh di antara tag `<head>` dan `</head>`
berikut codenya :
```
<!DOCTYPE html> 
<html lang="en"> 
    <head> 
        <meta charset="UTF-8"> 
        <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
        <title>HTML Lanjutan</title> 

        <!-- Menambah Style -->
        <style> 
            form p > label { 
            display: inline-block; 
            width: 100px; 
            } 
            form input[type="text"], form textarea { 
                border: 1px solid #197a43; 
            } 
            form input[type="submit"] { 
                border: 1px solid #197a43; 
                background-color: #197a43; 
                color: #ffffff; 
                font-weight: bold; 
                padding: 5px 15px; 
            } 
        </style>
    </head>
```
![image](https://user-images.githubusercontent.com/101440705/160273386-f2f359fd-e484-4f30-80bc-f015c64439ae.png)
===========================================================================

# Pertanyaan dan tugas
## Buatlah form yang menampilkan **dropdown** menu dan **listbox** dengan multiple selection.

Disini saya menambahkan elemen `<option>` untuk menu **Dropdown**, Berikut Code nya :
```
                <div>
                    <label for="Asal kota">Asal Kota</label>
                    <select>
                      <option selected>--pilih kota asal--</option>
                      <option>Jakarta</option>
                      <option>Bogor</option>
                      <option>Depok</option>
                      <option>Tanggerang</option>
                      <option>Bekasi</option>
                    </select>
                </div>
```
Dan dibawah ini akan saya tampilkan **listbox** multiple selection.

disini saya menggunakan element `<input type="Checkbox">`, berikut codenya :
```
                <div>
                    <label for="Hobi">Sangat Menyukai</label>
                    <input type="checkbox" name="Hobi" value="Olahraga"><label>Gym</label>
                    <input type="checkbox" name="Hobi" value="Membaca"><label>Makan</label>
                    <input type="checkbox" name="Hobi" value="Memancing"><label>Jalan-jalan di tengah malam</label>
                    <input type="checkbox" name="Hobi" value="Musik"><label>Ngopi</label>
                </div>
```
Berikut Hasilnya

![image](https://user-images.githubusercontent.com/101440705/160273698-2caf0391-d150-4684-bed6-160bac98b83a.png)

==================================SELESAI==================================


