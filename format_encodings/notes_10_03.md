# COMP122 Lecture Notes: October 2 & 3, 2022

## Announcements
   1. Graded: 21-table-encodings
   1. Assignments:
      - 22-utf-encoding: Due Monday
      - 41-echo: Due Sunday night

## Today's Agenda
   1. Review outstanding questions
   1. Practicum
      - Table Encodings
      - UTF-8 Encodings
   1. Intro into Numbering Systems

   1. Concepts for the day:
      1. Introduce MIPS-122 with TAC

      1. TAC: simple constant calculation
         - Register Allocation (& Bookkeeping)
         - Providing the Result of a Calculation

      1. Providing Inputs
         - Code transformation
         - Well-known places

      1. Creating a Subroutine
         - Introduce Linkage between Subroutines
         - Marshaling

      1. Iteration via a For Loop
         - Multiplication via Successive Addition: Java Implementation
         - Transformation Process into:
           - Three Address Code (TAC)
           - MIPS

      1. Accessing an Array

      1. Processing of the argv Data Structure


## Questions
   1. M/W M: 
   1. M/W A:
   1. T/R M: 
   1. T/R A: 


---
# Today's Material
  1. See 10_03/

## MIPS-122 ISA:
   * TAC Instructions and corresponding subset MIPS Instructions

     1. Instructions
      - virtual registers: a, b, etc.  (name starts with a uppercase)
      - physical registers: $t0, $t1, etc.
      - memory references
        - text reference: label
        - data references: A, B, etc. (name starts with uppercase)
      - `<cond>`:  <, <=, ==, !=, >=, >
  
      | TAC Instruction               | MIPS Instruction          |
      |-------------------------------|---------------------------|
      | `nop`                         | `nop`                     |
      | `x = [ a \| imm ]`            | `li, move`                |
      | `x = a [+\|-] [ b \| imm ]`   | `add, sub, addi, subi`    |
      | `x = a * b`                   | `mul`                     |
      | `x = a >> imm`                | `srl`                     |
      | `if  a <cond> b, goto label`  | `b<cond> a, b, label`     |
      | `if! a <cond> b, goto label`  | `b<! cond>, a, b, label`  |
      | `goto label`                  | `b label`                 |
      | `x = & A`                     | `la x, A`                 |
      | `x = (* a)`                   | `lb x, 0(a)`              |
      | `call label`                  | `jal label`               |
      | `return`                      | `jr $ra`                  |

## TAC: simple constant calculation
  1. Example
     - x = 1 + 2 * 3 + 4
     * Problem 1: Where do I put things?
     * Problem 2: Where to do we place the results


## Providing Inputs 
  1. Example
     * area of a trapezoid
     * area = 1/2 * (height * base * top)
      
  1. Issues:
     * Problem 3: 1/2 is not integer
     * Problem 4: We don't have a divide operation
     * Problem 5: Where to do we place the inputs?

## Creating a subroutine
  1. Put the first two things together!

  1. Issuse
     * Problem 6: Multiple return locations:
     * Problem 7: Our input variables are over written



---
## Resources
   * 41-echo
   * git cheatsheet
