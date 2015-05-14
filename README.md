# Iqbal-REPO
package finalproject;

import java.util.Scanner;

public class uas2 {
    static Scanner scan = new Scanner(System.in); 
    static  uas2 panggil = new uas2();
    
    String[]  makanA = new String[7], minumB = new String[7] ;
    int[] pesanA = new int[7], pesanB = new int[7], porsiMakan = new int[7], 
            porsiMinum = new int[7], jumlahA = new int[7], jumlahB = new int[7] ;
    String makan1, makan2, makan3, makan4, makan5, makan6, makan7, 
            minum1, minum2, minum3, minum4, minum5, minum6, minum7 ;
    int i=0,lain, j=0, m, n, pesan, lagi, totalA, totalB, TOTAL, makan1a, makan2a, makan3a, makan4a, makan5a, makan6a, makan7a,
            minum1a, minum2a, minum3a, minum4a, minum5a, minum6a, minum7a ;
    boolean yaTidak;
    
    void daftarMenu() {
        makan1 = "1. Salad";
        makan1a = 9000;
        makan2 = "2. Pasta";
        makan2a = 15000;
        makan3 = "3. Steak";
        makan3a = 30000;
        makan4 = "4. Lasagna";
        makan4a = 25000;
        makan5 = "5. Burger";
        makan5a = 13000;
        makan6 = "6. Fried Chicken";
        makan6a = 9000;
        makan7 = "7. Rice";
        makan7a = 4000;
        
        
        minum1 = "1. Ice Tea";
        minum1a = 5000;
        minum2 = "2. Cappucino";
        minum2a = 13000;
        minum3 = "3. Milk Shake";
        minum3a = 15000;
        minum4 = "4. Blue Float";
        minum4a = 9000;
        minum5 = "5. Lemon Tea";
        minum5a = 8000; 
        minum6 = "6. Chocolate Ice Cream";
        minum6a = 15000;
        minum7 = "7. a Bottle of Water";
        minum7a = 4000;
    }
            
    void menu() {
        daftarMenu();
        System.out.println("~~~~~~~~~~~~Menu~~~~~~~~~~~");
        System.out.println(makan1 + "\t\t\t\t" + makan1a);
        System.out.println(makan2 + "\t\t\t\t" + makan2a);
        System.out.println(makan3 + "\t\t\t\t" + makan3a);
        System.out.println(makan4 + "\t\t\t\t" + makan4a);
        System.out.println(makan5 + "\t\t\t\t" + makan5a);
        System.out.println(makan6 + "\t\t\t" + makan6a);
        System.out.println(makan7 + "\t\t\t\t" + makan7a);
        System.out.println("");
        System.out.println(minum1 + "\t\t\t\t\t" + minum1a);
        System.out.println(minum2 + "\t\t\t\t" + minum2a);
        System.out.println(minum3 + "\t\t\t\t" + minum3a);
        System.out.println(minum4 + "\t\t\t\t" + minum4a);
        System.out.println(minum5 + "\t\t\t\t" + minum5a);
        System.out.println(minum6 + "\t\t\t" + minum6a);
        System.out.println(minum7 + "\t\t\t" + minum7a);
    
    }
    
    void makanAtauMinum(){
        System.out.println("ingin pesan Apa qaqa ??");
        System.out.println("1. Makan");
        System.out.println("2. Minum");
        System.out.print("Input : ");
        int pilih = scan.nextInt();
        
        switch (pilih) {
            case 1 :
                makan();
            case 2 :
                minum();
            default :
                System.out.println("Input qaqa salah, Silahkan input lagi");
                makanAtauMinum();
        }
    }
    
    void makan() {
        yaTidak = true;
        while (yaTidak) {
            System.out.println("Pesan Makanan nomor berapa qaqa?");
            System.out.print("Input : ");
            pesan = scan.nextInt();
        
            switch (pesan) {
                case 1 :
                    makanA[i] = makan1;
                    pesanA[i] = makan1a;
                    break;
                case 2 :
                    makanA[i] = makan2;
                    pesanA[i] = makan2a ;
                    break;
                case 3 :
                    makanA[i] = makan3;
                    pesanA[i] = makan3a ;
                    break;
                case 4 :
                    makanA[i] = makan4;
                    pesanA[i] = makan4a ;
                    break;
                case 5 :
                    makanA[i] = makan5;
                    pesanA[i] = makan5a ;
                    break;
                case 6 :
                    makanA[i] = makan6;
                    pesanA[i] = makan6a ;
                    break;
                case 7 :
                    makanA[i] = makan7;
                    pesanA[i] = makan7a ;
                    break;
                default :
                    System.out.println("Input salah, Silahkan input lagi qaqa");
                    makan();
            }
            
            System.out.println("Pesan berapa Porsi qaqa?");
            System.out.print("input : ");
            porsiMakan[i] = scan.nextInt();
            
            jumlahA[i] = porsiMakan[i] * pesanA[i];
            
            totalA += jumlahA[i];
            tanyamakanlain();
                   
        }            
    }
    
    void tanyamakanlain(){
    System.out.println("Apakah Anda ingin pesan makanan lain??");
            System.out.println("1. YA");
            System.out.println("2. TIDAK");
            lagi = scan.nextInt();
            switch (lagi) {
                case 1 :
                    i++ ;
                    makan();
                    break;
                case 2 :
                    tanyalain();
                    break;
                default :
                    System.out.println("Inputnya salah qaq");
                    tanyamakanlain();
            }
    }
    
    void tanyalain(){
    
        System.out.println("Ingin Pesan yang minum???");
        System.out.println("1. YA");
        System.out.println("2. TIDAK");
        System.out.print("Input : ");
        lain = scan.nextInt();
        switch (lain) {
            case 1 :
                minum();
                break;
            case 2 :
                output();
                break;
            default :
                System.out.println("Inputnya salah lo qaq, masukin lagi dong");
                tanyalain();        
        }
    }
    
    void minum() {
        yaTidak = true;
        while (yaTidak) {
            System.out.println("Pesan Minuman nomor berapa qaqa?");
            System.out.print("Input : ");
            pesanB[j] = scan.nextInt();
        
            switch (pesanB[j]) {
                case 1 :
                    minumB[j] = minum1;
                    pesanB[j] = minum1a ;
                    break;
                case 2 :
                    minumB[j] = minum2;
                    pesanB[j] = minum2a ;
                    break;
                case 3 :
                    minumB[j] = minum3;
                    pesanB[j] = minum3a ;
                    break;
                case 4 :
                    minumB[j] = minum4;
                    pesanB[j] = minum4a ;
                    break;
                case 5 :
                    minumB[j] = minum5;
                    pesanB[j] = minum5a ;
                    break;
                case 6 :
                    minumB[j] = minum6;
                    pesanB[j] = minum6a ;
                    break;
                case 7 :
                    minumB[j] = minum7;
                    pesanB[j] = minum7a ;
                    break;
                default :
                    System.out.println("Input salah, Silahkan input lagi qaqa");
                    minum();
            }
            
            System.out.println("Pesan berapa Porsi qaqa?");
            System.out.print("input : ");
            porsiMinum[j] = scan.nextInt();
            
            jumlahB[j] = porsiMinum[j] * pesanB[j];
            
            totalB += jumlahB[j];
            tanyaminumlain();
        }
    }
    
    void tanyaminumlain(){
    System.out.println("Apakah Anda ingin pesan minuman lain??");
            System.out.println("1. YA");
            System.out.println("2. TIDAK");
            lagi = scan.nextInt();
            switch (lagi) {
                case 1 :                    
                    j++ ;
                    minum();
                    break;
                case 2 :                    
                    output();
                    break;
                default : 
                    System.out.println("Input qaqa salah tuch, masukkan lagi yaaa");
                    tanyaminumlain();
            }
    }
    
    void output(){
        System.out.println("MAKAN");
        System.out.println("Nama\t|\t\tjumlah\t|\t\tHarga");
        for (m=0 ; m<=i ; m++ ){
            System.out.println(makanA[m]+"\t\t|"+porsiMakan[m]+"\t\t|"+jumlahA[m]);
        }
        System.out.println("Harga Total Makanan Anda = " + totalA);
        
        System.out.println("MINUM");
        System.out.println("Nama\t|\tjumlah\t|\tHarga");
        for (n=0 ; n<=j ; n++ ){
            System.out.println(minumB[n]+"\t\t|"+porsiMinum[n]+"\t\t|"+jumlahB[n]);
        }
        System.out.println("Harga Total Makanan Anda = " + totalB);
    
        System.out.println("=======================================");
        TOTAL = totalA +totalB;
        System.out.println("Harga Total Makan dan Minum anda = " + TOTAL);
        System.out.println("Silahkan Bayar qaqa! \n Terima Kasih atas Kunjungan Anda \n\n\n\n");
        System.exit(0);
      /* System.out.println();
       System.out.println("SIlahkan memesan!!!!");
       menu();
       makanAtauMinum();
       tanyalain();*/
    }
    
    public static void main(String[] args) {
       

        panggil.menu();
        panggil.makanAtauMinum();      
        
    
    }
}
