## Hi, I'm František Slivko

Currently a B.Sc. student in Informatics at IMC University of Applied Sciences Krems (2025–2027), focusing on systems programming, compiler construction, and low-level programming.

[LinkedIn](https://www.linkedin.com/in/frantisek-slivko)


### Technical Skills
​- Primary: C, C++, x86-64 Assembly, Rust, Python
- Familiar: Kotlin, Java, C#, LLVM IR, Pascal
​- Compilers & Systems: Compiler Design, SSA IR, LLVM, QBE, ELF64 / PE32+ Formats, System V AMD64 ABI
​- Tools & Environment: Linux, Git, CMake, Make, GitHub, GDB, objdump, readelf


​### Featured Projects
​
**[chek](https://github.com/FrantisekSlivko/chek)  — Native x86-64 Compiler in C**
​A zero-dependency, native compiler written in C targeting x86-64 (ELF64 and PE32+).
​- Frontend: Zero-copy tokenizer, recursive-descent and Shunting-Yard expression parser, and `file:line:col` caret diagnostics.
​- Optimizations (`-O1` / `-O2`): Constant folding, constant propagation, algebraic simplification, constant branch evaluation, and function inlining.
​- Backend: Custom x86-64 code generator following the System V AMD64 ABI with standalone ELF64 and PE32+ binary emitters (no external assembler or linker).


**Multi-Stage SSA Compiler in C** *(In Progress)*  
A statically typed compiler written in C targeting QBE.
- **Frontend & IR:** Emits SSA HIR directly during parsing without building an AST or resolving types.
- **HIR Analysis:** Type inference on temporals and stack slot materialization for address taken or oversized values.
- **Middle-End:** Progressive lowering from SSA HIR to SSA MIR with static type checking, lazy monomorphization for generics, and an RAII verification pass.
- **Backend:** Lowers verified SSA MIR to QBE IR.
