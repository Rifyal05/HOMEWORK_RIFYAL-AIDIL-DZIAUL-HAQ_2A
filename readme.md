A. Modul <br></br>
a. data list kosong

 	data_barang = []
 Baris di atas merupakan tipe data list yang akan digunakan untuk menyimpan data dictionary kedalam list. artinya baris di atas akan digunakan untuk menggabungkan data dictionary dengan 	 list.<br> </br>
  - Contoh output dari kode
    
    - Output :
    
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
- contoh output dari kode
    - Output :
  
                Masukan pilihan anda: 1
                
                ========================= TAMBAH BARANG ==========================
                
                Masukan nama barang    : Mina
                Masukkan jumlah barang : 123
                
                ==================================================================
                Message : Data Barang Berupa MINA Berhasil Di Tambahkan
                ==================================================================

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
- Looping dan percabangann 1
  
        while True:
                if input_pilihan == 'Index':
                    index_barang = int(input('Masukan index barang : '))
                    data_barang.pop(index_barang)
                    print(f"barang dengan index {index_barang} telah berhasil dihapus")
  kode di atas merupakan kode untuk melakukan perulangan 'while' dimana perulangan ini akan terus berlanjut hingga ada kondisi yang membuatnya berhenti => ⚰ (death x_x).
  Dan kemudian kode itu akan meminta anda untuk memasukkan input 'index barang' dengan integer sebagai tipe datanya, lalu memunculkan output bahwa barang di dalam 'data_barang' telah di hapus berdasarkan nomor 'index' yang di input oleh pengguna.
 - Looping dan percabangan 2
    
          elif input_pilihan == 'Nama':
                    print('Jika anda memilih untuk menghapus dengan nama maka')
                    print('Anda harus memasukkan nama lengkap barang yang telah anda input')
                    nama_barang = str(input('Masukan nama barang  : ')).upper()
    kode di atas merupakan cek poin kedua dimana kode tersebut akan di jalankan jika cek poin pertama yaitu 'input_pilihan == 'Index' tidak terpenuhi. jika input terpenuhi dalam cek poin ini, kode selanjutnya akan di jalanlan yaitu anda diminta memasukkan nama lengkap dari barang yang akan anda hapus. jika tidak terpenuhi, maka akan di lanjutkan ke cek poin selanjutnya.
- Looping dan pecabangan 3

                      for barang in data_barang:
                        if barang['nama barang'] == nama_barang:
                            data_barang.remove(barang)
                            print(f"Message : Barang dengan nama '{nama_barang}' telah berhasil dihapus")
                            break

    kode di atas merupakan kode sub bagian dari kode pada poin "Looping dan Percabangan 2" yang berupa cek poin perulangan for yang digunakan untuk mengecek apakah input dari pengguna memenuhi syarat atau tidak untuk melanjutkan ke step berikutnya. jika iya, maka kode akan menghapus data barang dan kemudian memunculkan informasi bahwa data barang telah di hapus. Jika tidak, program akan melanjutkannya ke cek poin berikutnya

- Looping dan percabangan 4

                      else:
                        print(f"Message : Barang dengan nama '{nama_barang}' tidak ditemukan.")  
     kode di atas merupakan bagian dari poin "Looping dan percabangan 3" yang digunakan untuk menampilkan pesan bahwa barang yang ingin di hapus tidak ada atau tidak di temukan

- Looping dan perulangan 5

        else:
                     print('Input yang anda masukan tidak valid,')
                     print('harap masukan input yang valid [Nama/Index]')
                     print('Ulangi proses')
                     print()
                break
            return()
     kode diatas merupakan baris terakhir dari fungsi hapus barang yang akan dieksekusi jika cek poin 'elif' sebelumnya tidak terpenuhi dengan menampilkan output bahwa input yang di masukkan oleh pengguna tidak valid 

d. Fungsi Tampilkan Barang

        def tampil_barang():
            if not data_barang:
                print("Data Barang Kosong")
            else:
                print('Berikut Daftar Barang Yang Telah Anda Input:')
                for nomor, barang in enumerate(data_barang):  
                    print(f"{nomor}. {barang['nama barang']} dengan jumlah barang ""=", F"{barang['jumlah barang']}")
                    continue
            return()
  kode di atas merupakan baris kode dari fungsi 'tampil_barang' dimana fungsi tersebut digunakan untuk menampilkan barang yang telah di input oleh pengguna. Berikut rinciannya:
  - Mengecek data barang 1

         def tampil_barang():
                    if not data_barang:
                        print("Data Barang Kosong")
    kode di atas menggunakan operasi logika boolean yaitu negasi untuk mencari tau apakah variabel 'data_barang' memiliki nilai atau tidak. cara kerjanya adalah: <br></br>
    a. kata kunci 'not' digunakan sebagai negasi logika (pembalikan nilai) yaitu membalikan nilai dari nilai yang sebenarnya. misalnya a = true maka not a = false <br>
    b. blok kode if harus bernilai true untuk menjalankan prosesnya. Tetapi,<br>
    c. dalam kode ini variabel 'data_barang' kosong bernilai false karena variabel tersebut tidak memiliki nilai, oleh karena itu maka negasi 'not' digunakan untuk membalikan nilai dari nilai boolean variabel tersebut menjadi true dan membuat baris kode selanjutnya di eksekusi <br>
    d. jika variabel 'data_barang' memiliki nilai, maka akan bernilai true dan negasi 'not' digunakan untuk membalikan nilai dari nilai boolean variabel menjaddi false dan blok 'else' akan dijalankan <br>
    e. prinsip dari kode ini adalah jika tidak ada nilai maka variabel bernilai 'true' (setelah proses pembalikan) dan kode pada baris selanjutnya akan di jalankan, jika kode memiliki nilai maka kode akan masuk ke cek poin berikutnya yaitu cek poin 'else' <br>

 - Mengecek data barang 2
   
                  else:
                print('Berikut Daftar Barang Yang Telah Anda Input:')
                for nomor, barang in enumerate(data_barang):  
                    print(f"{nomor}. {barang['nama barang']} dengan jumlah barang ""=", F"{barang['jumlah barang']}")
                    continue
            return()
   Blok kode ini merupakan cek poin terkhir dari mengecek 'data_barang' dimana kode ini akan dijalankan jika cek poin pertama yaitu 'if' bernilai false. kode ini akan memberikan output "VALUE" dari isi data dictionary di dalam variabel 'nama barang' dan 'jumlah barang' di dalam dictionary tersebut dan outputnya juga akan menampilkan index dari output tersebut dengan menggunakan fungsi 'enumerate'
<br><br/>
e. cek data barang

              def cari_data():
                  keyword = str(input('Masukan keyword untuk mencari data: ')).upper()
                  found = False
                  print(f'Berikut barang yang di temukan berdasarkan kata kunci {keyword}:') 
                  i = 1
                  for barang in data_barang:
                      if keyword in barang['nama barang']:
                          print(f"{i}. {barang['nama barang']} dengan jumlah barang = {barang['jumlah barang']}")
                          found = True
                          i+=1
                          continue    
                  if not found:
                      print(f"Uhhh maaf tapi barang yang anda cari menggunakan kata kunci '{keyword}' tidak ditemukan.")
                      return()
- input dan pendefinisian
  
             keyword = str(input('Masukan keyword untuk mencari data: ')).upper()
                          found = False
                          print(f'Berikut barang yang di temukan berdasarkan kata kunci {keyword}:') 
                          i = 1
  kode di atas digunakan untuk meminta pengguna untuk memasukkan 'keyword' dan kemudian 'keyword' yang di input oleh pengguna akan di konversi ke dalam format 'UPPERCASEE'.
  kemudian variabel 'found' di gunakan untuk mendefinisikan bahwa input bernilai 'false'. 'i' digunakan sebagai iterasi penomoran yang akan digunakan untuk menampilkan data.
- perulangan dan percabangan 1

           for barang in data_barang:
                              if keyword in barang['nama barang']:
                                  print(f"{i}. {barang['nama barang']} dengan jumlah barang = {barang['jumlah barang']}")
                                  found = True
                                  i+=1

  kode di atas adalah kode yang digunakan untuk menemukan data 'barang' di variabel 'data_barang' berdasarkan keyword yang di masukkan oleh pengguna. berikut rinciannya: <br>

  - sub perulangan dan percabangan 1
  
        for barang in data_barang:

    kode di atas digunakan untuk mengiterasi data 'barang' kedalam variabel 'data_barang'
  - sub perulangan dan percabangan 2
 
        if keyword in barang['nama barang']:
    kode di atas digunakan untuk menegecek apakah 'keyword(Value input)' yang berada pada "iterasi" 'barang' ada di dalam variabel 'data_barang' dengan variabel dictionary 'nama_barang' yang berada dalam data list 'data_barang' ada atau tidak.
		  
  - sub perulangan dan percabangan 3
 
		  print(f"{i}. {barang['nama barang']} dengan jumlah barang = {barang['jumlah barang']}")
		  found = True
		  i+=1
    kode di atas akan mencetak barang dan jumlah barang yang telah di input oleh pengguna. kemudia menguah variabel 'found' menjadi bernilai true. kemudia 'i+=1' digunakan untuk membuat nomor dari setiap output yang di tampilkan

  - sub perulangan dan percabangan 4
	 
	    if not found:
	    print(f"Uhhh maaf tapi barang yang anda cari menggunakan kata kunci '{keyword}' tidak ditemukan.")
	    return()
    kode di atas adalah cek poin terakhir yang akan dijalankan jika found bernilai 'true', tetapi karena barang yang tidak ada bernilai 'false' sedangkan blok 'if' harus bernilai true, maka penggunaan fungsi 'not' ini di perlukan untuk membalikkan nilai dari yang sebelumnya yaitu 'false' menjadi 'true'. setelah itu mencetak pesan terkait ketidak adaan barangnya.

f. edit data

	def edit_data():
	    index_barang = int(input('Masukan index barang : '))
	    nama_barang = str(input('Masukan nama barang: ')).upper()
	    jumlah_barang = int(input('Masukkan jumlah barang: '))
	    data_barang[index_barang] = {'nama barang': nama_barang, 'jumlah barang': jumlah_barang}
	    print(f"Message : Data barang dengan index {index_barang} telah diubah.") 
	    return()
   kode diatas adalah kode yang digunakan untuk mengedit data barang. Berikut rinciannya: <br>
 - Input

		index_barang = int(input('Masukan index barang : '))
		nama_barang = str(input('Masukan nama barang: ')).upper()
		jumlah_barang = int(input('Masukkan jumlah barang: '))
    kode diatas digunakan untuk meminta pengguna memasukkan input berupa index, nama, dan jumlah barang.

- Mengubah

		data_barang[index_barang] = {'nama barang': nama_barang, 'jumlah barang': jumlah_barang}
		print(f"Message : Data barang dengan index {index_barang} telah diubah.") 
		return()
  setelah pengguna memasukkan data berupa index,nama, dan jumlah, maka variabel 'data_barang' dalam 'index(input pengguna)' akan mengubah value dai variabel 'nama barang' dengan hasil input dari 'nama_barang' dan 'jumlah_barang'. setelah itu, kode akan menampilkan pesan bahwa pengubahan data baang telah berhasil.



  

