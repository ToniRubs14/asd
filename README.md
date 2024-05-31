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


public class StringBuilderExample {
    public static void main(String[] args) {
        // Create a new StringBuilder instance
        StringBuilder sb = new StringBuilder();

        // Append strings to the StringBuilder
        sb.append("Hello, ").append("world!");
        System.out.println(sb.toString());  // Output: Hello, world!

        // Get the length of the current string
        System.out.println(sb.length());  // Output: 13

        // Insert a string at a specific index
        sb.insert(7, "beautiful ");
        System.out.println(sb.toString());  // Output: Hello, beautiful world!

        // Delete a portion of the string
        sb.delete(7, 16);
        System.out.println(sb.toString());  // Output: Hello, world!

        // Clear the StringBuilder
        sb.setLength(0);
        System.out.println(sb.toString());  // Output: (empty string)
    }
}
