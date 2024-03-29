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
1st Generation: Machine code
2nd Generation: Assembly languages
3rd Generation: More machine-independent and programmer-friendly
4th Generation: Specific to a domain
5th Generation: Problem-solving using constraints, though looking into a couple they are noted as being written in one of the lower level languages.

Machine Code ___ 1 (    )
Assembly _______ 2 (1947) (not digging in here - bit _too_ deep for me right now)

Historically significant bunch from the 60s/70s
ALGOL __________ 3 (1958)
COBOL __________ 3 (1959)  
Lisp ___________(1958) (which old one? Common Lisp?)
FORTRAN 77 _____ 3 (1977)

BASIC __________ 3 (1963)  
Pascal _________ 3 (1970)  
Prolog _________(1972) ... (2024) (More of a standard for defining logic)
C ______________ 3 (1972) ... (2024)    
Smalltalk ______(1972)  (Will look at Smalltalk-80 - seems the defacto "Smalltalk". Pure Object Oriented - _everything_ is an object.)
C++ ____________ 3 (1979) ... (2023)  
MATLAB _________(1984) ... (2023)  
Perl ___________ 3 (1987) ... (2023)  
Python _________ 3 (1991) ... (2024)  
Erlang _________(1986) ... (2024)  
Haskell ________(1990) ... (2024)  
Visual Basic ___(1991) ... (2019)  
R ______________ 4 (1992) ... (2024)        
Ruby ___________(1993) ... (2023)      
PHP ____________ 3 (1994) ... (2023)    
Java ___________ 3 (1995) ... (2024)  
JavaScript _____(1995) ... (2023)  
Racket (Lisp) __(1995) ... (2023)  (A language for exploring and defining languages)
OCaml __________(1996) ... (2023)  
C# _____________ 3 (2000) ... (2023)  
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

One Assembly instruction refers to a specific operation that the processor can perform. Follows that the processor you're working with determines the operations you can perform. Looks like there are 2 general approaches: CISC - complex individual instructions that do multiple things (memory/arithmetic/logic), and RISC - simple individual instructions.

```
CISC architectures/assembly languages
x86: Intel PCs (and AMD?)

RISC architectures/assembly languages
ARM: used on many cell phones and embedded systems
MIPS: IBM CPUs, Apple devices, gaming consoles
```

Maybe one day I'll come back and dig through some assembly instructions. But for now - onwards to the next language!

### FORTRAN 77

FORTRAN was created when punch cards were in use. Modern versions are still popular today. A rough timeline appears to go along the lines of:

1953: FORTRAN proposed as a more practical alternative to assembly  
1957: FORTRAN "Released"? Published?  
1958: FORTRAN II - added subroutines among other things (III added inline assembly)  
1962: FORTRAN IV - the first version standardized by ANSI/ISO  
1966: FORTRAN 66 standard named, essentially IV  
1977: FORTRAN 77 update to the standard. Further updates to the standard were delayed until 90 making 77 the more historically significant version - so going with that to get a taste!   

### ALGOL 60

"Designed by committie where every member tried hard to get their favourite thing in ... lessons learned in hindsight" (computerphile youtube)
