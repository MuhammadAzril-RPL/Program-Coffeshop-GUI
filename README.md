# Aplikasi Menu Kafe - Sistem Pemesanan Makanan dan Minuman

Aplikasi ini merupakan sistem pemesanan makanan dan minuman berbasis grafis (GUI) yang dibuat menggunakan Python dan Tkinter. Pengguna dapat memilih menu makanan, minuman, dan dessert melalui checkbox, kemudian memasukkan jumlah yang diinginkan untuk setiap item. Aplikasi ini secara otomatis menghitung harga subtotal, pajak, dan total yang harus dibayar.

## Fitur

- Pemilihan makanan, minuman, dan dessert menggunakan checkbox.
- Pengguna dapat mengisi jumlah item yang dipesan melalui entri (input).
- Kalkulasi subtotal dan pajak secara otomatis.
- Tampilan yang responsif dan mudah digunakan.

Cara Menggunakan
Pilih Menu
Pengguna dapat memilih berbagai item dari menu makanan, minuman, dan dessert. Cukup centang checkbox di samping nama menu yang ingin dipesan.

Masukkan Jumlah
Setelah memilih item, Anda bisa memasukkan jumlah yang diinginkan untuk setiap item. Misalnya, jika memilih "Pancake", Anda bisa mengisi jumlahnya pada kolom yang tersedia di sebelah kanan nama item.

Hitung Total
Setelah memilih semua menu yang diinginkan, aplikasi akan menghitung subtotal berdasarkan harga item yang dipilih dan jumlah yang dimasukkan.

Cetak Struk
Setelah selesai memilih dan menghitung harga, Anda dapat mencetak struk yang menunjukkan rincian pesanan.

Penjelasan Kode
Aplikasi ini menggunakan Tkinter untuk membuat antarmuka grafis. Berikut adalah penjelasan mengenai bagian-bagian utama dari kode:

Widget Checkbox
Setiap menu makanan, minuman, dan dessert dilengkapi dengan checkbox yang dapat dicentang atau tidak. Ketika checkbox dicentang, kolom entri untuk memasukkan jumlah akan aktif.

python
Copy
def avocadotoast():
    if var8.get() == 1:
        textavocadotoast.config(state=NORMAL)
        textavocadotoast.delete(0, END)
        textavocadotoast.focus()
    else:
        textavocadotoast.config(state=DISABLED)
        e_avocadotoast.set('0')
Pembuatan Frame
Aplikasi dibagi menjadi beberapa frame untuk menampilkan menu makanan, minuman, dan dessert. Setiap kategori menu dibuat menggunakan LabelFrame:

python
Copy
brunchFrame = LabelFrame(menuFrame, text=' Brunch ', font=('Castellar', 19, 'bold'), bd=10, relief=RIDGE, fg='#2f2f2f', bg='#f6f6f6')
brunchFrame.pack(side=LEFT)
Kolom Input dan Checkbox
Untuk setiap menu, ada kolom input (entry) untuk jumlah yang dipesan dan checkbox untuk memilih item. Contoh untuk menu makanan:

python
Copy
pancake = Checkbutton(brunchFrame, text='Pancake', font=('Calibri', 16, 'bold'), onvalue=1, offvalue=0, variable=var1, command=pancake, bg='#f6f6f6')
pancake.grid(row=0, column=0, sticky=W)
textpancake = Entry(brunchFrame, font=('Calibri', '16', 'bold'), bd=7, width=8, state=DISABLED, textvar=e_pancake)
textpancake.grid(row=0, column=1)
Struktur Kode
1. Fungsi Mengaktifkan/Menonaktifkan Entri
Setiap menu memiliki fungsi terkait yang mengaktifkan atau menonaktifkan kolom entri sesuai dengan apakah checkbox dicentang atau tidak. Contoh:

python
Copy
def avocadotoast():
    if var8.get() == 1:
        textavocadotoast.config(state=NORMAL)
        textavocadotoast.delete(0, END)
        textavocadotoast.focus()
    else:
        textavocadotoast.config(state=DISABLED)
        e_avocadotoast.set('0')
2. Pembuatan Frame
Setiap kategori menu ditempatkan dalam frame agar tampilan lebih rapi dan mudah dipahami oleh pengguna.

python
Copy
brunchFrame = LabelFrame(menuFrame, text=' Brunch ', font=('Castellar', 19, 'bold'), bd=10, relief=RIDGE, fg='#2f2f2f', bg='#f6f6f6')
brunchFrame.pack(side=LEFT)
3. Kolom Input dan Checkbox
Setiap item menu dilengkapi dengan checkbox untuk memilih menu dan kolom entri untuk memasukkan jumlah yang dipesan. Contoh untuk menu makanan seperti pancake:

python
Copy
pancake = Checkbutton(brunchFrame, text='Pancake', font=('Calibri', 16, 'bold'), onvalue=1, offvalue=0, variable=var1, command=pancake, bg='#f6f6f6')
pancake.grid(row=0, column=0, sticky=W)
textpancake = Entry(brunchFrame, font=('Calibri', '16', 'bold'), bd=7, width=8, state=DISABLED, textvar=e_pancake)
textpancake.grid(row=0, column=1)
