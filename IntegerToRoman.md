## Algorithm to convert decimal number to Roman Numeral  ##

|SYMBOL       |VALUE|
|-------------|-----|
|I             |1|
|IV            |4|
|V             |5|
|IX            |9|
|X             |10|
|XL            |40|
|L             |50|
|XC            |90|
|C             |100|
|CD            |400|
|D             |500|
|CM            |900|
|M             |1000|

Compare given number with base values in the order 1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1. 
Base value which is just smaller or equal to the given number will be the initial base value (largest base value) .
Divide the number by its largest base value, the corresponding base symbol will be repeated quotient times, 
  the remainder will then become the number for future division and repetitions.
The process will be repeated until the number becomes zero.

** Explanation: **

**Step 1**

Initially number = 3549
Since 3549 >= 1000 ; largest base value will be 1000 initially.
Divide 3549/1000. Quotient = 3, Remainder =549. The corresponding symbol M will be repeated thrice.

**Step 2**

Now, number = 549
1000 > 549 >= 500 ; largest base value will be 500.
Divide 549/500. Quotient = 1, Remainder =49. The corresponding symbol D will be repeated once.

**Step 3**

Now, number = 49
50 > 49 >= 40 ; largest base value is 40.
Divide 49/40. Quotient = 1, Remainder = 9. The corresponding symbol XL will be repeated once.

**Step 4**

Now, number = 9
10> 9 >= 9 ; largest base value is 9.
Divide 9/9. Quotient = 1, Remainder = 0. The corresponding symbol IX will be repeated once.

**Step 5**

Finally number becomes 0, algorithm stops here.
Output obtained MMMDXLIX.

### Program ###

```
// C# Program to convert decimal number
// to roman numerals
using System;
class GFG
{

// To add corresponding base symbols in the
// array to handle cases which follow subtractive
// notation. Base symbols are added index 'i'.
static int sub_digit(char num1, char num2,
						int i, char[] c)
{
	c[i++] = num1;
	c[i++] = num2;
	return i;
}

// To add symbol 'ch' n times after index i in c[]
static int digit(char ch, int n, int i, char[] c)
{
	for (int j = 0; j < n; j++)
	{
		c[i++] = ch;
	}
	return i;
}

// Function to convert decimal to Roman Numerals
static void printRoman(int number)
{
	char[] c = new char[10001];
	int i = 0;

	// If number entered is not valid
	if (number <= 0)
	{
		Console.WriteLine("Invalid number");
		return;
	}

	// TO convert decimal number to
	// roman numerals
	while (number != 0)
	{
		// If base value of number is
		// greater than 1000
		if (number >= 1000)
		{
			// Add 'M' number/1000 times after index i
			i = digit('M', number / 1000, i, c);
			number = number % 1000;
		}
		
		// If base value of number is greater
		// than or equal to 500
		else if (number >= 500)
		{
			// To add base symbol to the character array
			if (number < 900)
			{
				
				// Add 'D' number/1000 times after index i
				i = digit('D', number / 500, i, c);
				number = number % 500;
			}
			
			// To handle subtractive notation in case
			// of number having digit as 9 and adding
			// corresponding base symbol
			else
			{
				
				// Add C and M after index i/.
				i = sub_digit('C', 'M', i, c);
				number = number % 100;
			}
		}
		
		// If base value of number is greater
		// than or equal to 100
		else if (number >= 100)
		{
			// To add base symbol to the character array
			if (number < 400)
			{
				i = digit('C', number / 100, i, c);
				number = number % 100;
			}
			
			// To handle subtractive notation in case
			// of number having digit as 4 and adding
			// corresponding base symbol
			else
			{
				i = sub_digit('C', 'D', i, c);
				number = number % 100;
			}
		}
		
		// If base value of number is greater
		// than or equal to 50
		else if (number >= 50)
		{
			
			// To add base symbol to the character array
			if (number < 90)
			{
				i = digit('L', number / 50, i, c);
				number = number % 50;
			}
			
			// To handle subtractive notation in case
			// of number having digit as 9 and adding
			// corresponding base symbol
			else
			{
				i = sub_digit('X', 'C', i, c);
				number = number % 10;
			}
		}
		
		// If base value of number is greater
		// than or equal to 10
		else if (number >= 10)
		{
			
			// To add base symbol to the character array
			if (number < 40)
			{
				i = digit('X', number / 10, i, c);
				number = number % 10;
			}
			
			// To handle subtractive notation in case of
			// number having digit as 4 and adding
			// corresponding base symbol
			else
			{
				i = sub_digit('X', 'L', i, c);
				number = number % 10;
			}
		}
		
		// If base value of number is greater
		// than or equal to 5
		else if (number >= 5)
		{
			if (number < 9)
			{
				i = digit('V', number / 5, i, c);
				number = number % 5;
			}
			
			// To handle subtractive notation in case
			// of number having digit as 9 and adding
			// corresponding base symbol
			else
			{
				i = sub_digit('I', 'X', i, c);
				number = 0;
			}
		}
		
		// If base value of number is greater
		// than or equal to 1
		else if (number >= 1)
		{
			if (number < 4)
			{
				i = digit('I', number, i, c);
				number = 0;
			}
			
			// To handle subtractive notation in
			// case of number having digit as 4
			// and adding corresponding base symbol
			else
			{
				i = sub_digit('I', 'V', i, c);
				number = 0;
			}
		}
	}

	// Printing equivalent Roman Numeral
	Console.WriteLine("Roman numeral is: ");
	for (int j = 0; j < i; j++)
	{
		Console.Write("{0}", c[j]);
	}
}

// Driver Code
public static void Main()
{
	int number = 3549;

	printRoman(number);
}
}

// This code is contributed by Rajput-Ji

```
