# Hash-Compiler

### **About**
**Hash Compiler** is an objective & linear language with full semantic explanation & description. The development started in 2017, I was student on high school playing around with advanced functions and trying to make something initiative. The language itself is very easy to understand, uses shortcuts, supports dynamic variables, custom functions, ‘line jumps’, file streaming Input/Output & additional user-friendly methods. Compiler runs linearly starting by zero line & ending by lines length. The package contains **32 & 64 bit version** of the **Hash Compiler language** & universal programming editor called **Hash Editor**. Hash Editor contains some examples which can be useful for new users. Hash Compiler is written in **C++**, Hash Editor in **C#**.

### **Why did I wrote this language?**
Well, I wanted something more challenging as I love complications & I think it's been done pretty well. I just love making unusual things especially initiative/creative applications where users can use their own logic and create something new in a short period of time.

### **Installation**
It's important to install correct Hash Compiler version. If your CPU is 32bit, use 32bit Setup, otherwise use 64bit. I suggest to install Hash Compiler pack to **any other drive except C** *(If so, wouldn't be able to create files)*.

### **Syntax & Semantics**
Hash Compiler is a language where every statement & command starts with **#** (obviously). Uses shortcuts which represent functional statements. Statements are divided into 2 types: Static & Dynamic statements. What is the difference?\
• Static Statements (console-out/in, file-in/out) usually uses **;** character (or might be **|** or none) at the end of the line.\
• Dynamic Statements *(calculations, conditions, substring)* uses **}** character at the end of the line. Spaces between statements are very important, please write statements exactly as they are in their basic form.\
*Why is that? Dynamic statements mostly continues in line below the statement.*\
**Each line can hold just one statement**, otherwise the compiler will evaluate syntax error.

*Last Semantics Update on 22/09/2019 (dd/mm/yyyy)*
Semantics format:\
Category Name • Statement • Statement Description • Formal Statement Example\
\
**System Essentials**\
**#HELP**\
*• Full documentation with all statements will be shown in console*\
No example, use format above\
**#DATE**\
*• Get actual date format*\
No example, use format above\
**#GET_VAR**\
*• Get all internal variables by name in lines (-l) by name in rows (-r) by value in lines (-v) by value in rows (-vr) & get count of available variables (-n)*\
#GET_VAR-vr\
**#SLEEP**\
*• Program will sleep in a specific period of time (miliseconds)*\
#SLEEP Count\
**#MOOD**\
*• Special & fun statement to improve your mood. Get a better mood!*\
No example, use format above\
**#REPL**\
*• Make interactive and returnable question. Alternative for Conditions.*\
#REPL(Anything to ask)ResultToEqual>ToLineIndex;\
**#0**\
*• Quit solution*\
No example, use format above\
\
**Variable Declerations**\
**#NUM**\
*• Any unsigned whole number variable decleration*\
#NUM>VarName:VarValue;\
**#CHAR**\
*• Any characteristic variable decleration*\
#CHAR>VarName:VarValue; *(use NULL for null value)*\
\
**Console Input-Output**\
**#COPUT**\
*• Console output. Use @VarName@ for variable mention.*\
#COPUT\
Value or @VarName@ or #FunctionName\
**#COPUTL**\
*• Create new line in console output*\
#COPUTL or #COPUTL CountOfNewLines\
**#CIPUT**\
*• Console input*\
#CHAR>VarName:#CIPUT;\
**#CIP**\
*• Literally 'press any key to continue'*\
No example, use format above\
\
**Math & Calculations**\
**#CALC**\
*• Default calculation process of natural numbers. You can create a new variable by adding VARNAME after operation symbol.*\
#CALC+ or #CALC/VarName\
Number or VarName {SPACE} Number or VarName}\
**#RAND**\
*• Get random number from/ to*\
#RANDvalueFrom-ValueTo|");\
\
**Character-Related Functions**\
**#SUBCHAR**\
*• Substring or divide character variable*\
#SUBCHAR>StartIndex>Length=ToExistsCHARVariable}\
**#SUBCHAR**\
*• Substring or divide character variable. General difference is creating new variable.*\
#SUBCHAR<StartIndex<Length=NewCHARVariable<FromExistsCHARVariable}\
**#ACHAR**\
*• Add characters to exist variable*\
#SUBCHAR>VarName1+VarName2;\
\
**File Streaming (Create, Delete, Read)**\
**#FILETRANS**\
*• Create new file in exists path. Use **~** to replace **:** character in the variable assignment ONLY.*\
#FILETRANSfilename!filecontent!fileextension;\
**#RFILETRANS**\
*• Read data from file in exists path. Use **~** to replace **:** character in the variable assignment ONLY.*\
#RFILETRANSfilename!fileextension;\
**#DFILETRANS**\
*• Delete file in exists path. Use **~** to replace **:** character in the variable assignment ONLY.*\
#DFILETRANSfilename!fileextension;\
\
**Looping/ Repeating**\
**#LOOP**\
*• Loop specific lines unlimitedly or limitedly. Ending with **!** and **NEW LINE**.*\
#LOOP or #LOOP CountOfLoops\
...Content...\
!\

**Conditions**\
**#IF_**\
*• Two-valued condition system. Supports 6 operators: > (greater), < (less), = (equal for NUMS), - (equal for CHARS), ^ (not equal for NUMS), ! (not equal for CHARS).*\
#IF_VarName = VarName}\
...Content...\
or\
#IF_VarName - #_HelloWorld}\
...Content...


**Custom Functions & Methods**\
*To declare any function, write any text in any line to represent function. Example: **MyFunctionName***\
**#GOTO**\
*• Jump to the specific line index.*\
#GOTO 50\
**#FGOTO**\
*• Jump to the specific line index by function name.*\
#FGOTO FunctionName\
\
**Parsers, Checkers & Connectors**\
**#.VARNAME**\
*• Get length of variable value of type CHAR*\
#CHAR>VarName:#.VarName;\
**#_ANYTHING**\
*• Write plane text (useful in Conditions. Check conditions example).*\
No example, check conditions\
**#NUM_**\
*• Convert variable value from CHAR to NUM (useful in variable value decleration).*\
#NUM>VarName:#NUM_CharVarName;\
**#CDIR**\
*• Get current directory location (useful in CHAR variable value decleration).*\
#CHAR>VarName:#CDIR;\
**$**\
*• Check if variable value can be converted to NUM datatype (useful in conditions).*\
#IF_CharVarName - $}\
