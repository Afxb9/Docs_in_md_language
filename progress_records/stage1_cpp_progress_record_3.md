# Stage 1 — Handover / Progress Record

## 1. Overall Stage Status

**Stage 0:** COMPLETE — exit gate passed.

**Stage 1:** In progress.

**Workspace:**

```text
~/Engineering/learning/stage1-foundations/

stage1-foundations/

├── README.md
├── cpp/
├── electronics/
└── python/
```

Current work is primarily in:

```text
cpp/
```

The Stage 1 curriculum remains governed by the Master Curriculum v1.2. Stage completion is based on competency rather than elapsed time, with a normal target workload of approximately **4–5 hours/week**.

---

## 2. Learning Method

Continue using:

**Learn → Predict → Build/Modify → Run/Test → Compare → Explain → Document → Commit**

The learner prefers prediction before execution and practical experiments rather than passive explanation.

Do **not** create exercises merely to fill time.

Exercises should exist because they establish or test a real competency.

---

## 3. C++ Progress

### Experiment 01 — Foundations

Completed.

Covered:

* variables
* `int`
* `double`
* `bool`
* arithmetic/operators
* functions
* arguments
* return values
* Boolean conditions
* prediction before execution

### Experiment 02 — Arguments, References, Addresses

Completed.

Covered:

* pass-by-value
* function-local parameters
* references
* modifying the original variable
* addresses
* basic scope

Important understanding:

```cpp
int x
```

creates a separate parameter/copy.

Whereas:

```cpp
int& x
```

allows the parameter to refer to the original variable.

Also established:

```cpp
&variable
```

gets the variable's address.

Reference and original variable were experimentally shown to have the same address.

### Experiment 03 — Consolidation

Completed and passed.

Tested:

* types
* arithmetic/operators
* functions
* arguments
* return values
* Boolean conditions
* pass-by-value
* references
* modifying original variables
* addresses
* scope
* prediction
* debugging

Important catches were successfully resolved:

* implicit `int → double` conversion
* pass-by-value does not modify caller
* reference does modify caller
* reference/original share the same address
* scope depends on declaration location
* compiler-error debugging

[image](file:////Users/ammarahmed/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image001.png)

## 4. Experiment 04 — Arrays

**Completed / competency checkpoint passed.**

Covered:

```cpp
int sensorReadings[4];
```

Understanding:

```text
int              → element type

sensorReadings   → array name

[4]              → four elements
```

Zero-based indexing:

```text
0 1 2 3
```

Covered:

* array declaration
* initialization
* reading elements
* writing elements
* indexing
* `sizeof`
* calculating element count
* `for` loops
* loop-variable scope
* element addresses
* contiguous memory

Established experimentally:

```text
sizeof(int) = 4 bytes
```

on the current Mac environment.

Therefore:

```cpp
int array[4]
```

= 16 bytes

and adjacent integer elements were observed to be 4 bytes apart.

Also successfully debugged:

```cpp
for (int i = 0, i < 4, i++)
```

versus:

```cpp
for (int i = 0; i < 4; i++)
```

and learned that the loop variable's scope ends with the loop.

## 5. Experiment 05 — C-style Strings

The original Progress Record 2 described this as in progress, but **the actual work in this chat has now substantially completed the intended C-string competency checkpoint.**

Covered and demonstrated:

### Character arrays

```cpp id="p3k6dy"
char name[6] = "Ammar";
```

Memory model:

```text id="zzb7e2"
index:  0  1  2  3  4  5

        A  m  m  a  r  \0
```

Established:

* `char`
* character arrays
* string literals
* null termination
* `'\0'`
* `'\n'`
* `'\r'`
* `0` vs `'0'`
* `4` vs `'4'`
* C strings vs `std::string`
* character-array memory
* `sizeof`
* addresses
* `name`
* `name[0]`
* `&name[0]`
* why `cout` treats `char*` specially
* why casting to `void*` can be used to display the address

Observed:

```text id="d8h5r4"
char = 1 byte
```

on the current platform, with consecutive characters occupying consecutive bytes.

---

## 6. Array-to-Pointer Relationship

Important understanding established:

For ordinary arrays, in most expressions, the array name decays to a pointer to its first element.

Examples:

```text id="x8y5c1"
int array[]    → int*

double array[] → double*

char array[]   → char*
```

So:

```text id="m4y2kn"
name
```

can behave as a pointer to:

```text id="d8j3v6"
&name[0]
```

but:

```text id="2e6csl"
sizeof(name)
```

is an important exception: it operates on the actual array and therefore gives the entire array size.

Established distinction:

```text id="z4q6tw"
name       → array / decays to pointer in most expressions

name[0]    → first element/value

&name[0]   → address of first element
```

---

## 7. Pointer Understanding

Established:

```cpp id="1at6y0"
char* p = name;
```

means:

`p` is a pointer variable storing the address of the first element of `name`.

Then:

```text id="m7s2yr"
*p
```

means:

access the value stored at the address held by `p`.

Therefore:

```text id="x1k4qy"
*p
```

and:

```text id="0xk6bz"
p[0]
```

both produced:

```text id="n8r5dp"
A
```

and:

```text id="b0l6xz"
p[1]
```

produced:

```text id="u7v3qn"
m
```

Also established experimentally:

```text id="xv9k1r"
sizeof(name) → 6

sizeof(p)    → 8

strlen(name) → 5
```

on the current 64-bit Mac.

This distinction is now understood as:

```text id="p8d1mx"
sizeof(array)  → allocated array storage

sizeof(pointer) → pointer storage

strlen(string)  → characters before '\0'
```

---

## 8. C-string Length and Termination

Established:

```cpp id="e4b8tq"
strlen(name)
```

counts characters before the first:

```text id="a0v6kc"
'\0'
```

It does **not** count the terminator.

Example:

```text id="q2z7rm"
A m m a r \0
←── 5 ──→
```

Therefore:

```text id="t6k3hs"
strlen(name) = 5

sizeof(name) = 6
```

Also demonstrated:

```cpp id="5s9fyk"
name[1] = '\0';
```

changes the effective C-string to:

```text id="n1q5av"
A \0 m a r \0
```

and:

```cpp id="k8v2jw"
strlen(name)
```

then returns:

```text id="s4m7pc"
1
```

Important understanding:

A C-string ends at the **first** `'\0'`, even if more bytes physically exist after it.

---

## 9. Experiment 06 — C-string Operations

Created:

```text id="x7d2mk"
cpp/06_c_string_operations.cpp
```

This experiment covered:

### `strlen()`

Measures the C-string length.

### `strcpy()`

Copies the source C-string into the destination, including `'\0'`.

It effectively **replaces the destination C-string**, rather than appending.

Important clarification:

`strcpy()` does **not** necessarily erase the entire destination array.

Example:

Before:

```text id="e5j1hz"
[H][e][l][l][o][1][2][3][\0]...
```

After `strcpy("Ammar")`:

```text id="q9f4sy"
[A][m][m][a][r][\0][2][3][\0]...
```

The old bytes may physically remain, but the new `'\0'` defines where the C-string ends.

---

### `strcat()`

Appends a source C-string to the destination C-string.

Example:

```text id="n3h6xb"
"Hi" + "Ammar"
```

becomes:

```text id="c8m1vt"
"HiAmmar"
```

The destination must have enough free capacity.

---

### `strcmp()`

Compares C-string **contents**.

Important rule:

```text id="k4p8qz"
strcmp(a, b) == 0

    → same contents

strcmp(a, b) < 0

    → a comes before b

strcmp(a, b) > 0

    → a comes after b
```

Do **not** memorize that the non-zero values must specifically be `-1` or `+1`.

---

## 10. C-string Comparison

A critical misconception was corrected.

Given:

```cpp id="a5n8xq"
char a[] = "ON";

char b[] = "ON";
```

this:

```cpp id="z3r7mc"
a == b
```

does **not** perform C-string content comparison.

It produced:

```text id="w6y2pk"
different
```

and Clang warned:

```text id="j9s4vn"
array comparison always evaluates to false
```

Correct content comparison:

```cpp id="r2c6hx"
strcmp(a, b) == 0
```

produced:

```text id="h5v8qa"
same
```

This is particularly important for future Arduino serial-command handling.

## 11. Buffer Capacity / Overflow

A major embedded-systems concept was established.

Example:

```cpp
char source[] = "Ammar123";

char destination[1];

strcpy(destination, source);
```

The program happened to repeatedly print:

```text
Ammar123
```

but this is **undefined behavior**.

The destination only owns one byte, while the source C-string requires:

```text
A m m a r 1 2 3 \0
```

= **9 bytes**.

Important engineering lesson:

A program producing the expected output does not mean the program is correct.

Out-of-bounds writes may:

* appear to work
* corrupt another variable
* produce garbage
* crash
* behave differently after unrelated code changes

This was explicitly connected to MCU debugging and fixed buffers.

---

## 12. Buffer-Sizing Competency

Successfully calculated:

```text
"TEMP:" = 5 characters

"12345" = 5 characters
```

Combined C-string:

```text
"TEMP:12345\0"
```

Required = **11 bytes**

Therefore:

```cpp
char buffer[10];
```

is insufficient.

Also demonstrated:

```cpp
char buffer[7] = "ABC";

strcat(buffer, "XYZ");
```

requires:

```text
ABCXYZ\0
```

= **7 bytes**

and is therefore technically safe but leaves:

```text
0 bytes
```

of spare capacity.

This was correctly described as:

> "barely" / exact fit, with no room for another byte.

---

## 13. `main()` Return

Clarified that:

```cpp
int main() {

    // ...

}
```

implicitly returns `0` when execution reaches the closing `}`.

Explicit:

```cpp
return 0;
```

is still valid and useful for learning/readability.

---

## 14. Experiment 06 Status

**PASSED — close experiment here.**

Do not artificially extend Experiment 06.

Competency demonstrated in:

* C-string creation
* null termination
* indexing
* `strlen`
* `sizeof`
* `strcpy`
* `strcat`
* `strcmp`
* C-string comparison
* array/pointer relationship
* pointer dereferencing
* buffer sizing
* buffer overflow awareness
* undefined behavior
* fixed-size buffers
* practical MCU relevance

---

## 15. Important Next Topic

The next chat should **not simply continue adding generic C-string functions**.

The next topic should investigate the user's previously confusing Arduino/MCU area:

**C/C++ strings ↔ character input ↔ Arduino Serial**

Particularly:

```text
char

char[]

char*

std::string
```

and:

```text
Serial.print()

Serial.println()

Serial.write()
```

including:

* character vs string
* ASCII values
* numeric value vs character representation
* `'\n'`
* `'\r'`
* `'\0'`
* serial bytes
* C-string buffers
* receiving serial data
* command matching
* why `strcmp()` matters
* how this relates to real Arduino code

This should be treated as a **separate investigation/topic**, rather than pretending Experiment 06 itself needs more material.

---

## 16. Broader Stage 1 Awareness

Do not let C++ consume the entire stage.

The Master Curriculum explicitly keeps these parallel tracks:

### C/C++

Deep early programming track.

### Electronics

Continue building systematic fundamentals:

* voltage/current/resistance/power
* Ohm's law
* series/parallel
* Kirchhoff intuition
* resistors
* LEDs/diodes
* capacitors
* BJT/MOSFET
* relays/flyback
* regulation
* pull-up/pull-down
* debouncing
* ADC
* PWM
* logic levels
* grounding/noise

### Light Python

Not a second beginner course.

Focus progressively on:

* data structures
* strings
* functions
* comprehensions
* modules
* classes/OOP
* exceptions
* file handling
* code reading

### Code Literacy

Every programming stage should include code-reading, not only writing. The eventual target progresses from reading own code toward unfamiliar structured code, libraries, and eventually professional/open-source projects.

---

## 17. New Weekly-Planning Approach

**New approach introduced for future chats:**

The planning hierarchy is now:

```text
Master Curriculum

       ↓

Stage Progress Record

       ↓

Current Weekly Plan

       ↓

Current Chat
```

The weekly plan will contain the intended topics/tasks for the week.

However:

**The entire weekly plan does NOT have to be completed in one chat.**

The current chat should select the appropriate portion of the weekly plan based on:

* actual demonstrated competency
* available time/workload
* logical topic dependencies
* experiments and consolidation
* whether a competency gate has actually been reached

Do **not rush through topics merely because they appear later in the weekly plan.**

Likewise, do not artificially extend a topic just to consume the planned week.

The Master Curriculum remains the highest-level authority; the progress record provides continuity; the weekly plan provides the immediate practical direction. The Master Curriculum itself describes this three-level planning model.

---

## 18. Documentation

The user has:

```text
cpp/notes_per_task_template.md
```

Use its structure for future experiment documentation.

For each meaningful experiment, maintain:

**Learn → Predict → Build/Modify → Run/Test → Compare → Explain → Document → Commit**

Experiment 06 should be documented and committed before moving on if the user hasn't already done so.

## 19. Git State at Start of This Chat

```text
ammarahmed@Ammars-MacBook-Pro stage1-foundations % git log --oneline

f810042 (HEAD -> main) adding 06 c string operations, stclen, cpy, cat, cmp

13fbb3a in 05 c strings, testing p var (var that has a char address)

c1edeb4 in 05 stings, looping over the char array

e06a0e3 in 05 c strings, testing name, name[0], &name[0]

e3f7e06 adding 05 char array/ c strings)

253de23 in 04 arrays, replacing the four repetitive statements with a for loop

24523ff modifying 04 testing sizeof()

6d202b0 adding 03 cons0lidation test and 04 arrays Exs

137d908 Add Stage 1 foundations and C++ argument experiments
```

---
