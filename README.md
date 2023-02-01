# Friend_numbers.java
    import java.util.Scanner;

    class num_amigos {
        public static void main(String args[]) {
            try (Scanner scan = new Scanner(System.in)) {
                System.out.println("Escribe el primer numero amigo:");
                int amigo1 = scan.nextInt();

                System.out.println("Escribe el segundo numero amigo:");
                int amigo2 = scan.nextInt();


                int amigoA = amigo1, amigoB = amigo2;
                int contadorA = 0, contadorB = 0;

                for (int i = 1; i <= amigoA-1; i++) {
                    if (amigoA % i == 0) {
                        contadorA = contadorA + i;
                        System.out.println("División: " + amigoA + " % " + i + " = " + contadorA);
                    }
                }

                System.out.println();

                for (int j = 1; j <= amigoB-1; j++) {
                    if (amigoB % j == 0) {
                        contadorB = contadorB + j;
                        System.out.println("División: " + amigoB + " % " + j + " = " + contadorB);
                    }
                }

                System.out.println();

                if (contadorA == amigoB && contadorB == amigoA) {
                    System.out.println("Sí son amigos");
                }
                else {
                    System.out.println("No son amigos");
                }
            }
        }
    }
