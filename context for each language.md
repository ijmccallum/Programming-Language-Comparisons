# Teeny intro write-ups for context

## Assembly (Skipping this in further on steps but doing a wee write-up for funsies)

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

## FORTRAN 77

FORTRAN was created when punch cards were in use. Modern versions are still popular today. A rough timeline appears to go along the lines of:

1953: FORTRAN proposed as a more practical alternative to assembly  
1957: FORTRAN "Released"? Published?  
1958: FORTRAN II - added subroutines among other things (III added inline assembly)  
1962: FORTRAN IV - the first version standardized by ANSI/ISO  
1966: FORTRAN 66 standard named, essentially IV  
1977: FORTRAN 77 update to the standard. Further updates to the standard were delayed until 90 making 77 the more historically significant version - so going with that to get a taste!   

## ALGOL 60

ALGOL 58
ALGOL 60
ALGOL 68

"Designed by committee where every member tried hard to get their favorite thing in ... lessons learned in hindsight" (computerphile YouTube)

Intended to avoid some of the problems of FORTRAN (what problems specifically?)

Introduced:
 - Code Blocks (Begin ... end) (are these subroutines? Functions?)
 - Nested functions & lexical scope

Wasn't picked up by commercial computing due to a lack of standard I/O - instead it was used to define algorithms.
