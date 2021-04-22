## Algorithm to convert Roman Numerals to Integer Number:  ##

  1. Split the Roman Numeral string into Roman Symbols (character).
  2. Convert each symbol of Roman Numerals into the value it represents.
  3. Take symbol one by one from starting from index 0: 
      1. If current value of symbol is greater than or equal to the value of next symbol, then add this value to the running total.
      2. else subtract this value **by adding the value of next symbol** to the running total.
      
  
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
  
  
  ### Program ###
  
  ```
  // C# Program to convert Roman
// Numerals to Numbers
using System;

class GFG {
	// This function returns value
	// of a Roman symbol
	public virtual int value(char r)
	{
		if (r == 'I')
			return 1;
		if (r == 'V')
			return 5;
		if (r == 'X')
			return 10;
		if (r == 'L')
			return 50;
		if (r == 'C')
			return 100;
		if (r == 'D')
			return 500;
		if (r == 'M')
			return 1000;
		return -1;
	}

	// Finds decimal value of a
	// given romal numeral
	public virtual int romanToDecimal(string str)
	{
		// Initialize result
		int res = 0;

		for (int i = 0; i < str.Length; i++)
		{
			// Getting value of symbol s[i]
			int s1 = value(str[i]);

			// Getting value of symbol s[i+1]
			if (i + 1 < str.Length)
			{
				int s2 = value(str[i + 1]);

				// Comparing both values
				if (s1 >= s2)
				{
					// Value of current symbol is greater
					// or equalto the next symbol
					res = res + s1;
				}
				else
				{
					res = res + s2 - s1;
					i++; // Value of current symbol is
					// less than the next symbol
				}
			}
			else {
				res = res + s1;
				i++;
			}
		}

		return res;
	}

	// Driver Code
	public static void Main(string[] args)
	{
		GFG ob = new GFG();

		// Considering inputs given are valid
		string str = "MCMIV";
		Console.WriteLine("Integer form of Roman Numeral"
						+ " is "
						+ ob.romanToDecimal(str));
	}
}

```
