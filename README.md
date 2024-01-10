# midtermjava
import java.time.LocalDate;
import java.time.format.DateTimeFormatter;
import java.util.Scanner;

public class ShortDateConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a short date (YYYY-MM-DD): ");
        String shortDate = scanner.nextLine();
        DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");
        LocalDate date = LocalDate.parse(shortDate, formatter);
        String monthName = date.getMonth().name();
        monthName = monthName.substring(0, 1).toUpperCase() + monthName.substring(1).toLowerCase();
        int day = date.getDayOfMonth();
        int year = date.getYear();
        String fullDate = monthName + " " + day + ", " + year;
        System.out.println("Full date representation: " + fullDate);
    }
}






2.
class Rectangle {
    protected double length;
    protected double width;

    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    public double getArea() {
        return length * width;
    }

    public double getPerimeter() {
        return 2 * (length + width);
    }
}

class Square extends Rectangle {
    public Square(double side) {
        super(side, side);
    }
}


