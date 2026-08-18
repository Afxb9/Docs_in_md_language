# Stage 1 — Progress Record

## Stage

Stage 1 — C/C++ + Electronics + Light Python

## Governing Resources

Master Curriculum v1.2:

https://github.com/Afxb9/Docs_in_md_language/blob/main/master_plan.md

Stage 0 Final Progress Record v1.4:

https://github.com/Afxb9/Docs_in_md_language/blob/main/stage0_final_progress_record_1.4.md

Stage 1 Progress Record 1:

https://github.com/Afxb9/Docs_in_md_language/blob/main/stage1_progress_record_1.md

The governing documents are maintained online in GitHub rather than as local reference files.

## Stage 0 Handover

Stage 0 is COMPLETE and passed its exit gate.

Stage 0 established:

* macOS development environment
* VS Code
* Git/GitHub workflow
* C++ compilation with clang++
* source → preprocess → compile → link → executable mental model
* basic .h/.cpp separation
* branches, merge and remote repository workflow
* engineering workspace structure

Stage 1 should NOT restart Stage 0 except for brief reinforcement when required.

## Stage 1 Workspace

Master workspace:

```text
~/Engineering/
```

Stage 1 repository:

```text
~/Engineering/learning/stage1-foundations/
```

Current structure:

```text
stage1-foundations/

├── README.md

├── cpp/

├── electronics/

└── python/
```

The cpp directory currently contains:

* `01_types_functions.cpp`
* `01_types_functions.md`
* `02_function_arguments.cpp`
* `02_function_arguments.md`
* `notes_per_task_template.md`

Compiled executables are currently also present:

* `01_types_functions`
* `02_function_arguments`

## Git State

Repository initialized on branch:

```text
main
```

First Stage 1 commit:

```text
137d908 — Add Stage 1 foundations and C++ argument experiments
```

At the end of this chat:

```text
working tree clean
```

## Initial Stage 1 Diagnostic

The initial diagnostic was completed in this chat.

### C/C++

Existing practical exposure:

* Arduino programming experience
* Has seen C/C++ code
* No dedicated previous C/C++ course

Diagnostic showed:

* Basic arithmetic and variable reasoning is functional.
* Basic functions are understandable with practical examples.
* References, addresses, pointers and memory concepts are currently developing areas.
* Scope needs continued reinforcement.
* Arrays, strings, structs, pointers and deeper C/C++ concepts have not yet been systematically studied.
* C++ should therefore be developed through practical experiments rather than assuming zero programming knowledge.

### Electronics

Existing practical experience:

* Arduino and motor-driver use
* L293D/L298N motor-driver experience
* Practical understanding of external motor power and MCU protection
* Familiarity with pull-up concepts and button wiring

Diagnostic showed:

* Basic voltage/current/resistance understanding exists.
* Ohm's law is known: V = IR.
* Voltage-divider reasoning is partially understood.
* Pull-up resistor purpose is broadly understood.
* MOSFET switching concept is recognized, but MOSFET operation and switching details need strengthening.
* Capacitors, decoupling, transistor behavior and related electronics fundamentals require systematic development.

### Python / Code Literacy

Existing practical Python experience exists.

Diagnostic showed:

* Basic reading of simple Python code is possible.
* Some concepts such as function arguments and `len()` can be recognized.
* `self`, classes/objects, structured Python and deeper code-reading concepts need development.
* Stage 1 should use short Python exercises and code-reading tasks rather than restarting a complete beginner Python course.

## C++ Work Completed

### Experiment 01 — Types and Functions

Topics demonstrated:

* `int`
* `double`
* `bool`
* variables
* arithmetic operators
* function declaration/definition
* function arguments
* return values
* Boolean comparison
* `true`/`false` displayed as `1`/`0`

Program used a sensor-reading example:

```text
sensorReading → offset → correctedReading → alarm
```

The learner correctly predicted all tested outputs.

Tests included:

* sensorReading = 120, offset = -5 → corrected = 115 → alarm true
* sensorReading = 90, offset = -5 → corrected = 85 → alarm false
* sensorReading = 90, offset = 20 → corrected = 110 → alarm true

### Experiment 02 — Function Arguments, References and Addresses

First demonstrated:

```cpp
void changeValue(int x)
```

The learner observed that changing `x` does not change the original `sensorReading`.

Mental model established:
Passing by value → function receives a copy.

Then changed to:

```cpp
void changeValue(int& x)
```

Observed:

```text
Before: 120
Inside before: 120
Inside after: 130
After: 130
```

The learner correctly concluded that changing `x` changes the original `sensorReading`.

Then memory addresses were printed.

Observed:

```text
Address of sensorReading:
0x7ff7b1671308

Address of x:
0x7ff7b1671308
```

The identical addresses provided experimental evidence that the reference refers to the same underlying variable.

## Concepts currently understood

* A normal parameter such as `int x` receives a copy.
* A reference parameter such as `int& x` refers to the original variable.
* A variable occupies a location in memory.
* A memory address identifies that location.
* `&variable` can obtain its address.
* `int& x` declares a reference.
* `x` remains a local name whose scope is the function.
* A reference does not make `x` globally available outside the function.
* The variable referred to by `x` depends on the argument passed during the function call.

## Current mental model

### Value parameter

```text
variable
   → value copied
   → local parameter
   → changes do not affect original
```

### Reference parameter

```text
original variable
       ↕
reference parameter
       → both refer to the same variable
```

### Address

```text
variable
   → stored somewhere in memory
   → memory location has an address
```

## Important Learning Decision

**Do NOT immediately move on as if these concepts are fully mastered.**

Before advancing, add targeted exercises to Experiments 01 and 02 covering everything learned so far.

Exercises should test:

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
* prediction before execution

Exercises should be short and practical, not a long written exam.

## Documentation Workflow

A reusable template was added:

```text
cpp/notes_per_task_template.md
```

The learner intends to copy the template for future exercises.

Engineering documentation should remain proportional and should capture meaningful:

* objective
* relevant theory
* setup
* procedure
* measurements/results
* failures
* debugging
* root cause
* lessons learned
* next improvement

## Learning Method

Use:

```text
Learn
 → Predict
 → Build/Modify
 → Run/Test
 → Compare
 → Explain
 → Document
 → Commit
```

Prefer evidence from experiments and real code over lengthy theoretical exams.

## Chat Continuity Rule

Do not split a chat in the middle of a meaningful topic.

Split after a coherent milestone, such as:

* topic completed
* exercises completed
* documentation updated
* Git checkpoint created

A new chat within Stage 1 must use this Progress Record as the handover rather than restarting the stage.

## Current Stage Position

### Completed

* Stage 1 repository setup
* Initial diagnostic
* C++ types/functions foundation
* C++ function arguments
* Pass-by-value
* References
* Memory addresses
* Basic scope understanding
* First documented Git milestone

### Next

Consolidate the first C++ topic with targeted exercises for Experiments 01 and 02.

Then continue with the Stage 1 C/C++ sequence, including arrays/strings, C-style arrays and strings, structs/enums, pointers/dereferencing and subsequent memory concepts.

Electronics and light Python should continue in parallel according to the Stage 1 curriculum.

## Workload

Normal sustainable target:

**4–5 hours/week**

Progress is competency-gated, not time-gated.

## Stage 1 Exit Direction

Stage 1 ultimately requires capability in:

* C/C++ foundations
* references/pointers/memory
* structured multi-file C++
* basic C literacy
* code reading
* electronics fundamentals
* Python foundation/code reading
* sensor/actuator integration

### Final Stage 1 Project

ESP32 sensor/actuator module with sensors, controlled load/motor, LEDs/buttons, appropriate interface/power circuitry, I²C or SPI, and at least one reusable C++ sensor driver developed from a datasheet.

The sequence above is grounded in the master curriculum's Stage 1 scope and exit gate.

---
