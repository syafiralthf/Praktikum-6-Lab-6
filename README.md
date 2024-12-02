# Biodata

Nama: Syafira Luthfi Azzahra

Kelas: TI.24.A.4

NIM: 312410353

# Latihan 1

![Screenshot from 2024-11-26 14-22-32](https://github.com/user-attachments/assets/7671aac1-384f-4cbb-af9f-42165a4e20fb)

## Latihan 1.py

```python
import math

a = lambda x: x**2
b = lambda x, y: math.sqrt(x*2 + y*2)
c = lambda *args: sum(args)/len(args) if args else 0
d = lambda s: "".join(set(s)) 

print("lambda a(5):", a(5))
print("lambda b(3, 4):", b(3, 4))
print("lambda c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))
print("lambda d('hello Syafira'):", d("Syafira"))
```

## Code Program

![image](https://github.com/user-attachments/assets/8261d24d-29b4-4746-9d77-f27f22f867e1)

## Hasil Program

![image](https://github.com/user-attachments/assets/b3197a2f-6127-4783-8219-809d221118a3)

# Tugas Praktikum

![image](https://github.com/user-attachments/assets/4a8a9c64-6ab8-4fdc-868d-2622883b9060)

## Tugas Praktikum.py

```python
def tambah():
    """Menambahkan data mahasiswa baru ke dalam daftar."""
    nama = input("Masukkan nama mahasiswa: ")
    if not nama.strip():
        print("Nama tidak boleh kosong.")
        return
    try:
        nilai = int(input("Masukkan nilai mahasiswa: "))
    except ValueError:
        print("Nilai harus berupa angka.")
        return
    daftar_mahasiswa[nama] = nilai
    print("Data mahasiswa berhasil ditambahkan.")

def tampilkan():
    """Menampilkan semua data mahasiswa."""
    if not daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
    else:
        print("Daftar Mahasiswa:")
        for nama, nilai in daftar_mahasiswa.items():
            print(f"{nama}: {nilai}")

def hapus(nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        del daftar_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

def ubah(nama):
    """Mengubah data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        try:
            nilai_baru = int(input(f"Masukkan nilai baru untuk {nama}: "))
            daftar_mahasiswa[nama] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah.")
        except ValueError:
            print("Nilai harus berupa angka.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

daftar_mahasiswa = {}

if __name__ == "__main__":
    while True:
        print("\nMenu:")
        print("1. Tambah data")
        print("2. Tampilkan data")
        print("3. Hapus data")
        print("4. Ubah data")
        print("5. Keluar")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == '1':
            tambah()
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            ubah(nama)
        elif pilihan == '5':
            print("Terima kasih!")
            break
        else:
            print("Pilihan tidak valid.")
```

## Penjelasan Code

```python
"""Menambahkan data mahasiswa baru ke dalam daftar."""
    nama = input("Masukkan nama mahasiswa: ")
    if not nama.strip():
        print("Nama tidak boleh kosong.")
        return
    try:
        nilai = int(input("Masukkan nilai mahasiswa: "))
    except ValueError:
        print("Nilai harus berupa angka.")
        return
    daftar_mahasiswa[nama] = nilai
    print("Data mahasiswa berhasil ditambahkan.")
```

Meminta pengguna untuk memasukan nama mahasiswa.Apabila nama kosong maka klick spasi.Program akan mencetak kesalahan dan keluar dari program tersebut. Menggunakan `try-except` untuk mengonversi nilai yang dimasukan menjadi integer, apabila gagal program akan mencetak pesan yang tidak valid, jika semua valid data mahasiswa(nama dan nilai) ditambahkan kedalam dictionary `daftar mahasiswa` dan program akan pesan konfirmasi.

```python
def tampilkan():
    """Menampilkan semua data mahasiswa."""
    if not daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
    else:
        print("Daftar Mahasiswa:")
        for nama, nilai in daftar_mahasiswa.items():
            print(f"{nama}: {nilai}")
```

fungsi ini menampilkan semua data mahasiswa yang ada dalam `daftar mahasiswa` kosong, apabila tidak kosong, mencetak `daftar mahasiswa` dan menggunakan loop untuk mencetak setiap nama mahasiswa dan nilai mereka dalam format `nama : nilai`.

```python
def hapus(nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        del daftar_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")
```

memeriksa nama mahasiswa apakah yang ingin di hapus ada dalam `daftar_mahasiswa`, apabila ada data mahasiswa dihapus menggunakan pesan konfirmasi bahwa data berhasil dihapus, apabila tidak ada maka program akan mencetak pesan bahwa mahasiswa tersebut tidak ditemukan.

```python
def ubah(nama):
    """Mengubah data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        try:
            nilai_baru = int(input(f"Masukkan nilai baru untuk {nama}: "))
            daftar_mahasiswa[nama] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah.")
        except ValueError:
            print("Nilai harus berupa angka.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")
```

Mengubah nilai mahasiswa berdasarkan yang di masukan, memeriksa apakah nama mahasiswa ada dalam `daftar_mahasiswa`, apabila ada maka pengguna akan diminta memasukan nilai baru dan mecoba megonversi nya menjadi `integer`. Jika konversi berhasil maka nilai mahasiswa diperbarui dalam `dictionary` dan mencetak pesan konfirmasi, apabila konversi gagal maka akan mencetak pesan kesalahan.dan apabila nama tidak ditemukan maka pesan akan mencetak bahwa mahasiswa tidak ditemukan.

`daftar_mahasiswa = {}`

`daftar_mahasiswa` adalah `dictionary` kosong yang akan digunakan untuk menyimpan `data_mahasiswa`

```python
if __name__ == "__main__":
    while True:
```

`if __name__ == "__main__"`: memastikan bahwa kode didalam blok ini akan dijalankan jika file ini dieksekusi langsung bukan ketika di impor sebagai modul oleh program lain. `While true` loop tak terbatas yang akan terus berjalan apabila perintah break di jalankan.

```python
print("\nMenu:")
        print("1. Tambah data")
        print("2. Tampilkan data")
        print("3. Hapus data")
        print("4. Ubah data")
        print("5. Keluar")
```

Program mencetak menu dengan lima opsi yang dapat dipilih penggguna:

1. Tambah Data: untuk menambahkan data mahasiswa baru
2.Tampilkan data: untuk menapilkan semua data mahasiswa yang telah dimasukan
3. Hapus data: Menghapuskan data mahasiswa sesuai nama
4. Ubah data: mengubah nilai mahasiswa berdasarkan nama
5. keluar: berhenti dari program

```python
pilihan = input("Pilih menu (1-5): ")
```

Program meminta pengguna untuk memasukan salah satu menu

```python
if pilihan == '1':
            tambah()
        elif pilihan == '2':
            tampilkan()
```
jika pengguna memasukan angka 1 maka fungsi akan `tambah()`, apabila pengguna memasukan angka 2 maka fungsi akan `tampilkan()` untuk menampilkan semua data mahasiswa yang ada dalam `daftar_mahasiswa`

```python
elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            ubah(nama)
```

Apabila pengguna memasukan angka 3 maka program akan meminta `input` nama mahasiswa yang ingin dihapus, jika pengguna memasukan angka 4 maka program akan meminta `input` nama mahasiswa yang ingin diubah.

```python
elif pilihan == '5':
            print("Terima kasih!")
            break
```

Jika pengguna memasukan angka 5 maka program akan mencetak `terima kasih !` dan keluar dari loop utama dengan menggunakan `break`.

```python
else:
            print("Pilihan tidak valid.")
```

Jika pengguna tidak memasukan angka `1-5` maka program akan menampilkan pesan `pilihan tidak valid` dan kembali menampilkan menu.

## Code Program

![image](https://github.com/user-attachments/assets/75a88463-5041-43c2-8236-d1f346d61c06)

Hasil Program

![image](https://github.com/user-attachments/assets/1382dc78-3dcb-4dbe-8a46-fd7c73820538)

Flowchart

![image](https://github.com/user-attachments/assets/33458806-846f-45dd-9af2-12dbaaf9675a)
