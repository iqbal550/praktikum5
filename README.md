# praktikum5
# LATIHAN 1

• Buat Dictionary daftar kontak
• Nama sebagai key, dan nomor sebagai value
• Tampilkan kontaknya Gusti
• Tambah kontak baru dengan nama Ubay, nomor 087655234561
• Ubah kontak Nada dengan nomor baru 081245673567
• Tampilkan semua Nama
• Tampilkan semua Nomor
• Tampilkan daftar Nama dan nomornya
• Hapus kontak Nada.

    # 1. Buat Dictionary daftar kontak
    daftar_kontak = {
    "Gusti": "081267432213",
    "Nada": "088234567889",
    "Rusdi": "085766574241"
    }

    # 2. Tampilkan kontaknya Ari
    print("Kontak Gusti:", daftar_kontak.get("Gusti"))

    # 3. Tambah kontak baru dengan nama Ubay, nomor 087655234561
    daftar_kontak["Ubay"] = "087655234561"
    print("Kontak Ubay telah ditambahkan.")

    # 4. Ubah kontak Nada dengan nomor baru 081245673567
    daftar_kontak["Nada"] = "081245673567"
    print("Kontak Nada telah diubah.")

    # 5. Tampilkan semua Nama
    print("Semua Nama:", list(daftar_kontak.keys()))

    # 6. Tampilkan semua Nomor
    print("Semua Nomor:", list(daftar_kontak.values()))

    # 7. Tampilkan daftar Nama dan nomornya
    print("Daftar Nama dan Nomornya:")
    for nama, nomor in daftar_kontak.items():
    print(f"{nama}: {nomor}")

    # 8. Hapus kontak Nada
    if "Nada" in daftar_kontak:
    del daftar_kontak["Nada"]
    print("Kontak Nada telah dihapus.")
    else:
    print("Kontak Nada tidak ditemukan.")   

![kodee py 1](https://github.com/user-attachments/assets/00a16048-6fe7-4aaa-9ab4-21b417b79fdc)


PENJELASAN:   
1. Membuat Dictionary Daftar Kontak
Di sini, sebuah dictionary bernama daftar_kontak dibuat. Kunci (key) dari dictionary ini adalah nama-nama kontak (Gusti, Nada, Rusdi), dan nilainya (value) adalah nomor telepon yang sesuai. 
2. Menampilkan Kontak Gusti
Menggunakan metode get(), kode ini menampilkan nomor telepon yang terdaftar untuk kontak "Gusti". Jika "Gusti" tidak ada dalam dictionary, get() akan mengembalikan None tanpa menghasilkan error. 
3. Menambahkan Kontak Baru
Di sini, kontak baru dengan nama "Nada" dan nomor "088234567889" ditambahkan ke dalam dictionary. Jika nama tersebut sudah ada, nilainya akan diperbarui. Secara keseluruhan, kode ini menunjukkan bagaimana cara membuat, mengubah, menampilkan, dan menghapus data dalam sebuah dictionary yang digunakan untuk menyimpan daftar kontak.
4. Mengubah Kontak Nada
Kontak "Nada" diubah dengan nomor baru "081245673567". Jika "Nada" tidak ada, maka kontak baru akan ditambahkan.
5. Menampilkan Semua Nama
digunakan untuk mendapatkan semua kunci (nama) dari dictionary, yang kemudian diubah menjadi list untuk ditampilkan
6. Menampilkan Semua Nomor
digunakan untuk mendapatkan semua nilai (nomor telepon) dari dictionary, yang juga diubah menjadi list untuk ditampilkan.
7. Menampilkan Daftar Nama dan Nomornya
digunakan untuk mendapatkan pasangan kunci-nilai dari dictionary. Dalam loop, setiap nama dan nomor ditampilkan dalam format yang rapi.
8. Menghapus Kontak Nada

# PRAKTIKUM 5

    # Pastikan dictionary mahasiswa sudah didefinisikan
    mahasiswa = {}

    def tambah_data():
    print("\n=== TAMBAH DATA MAHASISWA ===")
    nama = input("Masukkan Nama: ")
    
    if nama in mahasiswa:  # Cek apakah nama sudah ada
        print("Data mahasiswa sudah ada!")
        return
    
    try:
        # Input nilai
        tugas = float(input("Nilai Tugas (0-100): "))
        uts = float(input("Nilai UTS (0-100): "))
        uas = float(input("Nilai UAS (0-100): "))
        
        # Validasi rentang nilai
        if not (0 <= tugas <= 100 and 0 <= uts <= 100 and 0 <= uas <= 100):
            print("Nilai harus berada dalam rentang 0-100!")
            return
        
        # Hitung nilai akhir
        nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
        
        # Simpan ke dictionary
        mahasiswa[nama] = {
            "tugas": tugas,
            "uts": uts,
            "uas": uas,
            "nilai_akhir": nilai_akhir
        }
        print("Data berhasil ditambahkan!")
    
    except ValueError:
        print("Input tidak valid! Pastikan untuk memasukkan angka.")

    # Contoh pemanggilan fungsi
    tambah_data()

 ![kode py 2](https://github.com/user-attachments/assets/012a8d97-76f5-471e-a0ca-bacd7ac8f3db)


    PENJELASAN : 

1. Fungsi lihat_data():
        Menampilkan daftar nilai mahasiswa dalam format tabel.
        Jika tidak ada data, menampilkan pesan bahwa tidak ada data.
        Menghitung nilai akhir berdasarkan bobot: 30% untuk tugas, 35% untuk UTS, dan 35% untuk UAS.
        Menggunakan enumerate untuk menampilkan nomor urut mahasiswa.

2. Fungsi tambah_data():
        Meminta input dari pengguna untuk menambahkan data mahasiswa baru.
        Data yang dimasukkan (NIM, nama, nilai tugas, UTS, dan UAS) disimpan dalam dictionary dan ditambahkan ke list data_mahasiswa.
        Menampilkan pesan konfirmasi bahwa data berhasil ditambahkan.

3. Fungsi ubah_data():
        Menampilkan data yang ada dengan memanggil lihat_data().
        Meminta pengguna untuk memasukkan nomor data yang ingin diubah.
        Jika nomor valid, pengguna diminta untuk memasukkan data baru, yang kemudian menggantikan data lama di list.
        Menampilkan pesan konfirmasi bahwa data berhasil diubah.

4. Fungsi hapus_data():
        Menampilkan data yang ada dengan memanggil lihat_data().
        Meminta pengguna untuk memasukkan nomor data yang ingin dihapus.
        Jika nomor valid, data dihapus dari list menggunakan pop().
        Menampilkan pesan konfirmasi bahwa data berhasil dihapus.

5. Fungsi cari_data():
        Meminta pengguna untuk memasukkan NIM yang ingin dicari.
        Mencari data mahasiswa berdasarkan NIM dan menampilkan hasilnya dalam format tabel.
        Jika tidak ditemukan, menampilkan pesan bahwa data tidak ditemukan.
   
    
![Gambar WhatsApp 2024-11-21 pukul 12 21 46_848e96da](https://github.com/user-attachments/assets/20b72897-4799-4e7c-8207-1c27be4db863)

