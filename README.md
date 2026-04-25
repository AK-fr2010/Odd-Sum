# Odd-Sum

    import java.util.Scanner;
     public class Main {
      public static void main(String[] args) {
        Scanner scanner = new Scanner (System.in);

        int total = 0 ;

        System.out.print("Enter the Lower Limit of The No.s you want to Add :");
        int lowerLimit = scanner.nextInt();

        System.out.print("Enter the Upper Limit of The No.s you want to Add :");
        int upperLimit = scanner.nextInt();

        if (lowerLimit < upperLimit) {
            if (lowerLimit % 2 == 1) {
                for (int i = lowerLimit; i <= upperLimit; i= i + 2) {
                    total = total + i;
                    System.out.println("The No. is ->" + i + "\nTotal -> " + total);
                }
            }
            if (lowerLimit % 2 == 0) {
                for (int i = lowerLimit + 1; i <= upperLimit; i+=2) {
                    total+= i;
                    System.out.println("The No. is ->" + i + "\nTotal -> " + total);
                }
            }
        }
        else if (lowerLimit > upperLimit) {
            System.out.println("The Lower Limit exceeds the Upper Limit . Please Try Again");
        }
        else {
            System.out.println("The Lower Limit is equal to the Upper Limit . Please Try Again");
        }
        scanner.close();
    }
    }
