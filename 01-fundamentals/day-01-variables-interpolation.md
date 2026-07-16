Day 1 — Write Your First C# Code
Module: Write your first C# code (MS Learn) — 88% complete
Path: Write your first code using C# (Get started with C#, Part 1) — 25% complete
Concepts Covered
Top-level statements — modern C# console apps don't require an explicit Main() method; execution starts at the top of Program.cs.
Variables & types — declaring variables with explicit types (string, int, double) or with var (type inferred at compile time, not dynamic).
String interpolation vs. concatenation — $"{name} is {age}" vs "text " + variable. Interpolation is the more idiomatic/readable choice.
Console.WriteLine() / Console.ReadLine() — writing output and reading user input as a string.
Operator behavior with mixed types — int + int evaluates numerically before combining with a string (x + y + "!" → 7!, not "5" + "2" + "!").
Semicolons — every statement needs one; a missing semicolon is a compile-time error, not a warning.
Comments — // single-line, /* */ multi-line.
Brief Notes
var is safe for readability but the type is still fixed once inferred — it is not like a loosely-typed variable.
Concatenation (+) and interpolation ($"{}") can produce the same output, but the interviewer/task distinction matters: know which one you're asked for.
Numeric operators are evaluated left-to-right per normal precedence before any string conversion happens.
Assessment
Q1 (MCQ). In a modern C# console app using top-level statements, where does execution start?
A) The Main() method must always be explicitly written
B) The top of Program.cs, no Main() needed
C) Whichever method is marked [EntryPoint]
D) Startup.cs
Q2 (Predict the output).
string name = "Tino";
int age = 21;
Console.WriteLine($"{name} is {age} years old.");
Q3 (Write code). Declare a variable called city of type string, set it to your city, and print it using string interpolation (not concatenation).
Q4 (MCQ). Which is the correct way to store a decimal value like 19.99?
A) int price = 19.99;
B) double price = 19.99;
C) string price = 19.99;
D) bool price = 19.99;
Q5 (Find the bug).
int score = 100
Console.WriteLine("Score: " + score);
Q6 (Predict the output).
int x = 5;
int y = 2;
Console.WriteLine(x + y + "!");
Q7 (Write code). Read a line of input from the user with Console.ReadLine(), store it in a variable called input, and print it back with "You said: " in front of it.
Q8 (True/False). In C#, // starts a single-line comment and /* */ wraps a multi-line comment.