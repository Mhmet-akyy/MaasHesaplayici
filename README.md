# MaasHesaplayici
import java.util.Scanner;

public class MaasHesaplayici {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("=== Maaş Hesaplayıcı Programı ===");

        // Kullanıcıdan verileri al
        System.out.print("Günlük çalışma saati: ");
        int gunlukSaat = input.nextInt();

        System.out.print("Aylık çalışılan gün sayısı: ");
        int calismaGunSayisi = input.nextInt();

        System.out.print("Saatlik ücret (₺): ");
        double saatlikUcret = input.nextDouble();

        // Hesaplamalar
        int toplamSaat = gunlukSaat * calismaGunSayisi;
        double brutMaas = toplamSaat * saatlikUcret;
        double vergi = brutMaas * 0.15; // %15 vergi
        double netMaas = brutMaas - vergi;

        // Sonuçları yazdır
        System.out.println("\n--- Maaş Bilgileri ---");
        System.out.println("Toplam Çalışma Saati: " + toplamSaat + " saat");
        System.out.println("Brüt Maaş: " + brutMaas + " ₺");
        System.out.println("Vergi (%15): " + vergi + " ₺");
        System.out.println("Net Maaş: " + netMaas + " ₺");

        input.close();
    }
}
