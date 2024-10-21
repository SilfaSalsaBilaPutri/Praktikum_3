# Latihan
* Lengkapi latihan class Mahasiswa dengan setter dan getter.
  ```
  public class Mahasiswa extends Manusia {
    String nim;
    String jurusan;

    public Mahasiswa(String nama, String jenisKelamin, int umur, String alamat, String nim, String jurusan) {
        super(nama, jenisKelamin, umur, alamat);
        this.nim = nim;
        this.jurusan = jurusan;
    }

    // Getter dan Setter untuk Mahasiswa
    public String getNim() {
        return nim;
    }

    public void setNim(String nim) {
        this.nim = nim;
    }

    public String getJurusan() {
        return jurusan;
    }

    public void setJurusan(String jurusan) {
        this.jurusan = jurusan;
    }
    }
  ```
  Mahasiswa adalah subclass (kelas turunan), dan Manusia adalah superclass (kelas induk). Maka segala sesuatu yang dimiliki kelas Manusia seperti atribut dan metode akan secara otomatis dimiliki oleh Mahasiswa. Di dalam kelas Mahasiswa, ada dua atribut tambahan yang tidak ada di kelas Manusia, yaitu nim dan jurusan. Lalu memanggil constructor kelas Manusia dengan menggunakan kata kunci super() untuk menginisialisasi atribut dari kelas Manusia. Setelahnya menggunakan metode setter getter untuk memberikan nilai dan mengambil nilai dari masing-masing variabel.
# Hasil Output
![Screenshot 2024-10-21 223141](https://github.com/user-attachments/assets/e908e783-f576-462c-a1b8-f650fd614125)
* Implementasikan java code diagram pada class berikut:

![Screenshot 2024-10-21 215851](https://github.com/user-attachments/assets/b18f60c6-4934-4cc6-96b0-a36bfe179290)

- Menampilkan class Pegawai
  ```
  public class Pegawai {
    private String nama;
    private double gajiPokok;

    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getNama() {
        return nama;
    }

    public void setGajiPokok(double gajiPokok) {
        this.gajiPokok = gajiPokok;
    }

    public double getGajiPokok() {
        return gajiPokok;
    }

    public void cetakInfo() {
        System.out.println("Nama: " + nama);
        System.out.println("Gaji Pokok: " + gajiPokok);
    }
    }
    ```
- Menampilkan class Manager
  ```
  public class Manager extends Pegawai {
    private double tunjangan;

    public void setTunjangan(double tunjangan) {
        this.tunjangan = tunjangan;
    }

    public double getTunjangan() {
        return tunjangan;
    }

    @Override
    public void cetakInfo() {
        super.cetakInfo();
        System.out.println("Tunjangan: " + tunjangan);
    }

    public void cetakTunjangan() {
        System.out.println("Tunjangan: " + tunjangan);
    }
    }
    ```
- Menampilkan class Progremer
  ```
  public class Programmer extends Pegawai {
    private double bonus;

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    public double getBonus() {
        return bonus;
    }

    /**
     *
     */
    @Override
    public void cetakInfo() {
        super.cetakInfo();
        System.out.println("Bonus: " + bonus);
    }

    public void cetakBonus() {
        System.out.println("Bonus: " + bonus);
    }
    }
    ```
- Menampilkan class Main
  ```
  public class Main {
    public static void main(String[] args) {
        // Membuat objek Manager
        Manager manajer = new Manager();
        manajer.setNama("Budi");
        manajer.setGajiPokok(5000000);
        manajer.setTunjangan(2000000);
        manajer.cetakInfo();

        // Membuat objek Programmer
        Programmer programmer = new Programmer();
        programmer.setNama("Siti");
        programmer.setGajiPokok(4000000);
        programmer.setBonus(1000000);
        programmer.cetakInfo();
    }
    }
    ```
  Pada implementasi ini, class Manager dan Programmer mewarisi atribut dan metode dari class Pegawai. Mereka juga menambahkan atribut baru yaitu tunjangan untuk Manager dan bonus untuk Programmer, dengan metode setter, getter, dan metode tambahan untuk mencetak informasi yang relevan.
# Hasil Output
![Screenshot 2024-10-21 223116](https://github.com/user-attachments/assets/485ee40a-6387-442f-8e7d-35ea92ca42eb)
