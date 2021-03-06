# Obfuscation Benchmarks

By *Obfuscation Benchmarks* we mean programs which can be obfuscated using different tools at: source code, intermediate representation and/or machine code level.
The reason for obfuscating these programs can be (but is not limited) to compare the strength of different obfuscation transformations/implementations against both human-assisted and automated attacks. 
This repository contains the source code of C programs, which can be used as obfuscation benchmarks. 

## Description of Each Directory

  - `basic-algorithms` contains typical algorithms taught in Bachelor level computer science and programming courses, e.g. factorial, sorting algorithms, searching algorithms, greatest common divisor, least common multiple, etc.
  - `simple-hash-functions` contains non-cryptographic hash functions 
  - `small-programs` contains a set of 48 programs with few lines of code constructed by varying the following code characteristics:
    - Range of symbolic inputs
    - Number of symbolic inputs
    - Depth of nested control flow
    - Number of IF-statements
    - Number of input dependent IF-statements
    - Type of IF-condition
    - Number of loops
    - Number of input length dependent loops (e.g. if the input is 10 characters long, then the loop has 10 iterations)
    - Number of input value dependent loops (e.g. if the input is an integer equal to 100, then the loop has 100 iterations)
  - `tigress-generated-programs` contains a large set of programs automatically generated by the `RandomFuns` transformation of the [Tigress C Diversifier/Obfuscator](http://tigress.cs.arizona.edu/) by varying the following command line options:
    - `Seed` randomization seed
    - `RandomFunsTypes` data type of variables
    - `RandomFuns Operators` types of operators (e.g. arithmetic, logic)
    - `RandomFunsControlStructures` control structure of the program
    - `RandomFunsBasicBlockSize` the number of statements in each basic block
    - `RandomFunsForBound` the type of bound in loop conditions (e.g. constant, input dependent) 
  - `scrips` contains bash, Python and R scripts to obfuscate C programs
    using the Tigress and ollvm obfuscation tools and to perform a
symbolic execution attack described a series of papers by Banescu et
al. [1], [2] and [3]. For more details about how to use these scripts
see README inside folder.

## References

1. Banescu, S., Ochoa, M., & Pretschner, A. (2015, May). _A framework for measuring software obfuscation resilience against automated attacks_. In Proceedings of the 1st International Workshop on Software Protection.
2. Banescu, S., Collberg, C., Ganesh, V., Newsham, Z., & Pretschner, A. (2016, December). _Code obfuscation against symbolic execution attacks_. In Proceedings of the 32nd Annual Conference on Computer Security Applications.
3. Banescu, S., Collberg, C., & Pretschner, A. (2017, August). _Predicting the Resilience of Obfuscated Code Against Symbolic Execution Attacks via Machine Learning_. In Proceedings of the 26th USENIX Security Symposium.
