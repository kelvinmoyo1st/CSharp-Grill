Day 5 — Weighted Average (GPA Calculation)
Module: GPA / weighted average coding exercise
Path: Write your first code using C# (Get started with C#, Part 1)
Concepts Covered
Weighted averages — combining multiple values (grades) with different weights (credit hours) rather than a simple average.
Automatic type promotion in mixed expressions — when a double operand is already present anywhere in a chain of */+, the whole calculation is promoted, even if other operands are int.
Formatting a double for display — raw double values print with many digits; :F2 trims to a clean, human-readable form.
Brief Notes
Weighted average formula: (value1*weight1 + value2*weight2 + ...) / (weight1 + weight2 + ...) — classes/values worth more weight (credits) have proportionally more influence on the result.
Key distinction from earlier casting bugs: a cast is only needed when all operands in an expression are int. If even one operand is already double (e.g. grade1 in grade1 * credits1), that sub-expression is automatically promoted to double — no explicit cast required.
Checklist before assuming a cast is needed: scan the expression for at least one double operand first.
Dividing a double numerator by an int denominator (doubleValue / intValue) still produces a double result — division only truncates when both sides are int.
Raw double output from Console.WriteLine can print far more digits than expected (e.g. 3.4285714285714284) — this is why explicit formatting (:F2, etc.) matters for anything user-facing.
Assessment
Q1 (Write code). Given int credits1 = 3, credits2 = 4; and double grade1 = 4.0, grade2 = 3.0;, calculate the weighted GPA: (grade1*credits1 + grade2*credits2) / (credits1 + credits2). Store it in double gpa.
Q2 (Predict the output).
int credits1 = 3, credits2 = 4;
double grade1 = 4.0, grade2 = 3.0;
double gpa = (grade1 * credits1 + grade2 * credits2) / (credits1 + credits2);
Console.WriteLine(gpa);
Q3 (MCQ). Why is a weighted average (by credit hours) more accurate for GPA than a simple average of grades?
A) It isn't — simple average is always correct
B) It accounts for classes worth more credit having more influence on the final GPA
C) It avoids integer division bugs
D) It's only needed when grades are letters, not numbers
Q4 (Write code). Print gpa from Q1 formatted to exactly 2 decimal places.
Q5 (Find the bug).
int credits1 = 3;
int credits2 = 4;
double grade1 = 4.0;
double grade2 = 3.0;
double gpa = (grade1 * credits1 + grade2 * credits2) / (credits1 + credits2);
there a bug here? Is the division safe from truncation?
Q6 (Predict the output).
double gpa = 3.6666667;
Console.WriteLine($"Your GPA is {gpa:F2}");
Q7 (MCQ). If credits1 + credits2 were both int and the numerator were also purely int (no double anywhere), what would happen to the GPA calculation?
A) Nothing changes, C# always keeps decimals
B) Compile error
C) The result truncates to a whole number before it's ever stored, even in a double variable
D) It rounds to the nearest whole number
Q8 (True/False). In (grade1*credits1 + grade2*credits2) / (credits1 + credits2), if grade1 and grade2 are double but credits1 and credits2 are int, the whole expression still safely produces a double result.
