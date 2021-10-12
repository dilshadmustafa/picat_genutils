General Utilities For Picat
-------------
General utility functions and predicates for Picat programming language. 
> **Invoke Web service / REST API:**
<br>bp.shell(X, "curl -X GET https://catfact.ninja/fact")
<br>X will contain response:
<br>X = '{"fact":"The first formal cat show was held in England in 1871; in America, in 1895.","length":75}'

> **Invoke Python program:**
<br>bp.shell(X, "/usr/bin/python3 myprogram.py")
<br>X will contain output.

> **Compile as below (tested in Pop Linux):**
<br>$ cd emu
<br>$ make -f Makefile
<br>$ ./picat

The C source files (genutils/genutils.c, etc.) for these functions and predicates are released for anyone to use, modify and distribute freely for any purpose, including commercial purpose, under the Mozilla Public License, v. 2.0:

http://mozilla.org/MPL/2.0/. 

In essence, anyone is allowed to build works, including
proprietary ones, based on ths code, as long as the Source
Code Form is retained. The copyright holders, developers,
and distributors will not be held liable for any direct or
indirect damages.

> **Files Added/Modified:**
3 files added/modified: emu/genutils/genutils.c, emu/Makefile and emu/cpreds.c

Makefile (file path in git repo: emu/Makefile):-
Below lines added/modified:

GENUTILS_FLAGS = -c -O3 -I. -Igenutils
GENUTILS_OBJ = genutils.o

picat : $(OBJ) $(ESPRESSO_OBJ) $(GENUTILS_OBJ) $(KISSAT_OBJ)  
    $(CPP) -o picat $(OBJ) $(ESPRESSO_OBJ) $(GENUTILS_OBJ) $(KISSAT_OBJ) $(LFLAGS)  

genutils.o : genutils/genutils.c
    $(CC) $(GENUTILS_FLAGS) -o genutils.o genutils/genutils.c

cpreds.c file (file path in git repo: emu/cpreds.c):-
Below lines added/modified:

// Added
extern int p();
extern int shell();

// Added
insert_cpred("p", 2, p);
insert_cpred("shell", 2, shell);


Picat Quickstart
-------------
Picat is a logic programming language based on B-Prolog that implements imperative and functional programming language features. For detailed information please refer http://www.picat-lang.org/

About The Author
--------------------
Dilshad Mustafa is a Senior Software Architect with 20 years experience in Information Technology industry. He has experience across various domains, Banking, Retail, Healthcare, Energy & Utilities, Materials & Supply Chain.

He completed his B.E. in Computer Science & Engineering from Annamalai University, India and completed his M.Sc. in Communication & Network Systems from Nanyang Technological University, Singapore.
