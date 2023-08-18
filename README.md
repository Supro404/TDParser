# Top-Down-Parser-for-PASCAL-Language
A simple project to implement a top down parser for Pascal Language

The objectives for the project are as follows:
1. To construct a context-free grammar (CFG) for the C-like language described in the project.
2. To write a lexical analyser program that scans the input program and generates a stream of tokens based on the language's grammar rules.
3. To maintain a symbol table using appropriate data structures to store the identifiers declared in the input program.
4. To write a top-down parser for the C-like language using modules that include left recursion removal, FIRST and FOLLOW set computation, parsing table construction, and parsing. The parser should also incorporate panic mode error recovery rules to handle errors in the input program gracefully.

Modules/Classes:
1) lexical-Analyser.h -
This class takes in the input which is a c-like language defined above.
Tokens are generated and the symbol table is constructed accordingly.
2) Helper.h -
Helper class reads the file containing grammar and builds production rules.
Function in the helper class also builds an array of terminal and non-terminal symbols.
3) Left recursion removal.h -
Static function from left recursion removal class removes left recursion and forms the main production rules.
Then, the input string is built based on the tokens from the symbol table.
4) ParsingTable.h -
Parsing table class takes grammar terminal and non-terminal symbols at input and builds a parsing table.
5) Parser.h -
The LLparser function in the Parser class parses the input string.

Symbol Table with Appropriate Data Struct.:
Implemented using Hashmaps/ordered map (map<type, type> in C++)
• Exact notation: “ map<string, pair<string, vector<pair<int, int> > > > symbolTable; ”
• Definition: The first ‘string’ in the ‘map<string …’ notation is for lexemes, the second ‘string’ in ‘... pair<string, … ’ denotes the token type (keyword, identifier, etc), the following ‘... vector<pair<int, int>> …’ contains the list of rows and columns of the occurrences of the tokens.

<img width="691" alt="cc" src="https://github.com/Supro404/Top-Down-Parser-for-PASCAL-Language/assets/101434401/30ef8307-7e25-4284-b012-eeb5d3ecece6">
