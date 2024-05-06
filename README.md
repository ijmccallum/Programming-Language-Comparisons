## Programming-Language-Comparisons

Fun wee side project to see if anything interesting pops up from looking at a bunch of different programming languages

### Why - What's the Value?

I'm a ~~Javascript~~ Typescript guy with a light-touch smattering of experiences in other languages, but nothing nearing the in-depth comprehension I have of JS. _I ~~need~~ want more knowledge!_

### How - What's the Plan?

To start: for each of the top n languages (popular/important/historic):

- Do a teeny write-up to give context around what the language is intended for.
- Map out how the fundamentals are done:
  - data handling (variables, types, scope)
  - instructions (loops, branches, functions)
- With them mapped out, for each specific thing I'm looking at, group the languages together so we can see common patterns and maybe dig into some oddball cases.

After that: don't know! a few options to look into next could be concurrency/parallelism, memory management, error handling, performance, readability, or ecosystem (tooling/community/devX).

### Keeping Track ✅ 🔄 🟥

- Done ✅ (At least as far as I'm concerned for now)
- In Progress 🔄
- TODO 🟥

## Which Programming Languages 🔄

### List of Languages 🔄

Work in Progress list - many of these have multiple versions that differ significantly. As I dig into each I'll pick the version that appears to be the most historically significant.

Below I'm including the language "version" name and the date that version went "live".

```
  Listing these 2 for context only... for now
Machine Code ___(    )
Assembly _______(1947)

  A historically significant bunch from the 60s/70s
ALGOL __________(1958)
COBOL __________(1959)
Lisp ___________(1958)
FORTRAN 77 _____(1977)

Backus–Naur form? (a language to define languages... may come back to this)

BASIC __________(1963)
Pascal _________(1970)
Prolog _________(1972)
C ______________(1972)
Smalltalk-80 ___(1972)
C++ ____________(1979)
MATLAB _________(1984)
Perl ___________(1987)
Python _________(1991)
Erlang _________(1986)
Haskell ________(1990)
Visual Basic ___(1991)
R ______________(1992)
Ruby ___________(1993)
PHP ____________(1994)
Java ___________(1995)
JavaScript _____(1995)
Racket (Lisp) __(1995)
OCaml __________(1996)
C# _____________(2000)
Scala __________(2001)
Groovy _________(2003)
F# _____________(2005)
Clojure (Lisp) _(2005)
Rust ___________(2006)
Go _____________(2009)
Julia __________(2009)
Elixir _________(2012)
Swift __________(2014)
```

### Assembly (Skipping This in Further on Steps but Doing a Wee Write-up for fun) ✅

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

### FORTRAN 77 🔄

FORTRAN was created when punch cards were in use. Modern versions are still popular today. A rough timeline appears to go along the lines of:

1953: FORTRAN proposed as a more practical alternative to assembly  
1957: FORTRAN "Released"? Published?  
1958: FORTRAN II - added subroutines among other things (III added inline assembly)  
1962: FORTRAN IV - the first version standardized by ANSI/ISO  
1966: FORTRAN 66 standard named, essentially IV  
1977: FORTRAN 77 update to the standard. Further updates to the standard were delayed until 90 making 77 the more historically significant version - so going with that to get a taste!

### ALGOL 60 🔄

ALGOL 58  
ALGOL 60  
ALGOL 68

"Designed by committee where every member tried hard to get their favorite thing in ... lessons learned in hindsight" (computerphile YouTube)

Intended to avoid some of the problems of FORTRAN (what problems specifically?)

Introduced:

- Code Blocks (Begin ... end) (are these subroutines? Functions?)
- Nested functions & lexical scope

Wasn't picked up by commercial computing due to a lack of standard I/O - instead it was used to define algorithms.

### Prolog 🔄

More of a standard for defining logic

### Smalltalk-80 🔄

Smalltalk-80 seems the defacto "Smalltalk". Pure Object Oriented - _everything_ is an object.

## Concepts of Language Design 🔄

Things like "Lexical Scope", "Code Blocks" - the various things I'll be attempting to compare across various languages.

### Evaluation Strategy / Parameter-passing Strategy 🔄

Given a function that takes one (or some) parameter(s), _how_ are those params passed? Is it a value that becomes independent from the place it was called? Is it a reference to a location in memory where the value is stored? How else might this work? Turns out there are a bunch of ways to do this - way more than I expected!

_pass-by-... and call-by-... are the same thing. Going with pass-by... as it makes more sense to me._

- **pass-by-value** - "only" the value is passed in, editing the value in the called function won't change it in the caller. Usually done by copying the value to a new location in memory. Sets up a functional-like ability, but for functional languages where values are immutable pass-by-reference achieves the same thing.
- **pass-by-reference** - the caller passes the reference (a note of where the value/structure is held in memory). Modifications (to the object, or a reassignment of the object) are therefore visible to the caller. More efficient, but harder for programmers to avoid subtle bugs.
- **pass-by-sharing** - (for a specific type of value ("Reference", "Boxed Type", "Object")) a memory location is passed as in pass-by-reference (primitives passed by value?). Called functions can edit the value at that memory location. But, they cannot change where the ref points.
- **pass-by-pointer / address** a copy of the memory address is passed in. The called function can edit the data but if the pointer is reassigned that isn't reflected outside the function.
- **pass-by-copy-restore** - in the called function the value is copied, modifications are not visible outside it. Once the function returns, the final value is copied back into the original memory location from the caller scope. Acts _like_ pass-by-reference except when multiple functions running with the same argument both modify it before either return - neither will see the updates from the other. Only issue is not knowing which will return first. (Apparently, interest in this is picking up for Remote Procedure Calls as it allows us to drop a lot of cross-process coms!)
- **pass-by-unification**
- **pass-by-name** - don't figure out what the value passed is until it's needed?
- **pass-by-need** - don't figure out what the value passed is until it's needed? but memoised.
- **pass-by-reference-parameters**
- **pass-by-reference-to-const**

Table view of languages and which approach they allow?

**Pass-by-reference vs Pass-by-sharing (because the difference here seems pretty subtle!)**

```python
# I'm going to pass this list and in one case change the Data, in the other I'll change the Reference.
my_thing = [1, 2, 3]

def modify_value(ref):
    ref.append(4)  # Change the values in the given memory location

def modify_reference(ref):
    ref = [4, 5, 6]  # Change where the reference points

modify_value(my_thing)
print(my_thing)  # Output: [1, 2, 3, 4] - the data was changed!

modify_reference(my_thing)
print(my_thing)  # Output: [1, 2, 3] - the reference did not change
```

C++ allows a few options for passing parameters:

```cpp
#include <iostream>

void modifyValue(int x) {
    x = 2;
}
void modifyReference(int &x) {
    x = 3;
}
void modifyPointer(int *x) {
    *x = 4;
}

int main() {
    int myValue = 1;

    modifyValue(myValue);
    std::cout << myValue << std::endl; // Output: 1 (main scope wasn't changed)

    modifyReference(myValue);
    std::cout << myValue << std::endl; // Output: 3 (main scope WAS changed)

    modifyPointer(&myValue);
    std::cout << myValue << std::endl; // Output: 4 (main scope WAS changed)

    return 0;
}

```

## Comparisons! 🔄

### IF Statement 🟥

### IF Expression 🔄

ALGOL: `Z := if X = Y then P else Q `  
COBOL  
Lisp  
FORTRAN 77  
BASIC  
Pascal  
Prolog  
C  
Smalltalk-80  
C++  
MATLAB  
Perl  
Python  
Erlang  
Haskell  
Visual Basic  
R  
Ruby  
PHP  
Java  
JavaScript  
Racket (Lisp)  
OCaml  
C#  
Scala  
Groovy  
F#  
Clojure  
Rust  
Go

#### Julia

```Julia
score = 100
grade = if score > 80
    "Pass"
else
    "Fail"
end
println(grade)
```

#### Elixir

```Elixir
score = 100
grade = if score > 80 do
  "Pass"
else
  "Fail"
end
IO.puts(grade)
```

#### Swift 🔄 (not Got it Running Anywhere yet)

```swift
let score = 100
let grade: = if score > 80 { "Pass" } else { "Fail" }
print(grade)
```

### IF Ternary 🟥
