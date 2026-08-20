# Stage 1 — C/C++

**Stage 0:** COMPLETE — exit gate passed.

## Workspace

```text
~/Engineering/learning/stage1-foundations/

stage1-foundations/

├── README.md

├── cpp/

├── electronics/

└── python/
```

## Stage 1 commits

```text
ammarahmed@Ammars-MacBook-Pro stage1-foundations % git status

On branch main

nothing to commit, working tree clean

ammarahmed@Ammars-MacBook-Pro stage1-foundations % git log --oneline

e3f7e06 (HEAD -> main) adding 05 char array/ c strings)
253de23 in 04 arrays, replacing the four repetitive statements with a for loop
24523ff modifying 04 testing sizeof()
6d202b0 adding 03 cons0lidation test and 04 arrays Exs
137d908 Add Stage 1 foundations and C++ argument experiments
```

## Governing documents

Master Curriculum v1.2:

[master_plan.md](https://github.com/Afxb9/Docs_in_md_language/blob/main/master_plan.md?utm_source=chatgpt.com)

This should remain the **authoritative curriculum/progress references**.

Stage 1 Progress Record 1 and 2:

https://github.com/Afxb9/Docs_in_md_language/blob/main/stage1_cpp_progress_record_1.md

https://github.com/Afxb9/Docs_in_md_language/blob/main/stage1_cpp_progress_record_2.md

---

## Initial Stage 1 diagnostic

Already completed — **do not repeat as a long diagnostic.**

Conclusion:

* Practical Arduino/C++ exposure.
* No dedicated C/C++ course background.
* Variables, arithmetic, functions and Boolean reasoning workable.
* References, addresses, pointers and memory initially developing gaps.
* Practical electronics experience, but systematic fundamentals need strengthening.
* Python practical, but structured code/OOP/code-reading need strengthening.

## C++ Experiments completed

### Experiment 01

Covered:

* variables
* `int`, `double`, `bool`
* arithmetic/operators
* functions
* arguments
* return values
* Boolean conditions
* prediction before execution

### Experiment 02

Covered:

* pass-by-value
* function-local parameters
* references
* modifying caller variables
* addresses
* basic scope

Key experimental result:

```cpp
int x
```

creates a separate parameter/copy.

```cpp
int& x
```

allows `x` to refer to the original variable.

```cpp
&variable
```

gets its address.

Reference and original variable produced identical addresses.

### Experiment 03 — Consolidation

Practical consolidation of Experiments 01–02.

Five exercises tested:

* types
* arithmetic/operators
* functions
* arguments
* return values
* Boolean conditions
* pass-by-value
* references
* modification of original variables
* addresses
* scope
* prediction
* debugging

**Result:** passed.

Important catches:

* `int` → `double` implicit conversion was understood.
* Pass-by-value does not modify caller variable.
* Reference modifies original.
* Reference and original have same address.
* Scope is determined by declaration location.
* A variable inside one function is not directly visible in another.
* Debugging compiler errors was successfully demonstrated.

### Experiment 04 — Arrays

Completed enough for competency checkpoint.

Covered:

```cpp
int sensorReadings[4];
```

Understanding:

```text
int             → element type

sensorReadings  → array name

[4]             → four elements
```

Indexes:

```text
0 1 2 3
```

not:

```text
1 2 3 4
```

Covered:

* declaration
* initialization with `{}`
* reading elements
* writing elements
* indexing
* `sizeof`
* determining element count
* `for` loops
* scope of `i`
* addresses of elements
* contiguous memory

Experimental evidence:

```text
int addresses increased by 4 bytes
```

and:

```text
sizeof(int) = 4

sizeof(array[4]) = 16
```

Also successfully debugged:

```cpp
for (int i = 0, i < 4, i++)
```

→ wrong separators.

Correct:

```cpp
for (int i = 0; i < 4; i++)
```

Then encountered the scope of `i` when trying to use it outside the loop.

### Experiment 05 — C-style strings

Currently in progress.

Established:

```cpp
char name[6] = "Ammar";
```

Conceptually:

```text
index   0  1  2  3  4   5

        A  m  m  a  r  \0
```

Covered:

* `char`
* character arrays
* string literals
* null terminator
* `'\0'`
* `'\n'`
* `'\r'`
* character vs integer
* `0` vs `'0'`
* `4` vs `'4'`
* C strings vs C++ `std::string`
* character-array memory
* `sizeof`
* addresses
* `name`
* `name[0]`
* `&name[0]`
* why `cout << &name[0]` prints `Ammar`
* why `static_cast<void*>(&name[0])` prints the address

Experimental evidence:

```text
A m m a r \0
```

occupied six bytes, with addresses increasing by one byte.

## Important unresolved area

Need a proper consolidation checkpoint for C strings before moving into broader string operations/pointers.
