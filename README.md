General Utilities For Picat
-------------
General utility functions and predicates for Picat programming language. 
> **Invoke Web service / REST API:**
bp.shell(X, "curl -X GET https://catfact.ninja/fact")
X will contain response:
X = '{"fact":"The first formal cat show was held in England in 1871; in America, in 1895.","length":75}'

> **Invoke Python program:**
bp.shell(X, "/usr/bin/python3 myprogram.py")
X will contain output.

The C source files (genutils/genutils.c, etc.) for these functions and predicates are released for anyone to use, modify and distribute freely for any purpose, including commercial purpose, under the Mozilla Public License, v. 2.0:

http://mozilla.org/MPL/2.0/. 

In essence, anyone is allowed to build works, including
proprietary ones, based on ths code, as long as the Source
Code Form is retained. The copyright holders, developers,
and distributors will not be held liable for any direct or
indirect damages.

Picat Quickstart
-------------
Picat is a logic programming language based on B-Prolog that implements imperative and functional programming language features. For detailed information please refer http://www.picat-lang.org/

About The Author
--------------------
Dilshad Mustafa is a Senior Software Architect with 20 years experience in Information Technology industry. He has experience across various domains, Banking, Retail, Healthcare, Energy & Utilities, Materials & Supply Chain.

He completed his B.E. in Computer Science & Engineering from Annamalai University, India and completed his M.Sc. in Communication & Network Systems from Nanyang Technological University, Singapore.
