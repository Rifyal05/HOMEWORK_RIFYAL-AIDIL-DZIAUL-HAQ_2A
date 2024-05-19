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
        data_barang.append(data_baru) # Memasukkan dictionary key kedalam (list 'data_barang')
        print(f'Message : Data Barang Berupa {nama_barang} Berhasil Di Tambahkan')
        return()
Baris diatas merupakan fungsi untuk menambahkan data barang kedalam list ('data_barang')  yang terdiri dari baris :
- Input nama

        nama_barang   = str(input('Masukan nama barang    : '))
  kode di atas digunakan untuk meng-input data berupa nama barang dan bertipe string
  

  
