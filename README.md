# Hash-Compiler
![hash](https://user-images.githubusercontent.com/22862602/65395296-3fb3e600-dd99-11e9-9b96-47f0abf987cd.png)
### **About**
**Hash Compiler** is a procedural & linear interpreted language written in C++ using .Net Framework 4.8. The development started in 2017, I was student on high school playing around programming stuff and trying to make something initiative. The language itself is quite easy to understand, uses shortcuts, supports dynamic variables, custom functions, ‘line jumps’, file streaming Input/Output & additional user-friendly methods. Compiler runs linearly, starting by zero line & ending by total length. The package contains **32 & 64 bit version** of the **Hash Compiler language** and universal programming editor called **Hash Editor**. Hash Editor contains some examples which can be useful for new users. Hash Compiler is written in **C++**, Hash Editor in **C#**.

### **Why did I wrote this language?**
Well, I wanted something more challenging as I love complications & I think it's been done pretty well. I just love making unusual things especially initiative/creative applications where users can use their own logic and create something new in a short period of time. Also I wanted to expand my knowledge about programming and technology in general by practicing this kind of stuff!

### **Installation**
It's important to install correct Hash Compiler version. If your CPU is 32bit, use 32bit Setup, otherwise use 64bit. I suggest to install Hash Compiler pack to **any other drive except C** *(If so, you wouldn't be able to create files)*.

### **Syntax & Semantics**
Hash Compiler is a language in which every statement & command starts with **#** (obviously). Uses shortcuts which represent functional statements. Statements are divided into 2 types: Static & Dynamic statements. What is the difference?\
• Static Statements (console-out/in, file-in/out) usually use **;** character (or might be **|** or none) at the end of the line.\
• Dynamic Statements *(calculations, conditions, substring)* use **}** character at the end of the line. Spaces between statements are very important, please write statements exactly as they are in their basic form & try not to make additional spaces.\
*Why is that? Dynamic statements mostly continues in line below the statement.*\
**Each line can hold just one statement**, otherwise the compiler will evaluate syntax error.\
Compiler ignores unknown characters, basically you can write anything else to make 'comments'.

<br/>

*Last Semantics Update on 22/09/2019 (dd/mm/yyyy)*

<br/>
<br/>

**System Essentials**
*System essential statements built in Hash Compiler.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #HELP | *Full documentation will be shown in console* | No example, use format above |
| #DATE | *Get actual date format* | `#CHAR>VarName:#DATE;` |
| #GET_VAR | *Get all internal variables by name in lines (-l) by name in rows (-r) by value in lines (-v) by value in rows (-vr) & get count of available variables (-n)* | `#GET_VAR-vr` |
| #SLEEP | *Pause program in a specific period of time (miliseconds)* | `#SLEEP NumericValue` |
| #MOOD | *Special & fun statement to improve your mood. Get a better mood!* | `#MOOD` |
| #REPL | *Interactive and returnable question. Quick alternative for conditions* | `#REPL(Anything to ask)CharResultToEqual>ToLineIndex;` |
| #0 | *Quit solution & program* | `#0` |

<br/>
<br/>

**Variable Declerations**
*General variable decleration. Exist variables will be replaced.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #NUM | *Any unsigned natural number variable decleration. Use NULL for null value* | `#NUM>VarName:VarValue;` |
| #CHAR | *Any characteristic variable decleration. Use NULL for null value* | `#CHAR>VarName:VarValue;` |

<br/>
<br/>

**Console Input-Output**
*Default console input-output statements.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #COPUT | *Console output. Use **@VarName@** for variable mention* | `#COPUT{NEWLINE}Value or @VarName@` |
| #COPUTL | *Create new line in console output* | `#COPUTL or #COPUTL CountOfNewLines` |
| #CIPUT | *Console input* | `#CHAR>VarName:#CIPUT;` |
| #CIP | *Stops the program and waits for user's interaction* | `#CIP` |

<br/>
<br/>

**Math & Calculations**
*Basic math functions & calculations. Calculations can be proceed with variables of type NUM only. Variables of type CHAR use Character-Related Functions.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #CALC | *Default calculation process of natural numbers. You can create a new variable by adding VarName after operation symbol* | `#CALC+ or #CALC/VarName{NEWLINE}Number or VarName {SPACE} Number or VarName}` |
| #RAND | *Get random number from-to* | `#NUM>VarName:#RANDvalueFrom-ValueTo|` |

<br/>
<br/>

**Character-Related Functions**
*Main functions for CHAR datatype. Substring (divide/cut) variable value of type CHAR or add new characters to the variable value of type CHAR.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #SUBCHAR | *Substring or divide character variable* | `#SUBCHAR>StartIndex>Length=ToExistsCHARVariable}` |
| #SUBCHAR | *Substring or divide character variable & create new variable* | `#SUBCHAR<StartIndex<Length=NewCHARVariable<FromExistsCHARVariable}` |
| #ACHAR | *dd characters to exist variable* | `#SUBCHAR>VarName1+VarName2;` |

<br/>
<br/>

**File Streaming (Create, Delete, Read)**
*File streaming allows you to control your files/ folders in your computer. It might be very risky as you can clearly delete your important folder or even drive. Testing on external & empty drive is recommended.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #FILETRANS | *Create new file in exists path. Use **~** to replace **:** character in the variable assignment ONLY* | `#FILETRANSfilename!filecontent!fileextension;` |
| #RFILETRANS | *Read data from file in exists path. Use **~** to replace **:** character in the variable assignment ONLY* | `#RFILETRANSfilename!fileextension;` |
| #DFILETRANS | *Delete file in exists path. Use **~** to replace **:** character in the variable assignment ONLY* | `#DFILETRANSfilename!fileextension;` |

<br/>
<br/>

**Looping/ Repeating**
*Looping or repeating allows you to repeat specific lines of code by included count.*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #LOOP | *Loop specific lines limitedly. Ending with **!** and **NEW LINE*** | `#LOOP or #LOOP CountOfLoops{NEWLINE}...Content.. {NEWLINE}!` |

<br/>
<br/>

**Conditions**
*Hash Compiler contains **two-valued condition system** which is a bit limited but it's far enough. Conditions in Hash Compiler have a very limited perspective because the result can be proceed just once, but you can **avoid** this limitation by **jumping to the specific line or function** writing **#FGOTO** or **#GOTO** (More in Custom Functions & Methods). You can use variables or custom characters by **#_** keyword (More in Parsers) and compare the result by the available operators (More below).*

| Statement | Description | Formal Example |
| --- | --- | --- |
| #IF_ | *Two-valued condition system. Supports 6 operators: > (greater), < (less), = (equal for NUMS), - (equal for CHARS), ^ (not equal for NUMS), ! (not equal for CHARS)* | `#IF_VarName = VarName}{NEWLINE}...Content...` or `#IF_VarName - #_HelloWorld}{NEWLINE}...Content...` |


<br/>
<br/>


**Custom Functions & Methods**\
*Functions allow you to make your code much more clear. For example, if you would like to process some kind of calculations, you will simply write DoCalculation and the specific function will be called. To declare any function, write any text in any line to represent the function. Example: **MyFunctionName{NEWLINE}...Content...***

| Statement | Description | Formal Example |
| --- | --- | --- |
| #GOTO | *Jump to the specific line index by line number* | `#GOTO LineIndexNumber` |
| #FGOTO | *Jump to the specific line index by function name* | `#FGOTO FunctionName` |


<br/>
<br/>


**Parsers, Checkers & Connectors**
*Parsers allow you to convert specific variable value of one type to another type. For example, if we have a characteristic number of type **CHAR** and we would like to convert it to the numeric type **NUM**, Hash Compiler uses keyword **#NUM_**. But first of all, we must check if it's even POSSIBLE to do it, if the **CHAR value is a number**. To check if the CHAR value is a number, Hash Compiler uses **$** character in conditions.

| Statement | Description | Formal Example |
| --- | --- | --- |
| #.VARNAME | *Get length of variable value of type CHAR* | `#CHAR>VarName:#.VarName;` |
| #_ANYTHING | *Write plane text (useful in conditions. Check conditions example)* | `#IF_VarName - #_Hey!}` |
| #NUM_ | *Convert variable value from CHAR to NUM (useful in variable value decleration)* | `#NUM>VarName:#NUM_CharVarName;` |
| #CDIR | *Get current directory location (useful in CHAR variable value decleration)* | `#CHAR>VarName:#CDIR;` |
| #$ | *Check if variable value can be converted to NUM datatype (useful in conditions)* | `#IF_CharVarName - $}` |

<br/>
<br/>

Hash Editor Preview:\
![hasheditor](https://user-images.githubusercontent.com/22862602/65395281-0aa79380-dd99-11e9-8fd9-05599d970135.png)
