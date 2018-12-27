# SchoolTrip
import java.util.Scanner;

public class P02_SchoolTrip {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        int numberDaysMissing = Integer.parseInt(scanner.nextLine());
        int leftFoodInKilos = Integer.parseInt(scanner.nextLine());
        double foodPerDayFirstDog = Double.parseDouble(scanner.nextLine());
        double foodPerDaySecondDog = Double.parseDouble(scanner.nextLine());
        double foodPerDayThirdDog = Double.parseDouble(scanner.nextLine());

        double eatenFoodPerDay =  (foodPerDayFirstDog + foodPerDaySecondDog + foodPerDayThirdDog);
        double remainingFood = leftFoodInKilos - (numberDaysMissing * eatenFoodPerDay);

        if (remainingFood >= 0){
            System.out.printf("%.0f kilos of food left.",Math.floor(remainingFood));
        }
        else {
            System.out.printf("%.0f more kilos of food are needed.",Math.ceil(Math.abs(remainingFood)));
        }
    }
}
