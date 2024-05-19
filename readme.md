A. Modul <br></br>
a. data list kosong

 	data_barang = []
 Baris di atas merupakan tipe data list yang akan digunakan untuk menyimpan data dictionary kedalam list. artinya baris di atas akan digunakan untuk menggabungkan data dictionary dengan 	 list.<br> </br>
  - Contoh output dari kode
    
    Output:
    
        Masukan pilihan anda: 7
        ============================ TEST ================================
        [{'nama barang': 'MANA', 'jumlah barang': 12}, {'nama barang': 'MONA', 'jumlah barang': 12}, {'nama barang': 'AC', 'jumlah barang': 12}]
        ==================================================================
  Contoh output di atas merupakan output yang akan muncul ketika anda memanggil 'data_barang' pada program setelah anda menambahkan data barang melalui fungsi 'tambah_barang'.<br></br>
  b. Fungsi tambah barang

    def tambah_barang():
        nama_barang   = str(input('Masukan nama barang    : ')) 
        nama_barang   = nama_barang.upper()
        jumlah_barang = int(input('Masukkan jumlah barang : ')) 
        data_baru = {'nama barang': nama_barang, 'jumlah barang': jumlah_barang}
        data_barang.append(data_baru)
        print(f'Message : Data Barang Berupa {nama_barang} Berhasil Di Tambahkan')
        return()
Baris diatas merupakan fungsi untuk menambahkan data barang kedalam list ('data_barang')  yang terdiri dari baris :
- Input nama

          nama_barang   = str(input('Masukan nama barang    : '))
  kode di atas digunakan untuk meng-input data berupa nama barang dan bertipe string
- Konversi input

          nama_barang   = nama_barang.upper()  
  kode di atas digunakan untuk mengonversi input dari pengguna ke dalam bentuk 'UPPERCASE'
- Input jumlah barang
        
          jumlah_barang = int(input('Masukkan jumlah barang : '))
  kode di atas digunakan untuk meng-input data berupa jumlah barang dan bertipe integer
- Variabel penyimpan input

        data_baru = {'nama barang': nama_barang, 'jumlah barang': jumlah_barang}
  Kode di atas di gunakan untuk menyimpan data input dari 'nama_barang' dan 'jumlah_barang' kedalam variabel 'data_baru' yang nantinya akan di masukkan kedalam list ('data_barang')
- Memasukkan hasil input

        data_barang.append(data_baru)
  kode di atas digunakan untuk menambahkan value dari vaiabel 'data_baru' kedalam variabel 'data_barang'

- Output informasi penambahan barang

        print(f'Message : Data Barang Berupa {nama_barang} Berhasil Di Tambahkan')
        return()
  kode di atas digunakan untuk menampilkan info bahwa penambahan value kedalam 'data_barang' telah berhasil

c. Fungsi hapus barang

        def hapus_barang():
            input_pilihan  = str(input('Silahkan pilih berdasarkan apa data di hapus? (Nama/Index) :' ))
            input_pilihan  = input_pilihan.capitalize()
            print(f'Pilihan anda adalah : {input_pilihan}')
            while True:
                if input_pilihan == 'Index':
                    index_barang = int(input('Masukan index barang : '))
                    data_barang.pop(index_barang)
                    print(f"barang dengan index {index_barang} telah berhasil dihapus")
                elif input_pilihan == 'Nama':
                    print('Jika anda memilih untuk menghapus dengan nama maka')
                    print('Anda harus memasukkan nama lengkap barang yang telah anda input')
                    nama_barang = str(input('Masukan nama barang  : ')).upper()
                    for barang in data_barang:
                        if barang['nama barang'] == nama_barang:
                            data_barang.remove(barang)
                            print(f"Message : Barang dengan nama '{nama_barang}' telah berhasil dihapus") # Kode yang di jalankan jika fungsi remove dijalankan
                            break
                    else:
                        print(f"Message : Barang dengan nama '{nama_barang}' tidak ditemukan.")
                else:
                     print('Input yang anda masukan tidak valid,')
                     print('harap masukan input yang valid [Nama/Index]')
                     print('Ulangi proses')
                break
            return()
Baris kode di atas merupakan baris kode yang di gunakan untuk menghapus data barang dalam variabel 'data_barang'. Berikut rinciannya:

- Input pilihan

        def hapus_barang():
                    input_pilihan  = str(input('Silahkan pilih berdasarkan apa data di hapus? (Nama/Index) :' ))
                    input_pilihan  = input_pilihan.capitalize()
                    print(f'Pilihan anda adalah : {input_pilihan}')
  kode di atas merupakan kode yang akan meminta pengguna untuk memasukkan pilihan di antara dua pilihan yang tersedia berupa 'Nama' atau 'Index'. Dan kemudian input dari pengguna akan di konversikan kedalam format 'Kapitalisasi' dan setelahnya menampilkan output format pilihan anda.
  

  
  

  
