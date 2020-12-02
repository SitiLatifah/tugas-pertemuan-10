# tugas-pertemuan-10
# labs06danlabs07
**Nama	   	: Siti Latifah** <br>
**Nim	  	  : 312010321** <br>
**Kelas	  	: TI.20.A2** <br>
**Matkul	  : Bahasa Pemrograman** <br>


# Praktikum 6
## Latihan 1
![Screenshot (56)](https://user-images.githubusercontent.com/73010098/100722150-de52c280-33f2-11eb-8fd9-ab5f6130655c.png)
## Syntax
```python
#def a(x):
#return x**2
a = (lambda x: x ** 2)
print(a(10))

#def b(x, y):
#return math.sqrt(x**2 + y**2)
b = (lambda x,y: x**2 + y**2)
print(b(4,8))

#def c(*args):
#return sum(args)/len(args)
c = (lambda *args: sum(args)/ len(args))
print(c(4))

#def d(s):
#return "".join(set(s))
d = (lambda s: "".join(set(s)))
print(d("vwxyz"))
```
## OUTPUT
![Screenshot (54)](https://user-images.githubusercontent.com/73010098/100722351-1b1eb980-33f3-11eb-892d-139d7aea24c0.png)
![Screenshot (55)](https://user-images.githubusercontent.com/73010098/100722375-2245c780-33f3-11eb-91c1-c7b6282d3d70.png)

## Tugas Praktikum 6
![Screenshot (57)](https://user-images.githubusercontent.com/73010098/100837668-9a6bc600-34a3-11eb-941a-d4187e186637.png)
## Syntax
```python
data = {}

def tambah():
    print("Tambah Data")
    nama = input("Nama\t\t: ")
    nim = int(input("NIM\t\t\t: "))
    tugas = int(input("NIlai Tugas\t: "))
    uts = int(input("Nilai UTS\t: "))
    uas = int(input("Nilai UAS\t: "))
    nilaiakhir = (tugas * 0.3 + uts * 0.35 + uas * 0.35)
    data[nama] = nim, tugas, uts, uas, nilaiakhir


def tampilkan():
    if data.items():
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~| Daftar Nilai |~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("_______________________________________________________________________________________")
        print("|  No  |      NIM      |      NAMA         |    TUGAS   |   UTS   |   UAS   | AKHIR  |")
        print("|______|_______________|___________________|____________|_________|_________|________|__")
        i = 0
        for a in data.items():
            i += 1
            print(f"| {i:4} | {a[0]:13s} | {a[1][0]:17} | {a[1][1]:10d} |  {a[1][2]:6d} | {a[1][2]:7d} | {a[1][4]:6.2f} | ")
    else:
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~| Daftar Nilai |~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("_______________________________________________________________________________________")
        print("|  No  |      Nama     |      NIM      |   TUGAS  |   UTS   |   UAS   | Nilai Akhir  |")
        print("_______________________________________________________________________________________")
        print("|      |               |             Tidak Ada Data         |         |                |")
    print("____________________________________________________________________________________________")


def hapus():
    print("Hapus Data Nilai Mahasiswa")
    nama = input(" Masukan Nama\t:")
    if nama in data.keys():
        del data[nama]
        print()
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("===| BERHASIL MENGHAPUS DATA |===")
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    else:
        print("Data {0} tidak ada".format(nama))


def ubah():
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    print("===| Edit Data Nilai Mahasiswa |===")
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    nama = input("Masukan Nama\t\t: ")
    print("___________________________________")
    if nama in data.keys():
        nim = input("NIM baru\t\t\t: ")
        tugas = int(input("Nilai Tugas Baru\t: "))
        uts = int(input("Nilai UTS Baru\t\t: "))
        uas = int(input("Nilai UAS Baru\t\t: "))
        nilaiakhir = (tugas * 30 / 100 + uts * 35 / 100 + uas * 35 / 100)
        data[nama] = nim, tugas, uts, uas, nilaiakhir
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("====| BERHASIL MENGUBAH DATA |====")
        print("<><><><><><><><><><><><><><><><>")
    else:
        print("Data nilai {0} tidak ada ".format(nama))


while True:
    print("")
    print("|_<><><><><><><><><><><><><><><><><>_|")
    print("|~~~~~~~~| DATA MAHASISWA |~~~~~~~~~~|")
    print("|_<><><><><><><><><><><><><><><><><>_|")
    x = input("1.| Lihat Data \n2.| Tambah Data \n3.| Ubah Data \n4.| Hapus Data \n0.| Keluar Aplikasi \nPilih menu : ")
    if x.lower() == "1":
        tampilkan()
    elif x.lower() == "2":
        tambah()
    elif x.lower() == "3":
        ubah()
    elif x.lower() == "4":
        hapus()
    elif x.lower() == "0":
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("====== KELUAR DARI PROGRAM ======")
        print("<><><><><><><><><><><><><><><><>")
        break

    else:
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("== Pilihan Anda Tidak Tersedia ==")
        print("== Pilihlah Menu Yang Tersedia ==")
        print("<><><><><><><><><><><><><><><><>")
 ```
 
 * Pada tugas praktikum saya menggunakan fitur function yang ada di Python. Dan menggunakan media penyimpanan data berupa Dictionary
Saya akan menjelaskan dikit mengenai fitur-fitur yang ada dalam program sederhana saya.
Ketika program di run pada pertama kali, maka akan muncul tampilan seperti ini :
![Screenshot (59)](https://user-images.githubusercontent.com/73010098/100848281-7b753000-34b3-11eb-9a11-b170a517472e.png)
![Screenshot (60)](https://user-images.githubusercontent.com/73010098/100848285-7d3ef380-34b3-11eb-9c3b-9848b9e021e9.png)

Terdapat 5 Pilihan menu, yaitu :

   1 Tambah Data
   2 Lihat Data
   3 Ubah Data
   4 Hapus Data
   0 Keluar Aplikasi
   
* Menambahkan Data <br>
<img width="897" alt="praktikum 1" src="https://user-images.githubusercontent.com/73053784/100829441-f0d10880-3493-11eb-9c22-afd0235f4835.png">


* Lihat Data Nilai Mahasiswa<br>
System akan menjalankan fitur ini ketika user mengetikkan perintah 2 pada pilihan Pilih Menu (1-2-3-4-5)
Inilah tampilan fitur Lihat Data :
![Screenshot (59)](https://user-images.githubusercontent.com/73010098/100848281-7b753000-34b3-11eb-9a11-b170a517472e.png)
![Screenshot (60)](https://user-images.githubusercontent.com/73010098/100848771-284fad00-34b4-11eb-9bc5-19684c6ac272.png)

* ubah data <br> 
Pada fitur ini user akan diminta untuk memilih data siapa yang akan diubah dan data apa yang akan dirubah
Setelah user memilih data, Misalnya user ingin merubah NIM dari mahasiswa dengan nama Ery , Maka akan muncul tampilan seperti ini :
![Screenshot (59)](https://user-images.githubusercontent.com/73010098/100848281-7b753000-34b3-11eb-9a11-b170a517472e.png)
![Screenshot (62)](https://user-images.githubusercontent.com/73010098/100849102-a6ac4f00-34b4-11eb-8118-a75df17bc10d.png)

* Fitur Hapus Data Nilai Mahasiswa <br>
System akan menjalankan fitur ini ketika user mengetikkan perintah 4 pada pilihan Pilih Menu (1-2-3-4-5)
Sebelum saya menjalankan fitur ini, saya akan menambahkan 1 data lagi dengan nama Ery
![Screenshot (59)](https://user-images.githubusercontent.com/73010098/100848281-7b753000-34b3-11eb-9a11-b170a517472e.png)
![Screenshot (63)](https://user-images.githubusercontent.com/73010098/100849221-d3f8fd00-34b4-11eb-9f81-9b14025eea28.png)





