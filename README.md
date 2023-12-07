# UAS-Pemrograman-Komputer-HIKMAH-MAHARANI-09011282328058
Nama: HIKMAH MAHARANI
Nim: 09011282328058
Kelas: SK1A
Ujian: Pemrograman Komputer 

1. Diskon Toko Online
    import java.util.Scanner;
public class DiskonTokoOnline {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Masukkan harga per barang: ");
        double hargaPerBarang = scanner.nextDouble();
        
        System.out.print("Masukkan jumlah barang yang dibeli: ");
        int jumlahBarang = scanner.nextInt();
        
        double totalHarga = hargaPerBarang * jumlahBarang;
        double diskon = 0;
        
        if (jumlahBarang >= 5 && jumlahBarang <= 10) {
            diskon = 0.05; 
        } else if (jumlahBarang >= 11 && jumlahBarang <= 20) {
            diskon = 0.10; 
        } else if (jumlahBarang > 20) {
            diskon = 0.20; 
        }
        
        double totalDiskon = totalHarga * diskon;
        double hargaSetelahDiskon = totalHarga - totalDiskon;
        
        System.out.println("Total harga sebelum diskon: " + totalHarga);
        System.out.println("Total diskon: " + totalDiskon);
        System.out.println("Total harga setelah diskon: " + hargaSetelahDiskon);
        scanner.close();
    }
}


2. Autentikasi Pengguna
   import java.util.Scanner;
public class AutentikasiPengguna {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        final String USERNAME = "user09011282328058";
        final String PASSWORD = "abc123";
        
        System.out.print("Masukkan username: ");
        String usernameInput = input.nextLine();
        
        System.out.print("Masukkan password: ");
        String passwordInput = input.nextLine();
        
        // Melakukan autentikasi
        if (USERNAME.equals(usernameInput) && PASSWORD.equals(passwordInput)) {
            System.out.println("**Autentikasi Berhasil**");
        } else {
            System.out.println("**Autentikasi Gagal**");
        }
        
        input.close();
    }
}
3. Deret Fibonacci
 import java.util.Scanner;
public class DeretFibonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Masukkan nilai n: ");
        int n = scanner.nextInt();
        int firstTerm = 0, secondTerm = 1;
        System.out.println("Deret Fibonacci hingga suku ke-" + n + ":");
        
        for (int i = 1; i <= n; ++i) {
            System.out.print(firstTerm + " ");
            
            int nextTerm = firstTerm + secondTerm;
            firstTerm = secondTerm;
            secondTerm = nextTerm;
            scanner.close();

        }
    }
}

4. Faktorisasi Bilangan
    import java.util.Scanner;
public class FaktorisasiBilangan {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Masukkan bilangan bulat positif: ");
        int number = scanner.nextInt();
        System.out.print("Faktorisasi " + number + ": ");
        
        for (int i = 2; i <= number; i++) {
            while (number % i == 0) {
                System.out.print(i + " ");
                number /= i;
                if (number > 1) {
                    System.out.print("* ");
                    scanner.close();
                }
            }
        }
    }
}

5. Kalkulator Sederhana
    import java.util.Scanner;
public class KalkulatorSederhana {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        System.out.print("Masukkan bilangan pertama: ");
        double bilangan1 = scanner.nextDouble();
        System.out.print("Masukkan bilangan kedua: ");
        double bilangan2 = scanner.nextDouble();

        System.out.println("Pilih operasi:");
        System.out.println("1. Penjumlahan");
        System.out.println("2. Pengurangan");
        System.out.println("3. Perkalian");
        System.out.println("4. Pembagian");

        System.out.print("Masukkan nomor operasi: ");
        int pilihan = scanner.nextInt();

        switch (pilihan) {
            case 1:
                System.out.println("Hasil penjumlahan: " + penjumlahan(bilangan1, bilangan2));
                break;
            case 2:
                System.out.println("Hasil pengurangan: " + pengurangan(bilangan1, bilangan2));
                break;
            case 3:
                System.out.println("Hasil perkalian: " + perkalian(bilangan1, bilangan2));
                break;
            case 4:
                System.out.println("Hasil pembagian: " + pembagian(bilangan1, bilangan2));
                break;
            default:
                System.out.println("Pilihan operasi tidak valid.");
        }
        scanner.close();
    }

    public static double penjumlahan(double a, double b) {
        return a + b;
    }

    public static double pengurangan(double a, double b) {
        return a - b;
    }

    public static double perkalian(double a, double b) {
        return a * b;
    }

    public static double pembagian(double a, double b) {
        if (b != 0) {
            return a / b;
        } else {
            System.out.println("Pembagian nol tidak valid.");
            return Double.NaN; 
        }
    }
}

6. Palindrom Cek
   public class PalindromCek {
    public static void main(String[] args) {
        String kata = "kasur rusak"; 
        System.out.println("Apakah '" + kata + "' adalah palindrom? " + isPalindrome(kata));
    }

    public static boolean isPalindrome(String kata) {
        kata = kata.toLowerCase().replaceAll("\\s+", "");
        int i = 0;
        int j = kata.length() - 1;
        while (i < j) {
            if (kata.charAt(i) != kata.charAt(j)) {
                return false;
            }
            i++;
            j--;
        }
        return true; 
    }
}

7. Perpustakaan Buku
    public class PerpustakaanBuku {
    private String judul;
    private String penulis;
    private int tahunTerbit;
    private boolean isDipinjam;

    public Buku(String judul, String penulis, int tahunTerbit) {
        this.judul = judul;
        this.penulis = penulis;
        this.tahunTerbit = tahunTerbit;
        this.isDipinjam = false;
    }

    public void TampilkanInfoBuku() {
        System.out.println("Judul Buku: " + judul);
        System.out.println("Penulis: " + penulis);
        System.out.println("Tahun Terbit: " + tahunTerbit);
        System.out.println("Status Pinjam: " + (isDipinjam ? "Dipinjam" : "Tersedia"));
    }

    public boolean pinjamBuku() {
        if (!isDipinjam) {
            isDipinjam = true;
            System.out.println(judul + " berhasil dipinjam.");
            return true;
        } else {
            System.out.println(judul + " sudah dipinjam.");
            return false;
        }
    }

    public boolean kembalikanBuku() {
        if (isDipinjam) {
            isDipinjam = false;
            System.out.println(judul + " berhasil dikembalikan.");
            return true;
        } else {
            System.out.println(judul + " tidak sedang dipinjam.");
            return false;
        }
    }

    public static void main(String[] args) {
        UAS_progkom7 buku1 = new UAS_progkom7("Hilmy Milan", "Nadia Ristivani", 2021);

        System.out.println("Informasi buku sebelum dipinjam:");
        buku1.tampilkanInfoBuku();

        buku1.pinjamBuku();

        System.out.println("\nInformasi buku setelah dipinjam:");
        buku1.tampilkanInfoBuku();
    }
}

8. Kelola Akun
     public class KelolaAkun {
    private String username;
    private String password;
    private boolean aktif;

    public KelolaAkun(String username, String password) {
        this.username = username;
        this.aktif = false;
    }
    public void tampilkanInfoAkun() {
        System.out.println("Username: " + username);
        System.out.println("Status: " + (aktif ? "Aktif" : "Nonaktif"));
    }
    public void aktifkanAkun() {
        if (!aktif) {
            System.out.println("Akun berhasil diaktifkan.");
            aktif = true;
        } else {
            System.out.println("Akun sudah aktif.");
        }
    }
    public void nonaktifkanAkun() {
        if (aktif) {
            System.out.println("Akun berhasil dinonaktifkan.");
            aktif = false;
        } else {
            System.out.println("Akun sudah nonaktif.");
        }
    }

    public static void main(String[] args) {
        KelolaAkun akun1 = new KelolaAkun("user09011282328058", "sayangjay");
        System.out.println("Informasi akun sebelum diaktifkan:");
        akun1.tampilkanInfoAkun();
        akun1.aktifkanAkun();
        System.out.println("\nInformasi akun setelah diaktifkan:");
        akun1.tampilkanInfoAkun();
        akun1.nonaktifkanAkun();
        System.out.println("\nInformasi akun setelah dinonaktifkan:");
        akun1.tampilkanInfoAkun();
    }
}

9. Cek Kurung
     import java.util.Stack;
public class CekKurung{
    public static void main(String[] args) {
        String ekspresi = "((2 + 2) * 3)";
        System.out.println("Ekspresi \"" + ekspresi + "\" memiliki kurung yang " + (cekKurung(ekspresi) ? "benar" : "salah"));
    }

    public static boolean cekKurung(String ekspresi) {
        Stack<Character> stack = new Stack<>();

        for (char c : ekspresi.toCharArray()) {
            if (c == '(') {
                stack.push(c);
            } else if (c == ')') {
                if (stack.isEmpty() || stack.pop() != '(') {
                    return false;
                }
            }
        }

        return stack.isEmpty();
    }
}
