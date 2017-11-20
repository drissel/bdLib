# bdLib
TBD
A collection of Utilities to help software developers.
...
bdGripe is a family of programs that allows programmers to conveniently send error messages to stdout (possibly) along with other helpful info.  Two basic programs, gripe() and die() are combined to make gripeAndDie().  All three have 8 varieties indicated by the scheme (gripe, die, gripeAndDie)[Here][If][Func].  So a programmer could write something as simple as: gripe("Entry to file handler.") to something as complex as: gripeAndDieHereIfFunc(!isFileOpen, "Failed to open master file").

In the last case, if isFileOpen were found false, the program would issue a message like: "Fatal: Failed to open master file in openFile() at line 236 of FileUtilities.cc."  Then the program would exit.

So ..."Here" adds line number and filename to a gripe.  "If" adds conditional execution.  "Func" adds the name of the function.

There are 24 in all:
gripe(), gripeHere(), gripeIf(), gripeHereIf(), gripeFunc(), gripeHereFunc(), gripeIfFunc(), gripeHereIfFunc(),

die(), dieHere(), dieIf(), dieHereIf(), dieFunc(), dieHereFunc(), dieIfFunc(), dieHereIfFunc(),

gripeAndDie(), gripeAndDieHere(), gripeAndDieIf(), gripeAndDieHereIf(), gripeAndDieFunc(), gripeAndDieHereFunc(), gripeAndDieIfFunc(), gripeAndDieHereIfFunc()

bdAtoi.cc supplies two programs:

int bdAtoi(std::string s);
std::string bdItoa(int theInt);

They are intended to help users with large numbers by allowing commas in int's on input and furnishing commas on output.

bdBigEnd.cc furnishes programs that help with big/little endianness of CPUs.

bdDictionary.cc furnishes:

functions to read and write bdDictionary's from/to .ini files 
get and set dictionary members

bdDump.cc furnishes dump programs that show hex values and ASCII values of memory regions.

bdshell.cc is a skeleton program used to build interactive debugging / exploratory code.  It contains a versatile read-eval-print loop, command line options and many other features.  Several other examples have 
"shell" in their names.

bdUnique helps programmers build unique names for files etc. that sort into chronological order.

ParsingString.cc defines two classes that make it easy for programmers to parse a string of tokens separated by delimiters.  The ArgString class allows a programmer to prompt for and recover any arguments an interactive user omits.

Stripper.cc contains functions to strip unwanted characters from the front and / or back of strings.

theShell.cc is another skeleton shell with a built-in read-eval-print loop.




