# avaliacao1
primeira avaliacao da mentoria
import java.util.Scanner;

public class SistemaEscolar {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        double[] notas = new double[8];

        // Entrada das 8 notas
        for (int i = 0; i < 8; i++) {
            System.out.print("Digite a " + (i + 1) + "ª nota: ");
            notas[i] = scanner.nextDouble();
        }

        // Cálculo das médias bimestrais
        double b1 = (notas[0] + notas[1]) / 2;
        double b2 = (notas[2] + notas[3]) / 2;
        double b3 = (notas[4] + notas[5]) / 2;
        double b4 = (notas[6] + notas[7]) / 2;

        // Cálculo das médias semestrais
        double s1 = (b1 + b2) / 2;
        double s2 = (b3 + b4) / 2;

        // Média final
        double mediaFinal = (s1 + s2) / 2;

        // Saída formatada
        System.out.println("\n----- RESULTADOS -----");
        System.out.println("1º Bimestre: " + b1);
        System.out.println("2º Bimestre: " + b2);
        System.out.println("1º Semestre: " + s1);
        System.out.println("----------------------");
        System.out.println("3º Bimestre: " + b3);
        System.out.println("4º Bimestre: " + b4);
        System.out.println("2º Semestre: " + s2);
        System.out.println("----------------------");
        System.out.println("Média Final: " + mediaFinal);

        scanner.close();
    }
}
