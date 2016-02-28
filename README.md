# ArrayStas

import java.util.Random;
import java.util.Arrays;

public class ArrayStas 
{
	

	public static void main(String[] args)
	{
		int array[] = new int[300];
		Random rand = new Random();
		
		for (int i = 0; i < array.length; i++)
		{
		    array[i] = rand.nextInt(100) + 1;
		}
		Arrays.sort(array);
	
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
		int value3prime = (value3 - value2 - value1);
		
		int stop4 = 81;
		int value4 = Arrays.binarySearch(array , stop4);
		int value4prime = (value4 - value3 - value2 -value1);
		
		int value5 = (300 - value4prime);
		
		
		
	System.out.println("-------------------------------------------------");
	
	//This prints out bar chart for 1-20
	System.out.println();
	System.out.print("1 - 20: ");
	for (int i = 0; i <= array.length - 1; i++)
	{
	 if ((array[i] >= 1) && (array[i] <= 20))
			 {
		 System.out.print("*");
			 }
	}
	System.out.print("  " + value1);
	
	//This prints out bar chart for 21-40 
	 System.out.println();
	 System.out.print("21 - 40: "); 
	 for (int i = 0; i <= array.length - 1; i++)
	 {
	 if ((array[i] >= 21) && (array[i] <= 40))
	 {
		 System.out.print("*");
	 }
	 }
	 System.out.print("  " + (value2prime));
	 
	 //This prints out bar chart for 41-60
	 System.out.println();
	 System.out.print("41 - 60: "); 
	 for (int i = 0; i <= array.length - 1; i++)
	 {
	 if ((array[i] >= 41) && (array[i] <= 60))
	 {
		 System.out.print("*");
	 }
	 }
	  System.out.print("  " + (value3prime));
	 
	 //This prints out bar chart for 61-80
	 System.out.println();
	 System.out.print("61 - 68: "); 
	 for (int i = 0; i <= array.length - 1; i++)
	 {
	 if ((array[i] >= 61) && (array[i] <= 80))
	 {
		 System.out.print("*");
	 }
	 }
	 System.out.print("  " + (value4prime));
	 
	//This prints out bar chart for 81-100
		 System.out.println();
		 System.out.print("81 - 100: "); 
		 for (int i = 0; i <= array.length - 1; i++)
		 {
		 if ((array[i] >= 81) && (array[i] <= 100))
		 {
			 System.out.print("*");
		 }
		 }
		 System.out.print("  " + (value5));
	}
	
	
	
	}
