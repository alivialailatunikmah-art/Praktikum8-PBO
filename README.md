1. AlatElektronik.java
	Kode program tersebut berada di dalam paket com.praktikum8 dan mendefinisikan sebuah interface bernama AlatElektronik. Di dalam Java, interface berfungsi sebagai kontrak atau cetak biru yang berisi kumpulan method abstrak tanpa bodi, sehingga tidak dapat diinstansiasi secara langsung menggunakan kata kunci new. Setiap kelas yang mengimplementasikan interface ini wajib menyediakan isi atau implementasi untuk seluruh method di dalamnya. Di dalam interface AlatElektronik ini terdapat dua method abstrak, yaitu nyalakan() untuk merepresentasikan perilaku menyalakan perangkat—yang secara otomatis bersifat public dan abstract serta matikan() untuk merepresentasikan perilaku mematikan perangkat elektronik tersebut.
2. Anjing.java
package com.praktikum8;: Menunjukkan bahwa kelas ini berada di dalam paket (folder) com.praktikum8.   
public class Anjing extends Hewan: Mendefinisikan sebuah kelas turunan (subclass) bernama Anjing yang mewarisi sifat dan perilaku dari kelas induk (superclass) Hewan.   
@Override: Sebuah anotasi opsional namun sangat direkomendasikan untuk menandai bahwa method di bawahnya sedang melakukan override (menimpa/menyesuaikan ulang) method yang ada di kelas induknya.   
public void bersuara(): Mengubah isi dari method bersuara() yang sebelumnya ada di kelas Hewan agar spesifik menjadi perilaku anjing.   
System.out.println("Anjing: Guk guk!");: Perintah untuk mencetak teks "Anjing: Guk guk!" ke konsol ketika method ini dijalankan. 
3. BangunDatar.java
public abstract class BangunDatar: Kelas abstrak yang berfungsi sebagai cetak biru (blueprint) dasar untuk berbagai bentuk bangun datar. Kelas abstrak tidak bisa diinstansiasi secara langsung menggunakan kata kunci new.   
Atribut & Konstruktor: Memiliki variabel warna beserta konstruktor untuk menginisialisasi warna bangun datar tersebut.   
public abstract double hitungLuas(): Method abstrak yang tidak memiliki isi (bodi) dan wajib di-override oleh kelas turunannya.   
public void cetakWarna(): Method biasa (concrete method) yang sudah memiliki implementasi untuk mencetak informasi warna bangun datar. 
4. Hewan.java
public class Hewan: Ini adalah kelas dasar (superclass) yang merepresentasikan konsep umum tentang hewan.  
public void bersuara(): Method konkrit yang mencetak teks standar mengenai suara hewan ke konsol. Method ini nantinya dapat di-override oleh kelas-kelas turunannya.
5. Kamera.java
package com.praktikum8;: Menunjukkan bahwa interface ini terletak di dalam package (folder) dengan nama com.praktikum8.  
public interface Kamera: Mendefinisikan sebuah interface bernama Kamera. Di dalam Java, interface berfungsi sebagai kontrak atau cetak biru yang berisi kumpulan method tanpa bodi (abstrak) dan tidak dapat diinstansiasi secara langsung menggunakan kata kunci new.   
void ambilFoto();: Sebuah method abstrak di dalam interface yang merepresentasikan perilaku atau fungsionalitas untuk mengambil foto. Kelas apa pun yang mengimplementasikan (implements) interface Kamera wajib menyediakan isi atau implementasi nyata untuk method ini.
6. Kucing.java
public class Kucing extends Hewan: Kelas Kucing merupakan kelas turunan (subclass) dari Hewan.  
@Override & public void bersuara(): Melakukan method overriding untuk mengubah isi dari method bersuara() agar sesuai dengan karakteristik kucing, yaitu mencetak "Kucing: Meow meow!". 
7. Lingkaran.java
public class Lingkaran extends BangunDatar: Kelas turunan dari BangunDatar.   
private double jariJari: Variabel khusus untuk menyimpan nilai jari-jari lingkaran.   
Konstruktor: Menggunakan super(warna) untuk meneruskan parameter warna ke konstruktor kelas induknya (BangunDatar), serta mengisi nilai jariJari.   
public double hitungLuas(): Implementasi wajib dari method abstrak kelas induk untuk menghitung luas lingkaran  
8. PoliTester.java
main Method & Polimorfisme: Mendemonstrasikan konsep polimorfisme menggunakan array dari superclass (Hewan[] daftarHewan = new Hewan[3]).   
Upcasting: Array diisi dengan objek dari kelas induk maupun kelas turunannya (new Hewan(), new Kucing(), dan new Anjing()).  
Perulangan for: Melakukan iterasi untuk memanggil method h.bersuara() secara dinamis sesuai dengan bentuk objek aslinya saat runtime. 
9. Smartphone.java
public class Smartphone implements AlatElektronik, Kamera: Menunjukkan penerapan konsep Multiple Inheritance menggunakan Interface. Kelas Smartphone mengimplementasikan kontrak dari dua interface sekaligus yaitu AlatElektronik dan Kamera.   
Atribut & Konstruktor: Memiliki variabel merk dan konstruktor untuk mengaturnya.   Implementasi Method (@Override): Menyediakan isi untuk method-method yang diwariskan dari interface, seperti nyalakan(), matikan(), dan ambilFoto().   
10. TesBangunDatar.java 
Kelas Pengujian (Runner): Berisi fungsi main untuk menguji fungsionalitas dari kelas Lingkaran.   
Membuat objek lingkaran dengan warna "Merah" dan jari-jari 5, kemudian memanggil method cetakWarna() serta menghitung dan mencetak luasnya menggunakan hitungLuas().
11. TesSmartphone.java 
Kelas Pengujian Smartphone: Berisi fungsi main untuk menjalankan objek Smartphone dengan parameter merk "Samsung".   
Memanggil method hp.nyalakan(), hp.ambilFoto(), dan hp.matikan() secara berurutan untuk melihat hasil eksekusi dari interface yang diimplementasikan. 
nb. penjelasan code sesuai urutan code yg terlampir diatas ya kak
