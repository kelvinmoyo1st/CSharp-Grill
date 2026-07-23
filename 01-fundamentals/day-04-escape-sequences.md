Day 4 — Guided Project: Calculate & Print Student Grades
Module: Guided project - Calculate and print student grades (MS Learn) — Module assessment passed
Path: Write your first code using C# (Get started with C#, Part 1)
Concepts Covered
Breaking a program into smaller steps — calculating sum before average, rather than one long expression.
Choosing appropriate data types for intermediate results (e.g. int for a sum of whole scores, double for an average that may have decimals).
Mathematical operations to determine results — sum and average of test scores.
Escaped character sequences — \t (tab), \n (newline), \" (literal quote), \\ (literal backslash) — and formatting console output with them.
Brief Notes
Averaging whole numbers is a classic integer-division trap: (score1 + score2 + score3) / 3 stays int division and truncates unless at least one operand is explicitly cast to double — e.g. (double)sum / 3. Casting only the divisor or only the sum both work, since either one being double promotes the whole expression.
Escape sequences let you embed characters that would otherwise break or be unrepresentable in a string literal:
\t → tab
\n → newline
\" → literal double-quote
\\ → literal backslash
Precision matters in exact output. Small things — a missing colon, an extra space, a misplaced escape character — are easy to lose track of mentally. Worth "typing out" the exact expected string character-by-character rather than approximating.
Breaking work into named intermediate variables (sum → average) isn't just for readability — it also controls where type promotion/casting happens, and makes bugs easier to isolate.
Assessment
Q1 (Write code). Given three test scores int score1 = 85, score2 = 90, score3 = 78;, calculate their sum and store it in int sum.
Q2 (Write code). Using sum from Q1, calculate the average as a double (not truncated to an int) and store it in average.
Q3 (Predict the output).
Console.WriteLine("Name:\tTino\nGrade:\tA");
Q4 (MCQ). Which escape sequence inserts a literal double-quote character inside a string?
A) \'
B) \"
C) \\
D) \q
Q5 (Find the bug).
int score1 = 85;
int score2 = 90;
int score3 = 78;
double average = (score1 + score2 + score3) / 3;
Console.WriteLine(average);
Q6 (Predict the output).
Console.WriteLine("Path: C:\\Users\\Tino");
Q7 (Write code). Print He said "C# is fun" to the console, correctly escaping the quotes.
Q8 (True/False). Breaking a program into smaller named variables/steps (like calculating sum before average) has no real benefit besides readability — the compiler treats it identically to one long expression either way.
