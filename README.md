# ArrayStas
import java.util.Random;
import java.util.Arrays;

public class ArrayStas 
{
	

	public static void main(String[] args)
	{
		int array[] = new int[300]; //makes an array of size 300
		Random rand = new Random(); //initializes a variable to be a random number
		
		for (int i = 0; i < array.length; i++) //loops through the same amount of times as the array's size
		{
		    array[i] = rand.nextInt(100) + 1; //makes the integers of the array all random, up to a value of 100
		}
		Arrays.sort(array); //sorts it in ascending order
	
		// This prints the sorted array
		for (int i = 0; i <= array.length - 1; i++) 
		{
		System.out.println(array[i]); 
		}
		
		//This initializes some values for the method that makes the bar chart
		//and counts the number of occurrences of numbers in the various ranges 
		int stop1 = 21;
		int value1 = Arrays.binarySearch(array , stop1);
		
		int stop2 = 41;
		int value2 = Arrays.binarySearch(array , stop2);
		int value2prime = (value2-value1);
		
		int stop3 = 61;
		int value3 = Arrays.binarySearch(array , stop3);
		int value3prime = (value3 - value2);
		
		int stop4 = 81;
		int value4 = Arrays.binarySearch(array , stop4);
		int value4prime = (value4 - value3);
		
		int value5 = (300 - value4);
		
		
		
	System.out.println("-------------------------------------------------"); //just a visual separator
	
	//This makes and prints out bar chart for 1-20
	System.out.println();
	System.out.print("1 - 20: ");
	for (int i = 0; i <= array.length - 1; i++)
	{
	 if ((array[i] >= 1) && (array[i] <= 20))
			 {
		 System.out.print("*");
			 }
	}
	System.out.print("  " + value1); //prints out the number of occurrences of integers in the range 1 - 20
	
	//This makes and prints out bar chart for 21-40 
	 System.out.println();
	 System.out.print("21 - 40: "); 
	 for (int i = 0; i <= array.length - 1; i++)
	 {
	 if ((array[i] >= 21) && (array[i] <= 40))
	 {
		 System.out.print("*");
	 }
	 }
	 System.out.print("  " + (value2prime)); //prints out the number of occurrences of integers in the range 21-40
	 
	 //This makes and prints out bar chart for 41-60
	 System.out.println();
	 System.out.print("41 - 60: "); 
	 for (int i = 0; i <= array.length - 1; i++)
	 {
	 if ((array[i] >= 41) && (array[i] <= 60))
	 {
		 System.out.print("*");
	 }
	 }
	  System.out.print("  " + (value3prime)); //prints out the number of occurrences of integers in the range 41-60
	 
	 //This makes and prints out bar chart for 61-80
	 System.out.println();
	 System.out.print("61 - 68: "); 
	 for (int i = 0; i <= array.length - 1; i++)
	 {
	 if ((array[i] >= 61) && (array[i] <= 80))
	 {
		 System.out.print("*");
	 }
	 }
	 System.out.print("  " + (value4prime)); //prints out the number of occurrences of integers in the range 61-80
	 
	//This makes and prints out bar chart for 81-100
		 System.out.println();
		 System.out.print("81 - 100: "); 
		 for (int i = 0; i <= array.length - 1; i++)
		 {
		 if ((array[i] >= 81) && (array[i] <= 100))
		 {
			 System.out.print("*");
		 }
		 }
		 System.out.print("  " + (value5)); //prints out the number of occurrences of integers in the range 81-100
	}
	
	
	
	}
