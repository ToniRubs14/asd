import java.time.LocalTime;
import java.time.format.DateTimeFormatter;

public class TimeConverter {
    public static void main(String[] args) {
        // Example military time
        String militaryTime = "14:35";

        // Convert military time to LocalTime
        LocalTime time = LocalTime.parse(militaryTime);

        // Define formatter for 12-hour format with AM/PM
        DateTimeFormatter formatter = DateTimeFormatter.ofPattern("hh:mm a");

        // Format the time
        String normalTime = time.format(formatter);

        // Print the result
        System.out.println("Military time: " + militaryTime);
        System.out.println("Normal time: " + normalTime);
    }
}
