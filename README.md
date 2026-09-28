topic : Drug-detector-robot


import java.util.Scanner;

public class DrugDetectorRobot {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int sensorValue;
        int threshold = 500;

        System.out.println("================================");
        System.out.println("     DRUG DETECTOR ROBOT");
        System.out.println("================================");
        System.out.println("Robot Started...");
        System.out.println("Robot is moving forward.");

        while (true) {

            System.out.print("\nEnter sensor value (0-1023): ");
            sensorValue = sc.nextInt();

            if (sensorValue >= threshold) {

                System.out.println("\n⚠ ALERT!");
                System.out.println("Suspicious substance detected!");
                System.out.println("Robot stopped.");
                System.out.println("Buzzer: ON");
                System.out.println("LED: ON");

                break;

            } else {

                System.out.println("No suspicious substance detected.");
                System.out.println("Robot continues moving...");
                System.out.println("Buzzer: OFF");
                System.out.println("LED: OFF");
            }
        }

        sc.close();
    }
}
