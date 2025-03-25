**this repo set to be able detect if being cloned**

# Dokumentasi Penjelasan

## 1. Mengganti warna background menjadi hijau muda

![Image](https://github.com/user-attachments/assets/83d3f483-ccb9-498e-8a18-57c09c889fdd)

Di dalam blok setContent, digunakan komponen Surface dengan modifier Modifier.fillMaxSize() yang memastikan komponen mengisi seluruh layar. Properti color pada Surface diatur ke Color(0xFFD5E8BE). Warna ini merupakan representasi dari hijau muda dalam format hexadecimal.

## 2. Membuat gambar bergerak-gerak saat sedang me-rolling

![Image](https://github.com/user-attachments/assets/8f800662-12a7-40ad-aef4-4154d9fb2d2f)

- Animasi Pergerakan:
1) Variabel shake dideklarasikan sebagai objek Animatable bertipe Float.
2) Animasi diatur menggunakan fungsi animateTo dengan infiniteRepeatable dan keyframes. Dalam animasi ini, gambar digeser secara horizontal menggunakan properti offset pada komponen Image.
3) Keyframe mengatur nilai-nilai pergeseran (misalnya, 10dp ke kanan dan -10dp ke kiri) selama durasi animasi 100 milidetik, sehingga menciptakan efek getar atau “shake”.

- Kondisi Animasi:
Animasi hanya aktif ketika variabel isRolling bernilai true. Artinya, saat pengguna menekan tombol dan proses pengacakan dadu sedang berlangsung, gambar dadu akan bergerak secara dinamis.

- Reset Animasi:
Setelah penundaan selama 1000 milidetik (simulasi durasi rolling), nilai dadu diperbarui secara acak dan animasi dihentikan dengan mengembalikan nilai shake ke nol menggunakan snapTo(0f).

## 3. Mengganti button teks menjadi "Rolling..." saat sedang me-rolling.

![Image](https://github.com/user-attachments/assets/8ae4c3a4-82dd-46ca-a660-a7b985248fcb)

- Penggunaan Kondisi:
Pada komponen Button, teks yang ditampilkan dikelola melalui komponen Text yang mengacu pada kondisi isRolling. Jika isRolling bernilai true, maka teks yang ditampilkan adalah "Rolling...". Jika tidak, maka teks yang muncul adalah "Roll".

- Manajemen Status:
Selain mengganti teks, properti enabled pada tombol juga diatur sehingga tombol tidak dapat ditekan lagi saat proses rolling sedang berlangsung. Hal ini membantu mencegah pemicu ganda atau konflik selama animasi.
