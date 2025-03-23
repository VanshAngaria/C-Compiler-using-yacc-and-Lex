# 🛠️ Compiler Project

Welcome to the **C++ Compiler** project! 🚀 This compiler is implemented in multiple phases, each handling a specific task in the compilation process. Below is an overview of each stage along with the necessary commands to execute them.

---

## 📌 Compilation Stages

### 1️⃣ Token and Symbol Table Generation 🔤
- This phase scans the source code and generates tokens and a symbol table.
- Uses **Lex** for lexical analysis.
- **Run it with:**
  ```bash
  cd 1TokenandSymbolTableGeneration
  lex phase1.l
  gcc lex.yy.c
  ./a.out < test_input.cpp
  ```

### 2️⃣ Syntax Parsing 📜
- Checks the syntax of the code using **YACC**.
- Produces a **parse tree**.
- **Run it with:**
  ```bash
  cd 2SyntaxParser
  lex lexical.l
  yacc -d gram.y
  gcc lex.yy.c y.tab.c
  ./a.out < input.cpp
  ```

### 3️⃣ Semantic Analysis 🧠
- Ensures correct meaning and structure of the parsed code.
- Generates an **Abstract Syntax Tree (AST)**.
- **Run it with:**
  ```bash
  cd 3SemanticParser
  lex ast.l
  yacc -d ast.y
  gcc lex.yy.c y.tab.c
  ./a.out < input.cpp
  ```

### 4️⃣ Intermediate Code Generation 🏗️
- Converts the AST into intermediate code.
- **Run it with:**
  ```bash
  cd 4IntermediateCodeGeneration
  lex ast.l
  yacc -d ast.y
  gcc lex.yy.c y.tab.c
  ./a.out < input.cpp
  ```

### 5️⃣ Code Optimization ⚡
- Optimizes the intermediate code for better performance.

### 6️⃣ Assembly Code Generation 🏁
- Generates assembly code from the optimized intermediate code.
- **Run it with:**
  ```bash
  cd 6AssemblyCodeGeneration
  nasm -f elf64 icg.s -o output.o
  ld output.o -o program
  ./program
  ```

---

## 🎯 Features
✅ Tokenization and Symbol Table Handling  
✅ Syntax & Semantic Analysis  
✅ Intermediate Code Generation  
✅ Code Optimization  
✅ Assembly Code Generation  

---

## 📂 Folder Structure
```
📦 Compiler
├── 1TokenandSymbolTableGeneration
├── 2SyntaxParser
├── 3SemanticParser
├── 4IntermediateCodeGeneration
├── 5ICGOptimization
├── 6AssemblyCodeGeneration
└── README.md
```

---

## 🛠️ Prerequisites
Ensure you have the following installed:
- **Lex & Yacc**
- **GCC Compiler**
- **NASM (for assembly generation)**

Install using:
```bash
sudo apt install flex bison gcc nasm -y
```

---

## 🚀 Running the Full Compilation Process
To compile a full **C++ program**, run all phases sequentially:
```bash
cd 1TokenandSymbolTableGeneration && lex phase1.l && gcc lex.yy.c && ./a.out < test_input.cpp
cd ../2SyntaxParser && lex lexical.l && yacc -d gram.y && gcc lex.yy.c y.tab.c && ./a.out < input.cpp
cd ../3SemanticParser && lex ast.l && yacc -d ast.y && gcc lex.yy.c y.tab.c && ./a.out < input.cpp
cd ../4IntermediateCodeGeneration && lex ast.l && yacc -d ast.y && gcc lex.yy.c y.tab.c && ./a.out < input.cpp
cd ../6AssemblyCodeGeneration && nasm -f elf64 icg.s -o output.o && ld output.o -o program && ./program
```

---

## 📢 Contributing
Feel free to **fork** and improve this compiler! Pull requests are welcome. 🙌

---

## 📄 License
This project is **open-source** under the MIT License.

---

🌟 **Happy Coding!** 💻🎉

