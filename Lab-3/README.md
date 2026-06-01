# LAB 3: Lexical Analyzer for Token Counting Using Flex (Lex)

## Objective

The objective of this lab is to design and implement a lexical analyzer using Flex (Lex) that reads input source code and classifies and counts different types of tokens such as keywords, identifiers, numbers, strings, operators, delimiters, logical operators, comments, and unknown tokens.

---

## Theory

Lexical analysis is the first phase of a compiler. It scans the source code character by character and converts it into meaningful tokens.

Flex (Fast Lexical Analyzer Generator) is a tool used to generate lexical analyzers automatically.

In this lab, the lexer not only identifies tokens but also maintains counters for each token type.

The tokens identified are:

- Keywords
- Identifiers
- Numbers
- Strings
- Operators
- Logical Operators
- Delimiters
- Comments
- Unknown Tokens

---

## Requirements

- macOS / Linux / Windows
- Flex (Lex)
- GCC Compiler

### Installation on macOS

```bash
brew install flex bison
```

### Steps to Execute

- Step 1: Create a Lex file
  Save teh program with the name:
  ```bash
  token_counter.l
  ```
- Step 2: Generate C source file using Flex
  ```bash
  flex token_counter.l
  This will generate "lex.yy.c"
  ```
- Step 3: Compile the generated C file
  ```bash
  gcc lex.yy.c -o token_counter
  ```
- Step 4: Run the program
  ```bash
  ./token_counter
  ```
- Step 5: Provide input
  - Type or paste your C code
  - Press:
    - Ctrl + D (Mac/Linux) to end input
    - (Ctrl + Z + Enter on Windows)
- Step 6: View Ouput
  - The program will display each token type
  - It will also show the final count of all tokens
