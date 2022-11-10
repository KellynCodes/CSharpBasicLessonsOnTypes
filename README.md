# CSharpBasicLessonsOnTypes
```C#
using System;
using System.Collections.Generic;
using System.Collections;
using System.Text;
using System.Threading.Tasks;
using System.Linq;

namespace CodeTester
{
    class Squares
    {
        public static void Main(string[] args)
        {
            int i = 0;
            int j;
            while (i < 10)
            {
                j = i * i;
                Console.WriteLine($"{i} x {i} = {j}");
                i++;
            }

            //BELOW ARE CODES FOR WORKING WITH STRINGS  
            //Values of  varibles can be changed
            string aFriend = "Bill";
            Console.WriteLine(aFriend);
            aFriend = "Maira";
            Console.WriteLine(aFriend);

            string firstFriend = "Maria";
            string secondFriend = "Sage";
            Console.WriteLine($"My friends are {firstFriend} and {secondFriend}");
            Console.WriteLine($"The name {firstFriend} has {firstFriend.Length} letters.");
            Console.WriteLine($"The name {secondFriend} has {secondFriend.Length} letters.");

            //triming empty spaces with Trim();
            string greeting = "      Hello World!       ";
            Console.WriteLine($"[{greeting}]");

            string trimmedGreeting = greeting.TrimStart();
            Console.WriteLine($"[{trimmedGreeting}]");

            trimmedGreeting = greeting.TrimEnd();
            Console.WriteLine($"[{trimmedGreeting}]");

            trimmedGreeting = greeting.Trim();
            Console.WriteLine($"[{trimmedGreeting}]");

            //Replacing a word with another using the Replace Keyword;
            string sayHello = "Hello World!";
            Console.WriteLine(sayHello);
            sayHello = sayHello.Replace("Hello", "Greetings");
            Console.WriteLine(sayHello);

            //Changing text case
            Console.WriteLine(sayHello.ToUpper());
            Console.WriteLine(sayHello.ToLower());

            //checking if sentence contains a letter or word: returns true OR false;
            string songLyrics = "You say goodbye, and I say hello";
            Console.WriteLine(songLyrics.Contains("goodbye")); // returns true;
            Console.WriteLine(songLyrics.Contains("greetings")); //returns false;
            Console.WriteLine(songLyrics.Contains("s")); // return true;

            //CHALLENGE AFTER THE LESSON
            string _string = "come here immediately";
            Console.WriteLine(_string.StartsWith("come")); // prints True;
            Console.WriteLine(_string.EndsWith("here")); // Prints False;

            //WORKING WITH NUMBERS;
            int a = 18;
            int b = 6;
            int c = a * b;
            Console.WriteLine(c);

            int _five = 5;
            int _four = 4;
            int _two = 2;
            int _TotalArr = _five + _four * _two;
            Console.WriteLine(_TotalArr); //The answer will be 13 because of BODMAS

            //adding parenthensis to the operation you want to run first
            int _TotalArrParam = (_five + _four) * _two; //Here the answer will be 18;
            Console.WriteLine(_TotalArrParam);

            //combining many different operations
            int d = (a + b) - 6 * c + (12 * 4) / 3 + 12;
            Console.WriteLine(d); // Here the answer will be -596;

            //             You may have noticed an interesting behavior for integers.Integer division always produces an integer result, even when you'd expect the result to include a decimal or fractional portion.

            // If you haven't seen this behavior, try the following code
            int seven = 7;
            int four = 4;
            int three = 3;
            int theTotal = (seven + four) / three;
            Console.WriteLine(theTotal); //This is surposed to return decimals but integers do not return decimals

            // The C# integer type differs from mathematical integers in one other way: the int type has minimum and maximum limits. Run this code in the interactive window to see those limits:
            int max = int.MaxValue;
            int min = int.MinValue;
            Console.WriteLine($"The range of integers is {min} to {max}"); //Print Out the mimimum and maximum value of integers in c#

            // If a calculation produces a value that exceeds those limits, you have an underflow or overflow condition. The answer appears to wrap from one limit to the other.Add these two lines to the interactive window to see an example:
            int overflow = max + 3;
            Console.WriteLine($"An example of overflow: {overflow}");
            int underflow = min + 3;
            Console.WriteLine($"An example of underflow: {underflow}");

            //Printing the range of double;
            double doubleMax = double.MaxValue;
            double doubleMin = double.MinValue;
            Console.WriteLine($"The range of double is {doubleMin} to {doubleMax}");

            //Printing the range of double;
            decimal decimalMin = decimal.MinValue;
            decimal decimalMax = decimal.MaxValue;
            Console.WriteLine($"The range of the decimal type is {decimalMin} to {decimalMax}");
            // Notice that the range is smaller than the double type. You can see the greater precision with the decimal type by trying the following code:

            //Working with the difference between double and decimal in C#endregion
            double doubleA = 1.0;
            double doubleB = 3.0;
            Console.WriteLine(doubleA / doubleB);

            decimal decimalC = 1.0M;
            decimal decimalD = 3.0M;
            Console.WriteLine(decimalC / decimalD);

            //LESSON CHALLENGE
            // # Question: Now that you've seen the different numeric types, write code that calculates the area of a circle whose radius is 2.50 centimeters. Remember that the area of a circle is the radius squared multiplied by PI. One hint: .NET contains a constant for PI, Math.PI that you can use for that value. Math.PI, like all constants declared in the System.Math namespace, is a double value. For that reason, you should use double instead of decimal values for this challenge.

            //             You should get an answer between 19 and 20.

            double radiusOfACircle = 2.50;
            double Area = Math.Pow(radiusOfACircle, 2) * Math.PI;
            Console.WriteLine(Area);
        }

    }
}
```
