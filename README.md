//arrey_class using conditional veriables//

import java.util.Scanner;
import java.util.Arrays;

public class NumberOrder 
{
    public static void main(String[] args) 
    {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int size = input.nextInt();

        int[] numbers = new int[size];

        System.out.println("Enter " + size + " numbers:");

        for (int i = 0; i < size; i++) 
        {
            numbers[i] = input.nextInt();
        }

        // Finding the greatest number
        int greatest = numbers[0];
        for (int i = 1; i < size; i++) 
        {
            if (numbers[i] > greatest) 
            {
                greatest = numbers[i];
            }
        }

        // Finding the smallest number
        int smallest = numbers[0];
        for (int i = 1; i < size; i++) 
        {
            if (numbers[i] < smallest) 
            {
                smallest = numbers[i];
            }
        }

        // Sorting the array in ascending order
        Arrays.sort(numbers);

        // Sorting the array in descending order
        int[] descending = new int[size];
        for (int i = 0; i < size; i++) 
        {
            descending[i] = numbers[size - 1 - i];
        }

        System.out.println("Greatest number: " + greatest);
        System.out.println("Smallest number: " + smallest);
        System.out.println("Ascending order: " + Arrays.toString(numbers));
        System.out.println("Descending order: " + Arrays.toString(descending));
    }
}
