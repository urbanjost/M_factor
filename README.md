## ![M_factor](docs/images/factor.gif)
# M_factor

This is a growing collection of Fortran procedures related to
factorization of integers and polynomials, and prime factorization.

## Introduction

Division is basically the reverse operation of multiplication. But it
gets a little more difficult when your factors can only be whole numbers.

The factors are any of the numbers (or symbols) that form a product when
multiplied together.

So, for example an **Integer Factor** is one of two or more integers
that can be exactly divided into another integer.

Another equivalent way to define "factor" is that it is quantity which
is multiplied by another quantity.

This is in contrast to statistics, where a factor can mean any independent
variable.

There are a few basic example programs included as well ...

+ **lcm**        -  display least common multiple of a list of whole numbers
+ **factors**    - [NUMBERS] display prime factors of numbers
+ **gcd**        - [NUMBERS] display greatest common divisor of a list of whole numbers

All the procedures are gathered into the Fortran module M_factor.f90. So far ...

## Name
  M_factor(3fm) - module for least common multiple, greatest
  common divisor, and prime factors

## Synopsis
```text
       use M_factor, only : least_common_multiple, greatest_common_divisor
       use M_factor, only : prime_factors, i_is_prime
```
+ least_common_multiple

    Least common multiple of two integers or vector m(:), matrix m(:,:)
    or cuboid m(:, :, :)

+ greatest_common_divisor

    greatest common divisor of two integers or vector m(:), matrix m(:,:)
    or cuboid m(:, :, :)

+ prime_factors

    decompose a number into its prime factors

+ i_is_prime

    Determine if a number is prime using Sieve of Erasthosthenes

## Description
  This module is a collection of procedures that perform common functions
  found in arithmetic and number theory such as Least Common Multiples,
  Greatest Common Divisors, and Prime Factors of INTEGER variables.  The
  INTEGER values are typically limited to values up to the magnitude
  (2**31)-1= 2147483647.

## Examples
  The individual man(1) pages for each procedure contain examples and a full
  description of the procedure parameters.

---
![gmake](docs/images/gnu.gif)
---
## Building the Module using make(1)
     git clone https://github.com/urbanjost/M_factor.git
     cd M_factor/src
     # change Makefile if not using one of the listed compilers
     
     # for gfortran
     make clean
     make F90=gfortran gfortran
     
     # for ifort
     make clean
     make F90=ifort ifort

     # for nvfortran
     make clean
     make F90=nvfortran nvfortran

This will compile the Fortran module and basic example
program that exercise the routine.

---
![-](docs/images/fpm_logo.gif)
---
## Build and Test with FPM

   Alternatively, download the github repository and build it with
   fpm ( as described at [Fortran Package Manager](https://github.com/fortran-lang/fpm) )

   ```bash
        git clone https://github.com/urbanjost/M_factor.git
        cd M_factor
        fpm run "*"
        fpm run --example "*"
        fpm test
   ```

   or just list it as a dependency in your fpm.toml project file.

```toml
        [dependencies]
        M_factor        = { git = "https://github.com/urbanjost/M_factor.git" }
```
---
![docs](docs/images/docs.gif)
---
## Documentation

### User
   - A single page that uses javascript to combine all the HTML
     descriptions of the man-pages is at 
     [BOOK_M_factor](https://urbanjost.github.io/M_factor/BOOK_M_factor.html).

   - a simple index to the man-pages in HTML form for the
   [routines](https://urbanjost.github.io/M_factor/man3.html) 
   and [programs](https://urbanjost.github.io/M_factor/man1.html) 

   - ![man-pages](docs/images/manpages.gif)
     There are man-pages in the repository download in the docs/ directory
     that may be installed on ULS (Unix-Like Systems).

      + [manpages.zip](https://urbanjost.github.io/M_factor/manpages.zip)
      + [manpages.tgz](https://urbanjost.github.io/M_factor/manpages.tgz)

   - [CHANGELOG](docs/CHANGELOG.md) provides a history of significant changes

### Developer
   - [ford(1) output](https://urbanjost.github.io/M_factor/fpm-ford/index.html).
<!--
   - [doxygen(1) output](https://urbanjost.github.io/M_factor/doxygen_out/html/index.html).
-->
   - [github action status](docs/STATUS.md) 
---
![-](docs/images/ref.gif)
---
## Pedigree

## References

   * [Wikipedia - Factorization](https://en.wikipedia.org/wiki/Factorization)
