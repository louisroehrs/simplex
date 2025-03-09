# simplex
The simplest language ever made for interacting with devices on the internet.

### Design Principles of Simplex
1. **Human-Centric Syntax**: Mimics natural language where possible, reducing cognitive load.
2. **Minimal Boilerplate**: No unnecessary keywords or punctuation (e.g., no semicolons unless disambiguating).
3. **Implicit Power**: Built-in features handle common tasks (e.g., concurrency, data manipulation) without complexity.
4. **Forgiving**: Sensible defaults and clear error messages to encourage learning.
5. **Extensible**: Advanced users can define custom behaviors without breaking simplicity.

---

### Core Features
- **Variables**: No type declarations needed unless explicitly desired (inferred by usage).
- **Functions**: Defined with a single keyword and natural flow.
- **Loops and Conditions**: Plain English-like constructs.
- **Concurrency**: Built-in "do parallel" keyword for effortless multitasking.
- **Data Structures**: Lists, maps, and sets are native, with simple syntax.
- **Error Handling**: Automatic "try" with optional explicit handling.

---

### Syntax and Examples

#### 1. Hello World
```
say "Hello, world!"
```
- No `main` function or setup—just write what you want to do.
- `say` is the print command, intuitive and short.

#### 2. Variables and Basic Math
```
x = 5
y = 10
total = x + y
say total  # Outputs: 15
```
- No type declarations; `x` and `y` are inferred as numbers.
- Assignment uses `=`, and math operations are standard.

#### 3. Functions
```
define add a b
  return a + b

result = add 3 7
say result  # Outputs: 10
```
- `define` starts a function, followed by its name and parameters.
- No parentheses or curly braces unless needed for clarity.

#### 4. Conditions
```
score = 85
if score > 90
  say "Excellent"
else if score > 70
  say "Good"
else
  say "Try again"
```
- Reads like English: `if`, `else if`, `else`.
- No parentheses or brackets unless grouping is ambiguous.

#### 5. Loops
```
count from 1 to 5
  say count
```
- Outputs: 1, 2, 3, 4, 5
- `count` is the loop variable, and `from ... to ...` defines the range.

#### 6. Lists and Maps
```
fruits = ["apple", "banana", "orange"]
say fruits[0]  # Outputs: apple

person = {name: "Alex", age: 30}
say person.name  # Outputs: Alex
```
- Lists use square brackets `[]`; maps use curly braces `{}` with key-value pairs.
- Dot notation (`.`) for accessing map values, intuitive and clean.

#### 7. Concurrency
```
do parallel
  task1: say "Task 1 running"
  task2: say "Task 2 running"
```
- `do parallel` spawns tasks concurrently without manual thread management.
- Tasks are labeled (e.g., `task1`) for clarity.

#### 8. Error Handling
```
number = "abc" / 0  # This will fail
say "This won't run"
```
- Simplex catches errors automatically and stops gracefully, printing:
  ```
  Error: Division by zero or invalid operation at line 1
  ```
- Optional explicit handling:
```
try
  number = "abc" / 0
catch error
  say "Oops: " + error
```
- Outputs: "Oops: Division by zero or invalid operation"

#### 9. Advanced: Custom Operators
```
define operator ** as base power
  return base ^ power

say 2 ** 3  # Outputs: 8
```
- Users can define custom operators (like `**` for exponentiation), making the language extensible.

---

### Why It’s Easy and Powerful
- **Ease of Use**: Syntax mimics natural language (e.g., "count from 1 to 5"), reducing the learning curve. No cryptic symbols or rigid structures intimidate beginners.
- **Power**: Concurrency, custom operators, and native data structures provide advanced functionality without complexity.
- **Human Factors**: Clear error messages, sensible defaults (e.g., inferred types), and minimal punctuation lower mental effort.
- **Scalability**: From simple scripts to complex systems, Simplex adapts via optional explicit features (e.g., types, manual memory management) for pros.

---
