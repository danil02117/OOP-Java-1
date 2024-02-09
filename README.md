import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введите количество строк: ");
        int n = scanner.nextInt();
        scanner.nextLine();

        String[] strings = new String[n];
        for (int i = 0; i < n; i++) {
            System.out.print("Введите строку " + (i + 1) + ": ");
            strings[i] = scanner.nextLine();
        }

        int totalLength = 0;

        for (String string : strings) {
            totalLength += string.length();
        }

        double averageLength = (double) totalLength / n;

        System.out.println("Строки, длина которых меньше средней:");
        for (String string : strings) {
            if (string.length() < averageLength) {
                System.out.println(string + " (" + string.length() + " символов)");
            }
        }
    }
}
