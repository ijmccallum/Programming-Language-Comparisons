# Programming-Language-Comparisons
Fun wee side project to see if anything interesting pops up from looking at a bunch of different programming languages

**Why - what's the value?**

I'm a ~~Javascript~~ Typescript guy with a light-touch smattering of experiences in other languages, but nothing nearing the in-depth comprehension I have of JS. _I ~~need~~ want more knowledge!_

**How - what's the plan?**

To start: for each of the top n languages (popular/important/historic):
 - Do a teeny write-up to give context around what the language is intended for.
 - Map out how the fundamentals are done:
   - data handling (variables, types, scope)
   - instructions (loops, branches, functions)

After that: don't know! a few options to look into next could be concurrency/parallelism, memory management, error handling, performance, readability, or ecosystem (tooling/community/devX).

**First things first - which languages!**

(Creation - Release - Last update) 
```
Assembly _______(1947) (not digging in here - bit _too_ deep for me right now)  
FORTRAN ________(1957) ... (2023)  
Lisp ___________(1958) (which old one? Common Lisp?)  
COBOL __________(1959)  
BASIC __________(1963)  
Pascal _________(1970)  
Prolog _________(1972) ... (2024) (More of a standard for defining logic)
C ______________(1972) ... (2024)    
Smalltalk ______(1972)  (Will look at Smalltalk-80 - seems the defacto "Smalltalk". Pure Object Oriented - _everything_ is an object.)
C++ ____________(1979) ... (2023)  
MATLAB _________(1984) ... (2023)  
Perl ___________(1987) ... (2023)  
Python _________(1991) ... (2024)  
Erlang _________(1986) ... (2024)  
Haskell ________(1990) ... (2024)  
Visual Basic ___(1991) ... (2019)  
R ______________(1992) ... (2024)        
Ruby ___________(1993) ... (2023)      
PHP ____________(1994) ... (2023)    
Java ___________(1995) ... (2024)  
JavaScript _____(1995) ... (2023)  
Racket (Lisp) __(1995) ... (2023)  (A language for exploring and defining languages)
OCaml __________(1996) ... (2023)  
C# _____________(2000) ... (2023)  
Scala __________(2001) ... (2024)  
Groovy _________(2003) ... (2024)  
F# _____________(2005) ... (2023)  
Clojure (Lisp) _(2005) ... (2022)  
Rust ___________(2006) ... (2024)  
Go _____________(2009) ... (2024)  
Julia __________(2009) ... (2024)  
Elixir _________(2012) ... (2024)  
Swift __________(2014) ... (2023)  
```

## Teeny intro write-ups for context

### Assembly (Skipping this in further on steps but doing a wee write-up for funsies)

(an) Assembly language -> machine code -> Computer Architecture - all three are fairly tied together.

One Assembly instruction refers to a specific operation that the processor can perform. Follows that the processor you're working with determins the operations you can perform. Looks like there are 2 general approaches: CISC - complex individual instructions that do multiple things (memory/arithmetic/logic), and RISC - simple individual instructions.

```
CISC architectures / assembly languages
x86: Intel PCs (and AMD?)

RISC architectures / assembly languages
ARM: used on many cell phones and embedded systems
MIPS: IBM CPUs, Apple devices, gaming consoles
```
