# MATHexrsiceJAVA
import java.util.Scanner;

class HelloWorld {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int cevap = 0;
        int dogru = 0;
        int yanlis = 0;
        int stopo = 1;
        int stopi = 1;

        while (stopo != 0) {
            System.out.println("ALISTIRMA NEDIR : ");
            System.out.println("1 : Carpma  ");
            System.out.println("2 : Toplama  ");
            System.out.println("3 : Cikarma  ");
            System.out.println("4 : 2. dereceden 2 bilinmeyenli denklemler  ");
            System.out.println(" cikmak istiyorsaniz sifira basin ");

            int sec = in.nextInt();
            stopo = sec;

            if (sec == 1) {
                while (stopi != 0) {
                    int x = (int) (Math.random() * 10 + 1);
                    int y = (int) (Math.random() * 10 + 1);
                    System.out.println(x + " * " + y + " = ? ");
                    int cev = in.nextInt();
                    stopi = cev;

                    if (cev == 0) {
                        stopi = 1;
                        break;
                    } else if (cev == x * y) {
                        cevap++;
                        System.out.println(" cevap dogru  " + x + " * " + y + " = " + (x * y));
                        dogru++;
                    } else {
                        cevap++;
                        System.out.println("cevap yanlis ! ");
                        System.out.println("dogru cevap : " + x + " * " + y + " = " + (x * y));
                        yanlis++;
                    }
                }
            } else if (sec == 2) {
                while (stopi != 0) {
                    int x = (int) (Math.random() * 10 + 1);
                    int y = (int) (Math.random() * 10 + 1);
                    System.out.println(x + " + " + y + " = ? ");
                    int cev = in.nextInt();
                    stopi = cev;

                    if (cev == 0) {
                        stopi = 1;
                        break;
                    } else if (cev == x + y) {
                        cevap++;
                        System.out.println(" cevap dogru  " + x + " + " + y + " = " + (x + y));
                        dogru++;
                    } else {
                        cevap++;
                        System.out.println("cevap yanlis ! ");
                        System.out.println("dogru cevap : " + x + " + " + y + " = " + (x + y));
                        yanlis++;
                    }
                }
            } else if (sec == 3) {
                while (stopi != 0) {
                    int x = (int) (Math.random() * 10 + 1);
                    int y = (int) (Math.random() * 10 + 1);
                    System.out.println(x + " - " + y + " = ? ");
                    int cev = in.nextInt();
                    stopi = cev;

                    if (cev == 0) {
                        stopi = 1;
                        break;
                    } else if (cev == x - y) {
                        cevap++;
                        System.out.println(" cevap dogru  " + x + " - " + y + " = " + (x - y));
                        dogru++;
                    } else {
                        cevap++;
                        System.out.println("cevap yanlis ! ");
                        System.out.println("dogru cevap : " + x + " - " + y + " = " + (x - y));
                        yanlis++;
                    }
                }
            } else if (sec == 4) {
                while (stopi != 0) {
                    int x = (int) (Math.random() * 10 + 1);
                    int y = (int) (Math.random() * 10 + 1);
                    int kts1 = (int) (Math.random() * 10 + 2);
                    int kts2 = (int) (Math.random() * 10 + 2);
                    int kts3 = (int) (Math.random() * 10 + 2);
                    int kts4 = (int) (Math.random() * 10 + 2);
                    int dnk1 = x * kts1 + kts3 + y;
                    int dnk2 = x * kts2 + kts4;
                    System.out.println(kts2 + "*x + " + kts4 + " = " + dnk2);
                    System.out.println(kts1 + "*x + y + " + kts3 + " = " + dnk1);
                    System.out.println(" y = ? ");
                    int cev = in.nextInt();
                    stopi = cev;
                    if (cev == 0) {
                        stopi = 1;
                        break;
                    }
                    if (cev == y) {
                        cevap++;
                        System.out.println(" tebrikler cevab dogru y = " + y);
                        dogru++;
                    } else {                  
                        cevap++;
                        System.out.println("maalesef cevabiniz yanlis ");
                        System.out.println("dogru cevap y = " + y);
                        yanlis++;
                    }
                }
            } else if (sec == 0) {
                System.out.println("cikiliyor ... sonuclar gosteriliyor ...  ");
            } else {
                System.out.println(" yanlis tuslama ! ");
            }
        }

        System.out.println("cevaplanan soru sayisi : " + cevap);
        System.out.println("cevaplanan dogru soru sayisi : " + dogru);
        System.out.println("cevaplanan yanlis soru sayisi : " + yanlis);

        if (dogru < yanlis) {
            System.out.println("maalesef testi gecmediniz  ");
        } else if (dogru == yanlis) {
            System.out.println(" lutfen tekrar deneyin");
        } else {
            System.out.println("tebrikler testi gectiniz  ");
        }
    }
}
