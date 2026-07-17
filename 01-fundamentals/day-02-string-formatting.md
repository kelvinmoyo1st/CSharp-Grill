Day 2 — Perform Basic String Formatting in C#
Module: Perform basic string formatting in C# (MS Learn)
Path: Write your first code using C# (Get started with C#, Part 1) — 45% complete
Concepts Covered
Composite formatting — string.Format() with positional placeholders ({0}, {1}).
Format specifiers — letters inside {value:X} that control how a value is displayed (currency, number, fixed-point, etc.).
Alignment — {value,width} pads a value to a minimum column width.
Escape sequences / literal braces — remembering the $ prefix is what turns {} into interpolation; without it, braces print literally.
Brief Notes
$"{}" (interpolation) and string.Format() (composite formatting) do the same job — interpolation is just more readable and is the modern default.
Format specifiers are not decimal-place shortcuts by default — each letter has a distinct meaning:
C → currency (culture-dependent, e.g. $19.99)
N → number with thousands separators, fixed decimals (N2 → 12,345.68)
F → fixed-point decimal places (F2 → 36.58)
D → integer formatting only (not decimals, not currency)
P → percentage
{value:00} is zero-padding for whole numbers, not a decimal-place control — e.g. {7:00} → 07.
{value,width} controls column alignment/padding (right-aligned by default for numbers), not an error — e.g. {42,6} → "    42".
Forgetting the $ before a string with {} in it is a common bug — the braces just print literally instead of interpolating.
:C formatting follows the system/current culture unless a specific CultureInfo is passed explicitly.
Assessment
Q1 (MCQ). Which produces "Price: $19.99" given decimal price = 19.99m;?
A) Console.WriteLine("Price: " + price);
B) Console.WriteLine($"Price: {price:C}");
C) Console.WriteLine($"Price: {price:D}");
D) Console.WriteLine("Price: {price}");
Q2 (Predict the output).
int score = 7;
Console.WriteLine($"Score: {score:00}");
Q3 (Write code). Given double temp = 36.5789;, print it rounded to 2 decimal places using interpolation.
Q4 (MCQ). What does the N format specifier do, e.g. {value:N2}?
A) Formats as a percentage
B) Formats as a number with thousands separators and fixed decimal places
C) Converts to a string explicitly
D) Formats as scientific notation
Q5 (Find the bug).
string name = "Tino";
Console.WriteLine("Hello, {name}!");
Q6 (Predict the output).
int value = 42;
Console.WriteLine($"{value,6}");
Q7 (Write code). Using composite formatting (not interpolation), print "Name: Tino, Age: 21" using string.Format().
Q8 (True/False). $"{price:C}" will always format as US dollars, regardless of the system's locale/culture settings.
