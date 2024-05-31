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

import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        // Create a new ArrayList instance
        ArrayList<String> list = new ArrayList<>();

        // Add elements to the ArrayList
        list.add("Apple");
        list.add("Banana");
        list.add("Orange");
        System.out.println("Initial list: " + list);  // Output: [Apple, Banana, Orange]

        // Get the size of the ArrayList
        System.out.println("Size of list: " + list.size());  // Output: 3

        // Access an element at a specific index
        String fruit = list.get(1);  // Index starts from 0
        System.out.println("Element at index 1: " + fruit);  // Output: Banana

        // Update an element at a specific index
        list.set(1, "Blueberry");
        System.out.println("Updated list: " + list);  // Output: [Apple, Blueberry, Orange]

        // Remove an element by index
        list.remove(2);  // Removes "Orange"
        System.out.println("List after removal: " + list);  // Output: [Apple, Blueberry]

        // Check if the list contains a specific element
        boolean containsApple = list.contains("Apple");
        System.out.println("Contains 'Apple': " + containsApple);  // Output: true

        // Iterate over the elements in the ArrayList
        System.out.print("Iterating over list: ");
        for (String item : list) {
            System.out.print(item + " ");
        }
        // Output: Apple Blueberry

        // Clear all elements from the ArrayList
        list.clear();
        System.out.println("\nList after clearing: " + list);  // Output: []
    }
}
