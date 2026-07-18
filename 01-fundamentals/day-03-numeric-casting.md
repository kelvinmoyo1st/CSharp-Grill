Day 3 — Numeric Operations & Type Casting
Module: Perform basic operations on numbers in C# (MS Learn)
Path: Write your first code using C# (Get started with C#, Part 1)
Concepts Covered
Mathematical operations on numeric values — +, -, *, / across int and double.
Implicit type conversion between strings and numeric values (e.g. + overloaded for concatenation vs. addition).
Explicit casting — temporarily converting one data type into another, e.g. (double)someInt.
Fahrenheit → Celsius conversion coding challenge, combining arithmetic, casting, and formatted output.
Brief Notes
Integer division truncates. int / int always produces an int result — the decimal portion is dropped, not rounded. 7 / 2 = 3.
Mixed-type math promotes to the wider type. If either operand is a double, the whole expression is evaluated as floating-point. 5 / 2.0 = 2.5, but 5 / 2 = 2.
Order of operations matters with casting. (98 - 32) * 5 / 9 evaluates entirely in int arithmetic if no operand is a double — division truncates before the result is ever assigned to a double variable. Cast early if a fractional result is needed.
Operator overloading: + means numeric addition between numbers, but string concatenation the moment a string is one of the operands — 5 + "5" is "55", not 10.
Casting double → int truncates toward zero, it does not round. (int)19.999 is 19, not 20. Rounding requires a separate call like Math.Round().
Console.WriteLine on a plain double/float doesn't print trailing zeros unless explicitly formatted (e.g. {value:F5}); 36.0 prints as 36.
Declaring a variable and assigning to it are two different steps — a variable needs a type the first time it's introduced (double x = ...;), not just on later assignments.
Assessment
Q1 (MCQ). What is the result of 7 / 2 in C# if both operands are int?
A) 3.5
B) 3
C) 4
D) Compile error
Q2 (Predict the output).
int a = 5;
double b = 2;
Console.WriteLine(a / b);
Q3 (Write code). Given int fahrenheit = 98;, convert it to a double using an explicit cast and store it in a variable called fahrenheitDouble.
Q4 (MCQ). In int x = 5; string y = "5"; var z = x + y; — what happens?
A) Compile error, can't mix int and string
B) z is 10
C) z is "55" — + is overloaded for string concatenation
D) z is 5
Q5 (Find the bug / explain).
int total = 10;
total = total + 5;
total += 5;
Is there a bug here? If not, what does total equal after both lines run?
Q6 (Predict the output).
double celsius = (98 - 32) * 5 / 9;
Console.WriteLine(celsius);
Q7 (Write code). Given double price = 19.999;, cast it to an int and print the result. What happens to the decimal portion?
Q8 (True/False). Casting a double to an int in C# rounds to the nearest whole number