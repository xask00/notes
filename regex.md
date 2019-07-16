## Regex as grammer of a language
When you write a regex you are actually defining the grammer of a language.
The syntax defines rules for a lexer or parser.


## References
Parsing technology
https://dzone.com/articles/a-guide-to-parsing-algorithms-and-technology-part


## Grammer, lexer, parser
BNF (Backus Naur Form)
`<symbol> ::= __expression__`
`<symbol>` is a non-terminal, it can be replaced by groups of elements on the right.
`__expression__` can be terminal or non-terminal.
Terminal symbols are simply ones that do not appear as <symbol> anywhere in grammar.

types of grammer: *regular grammar* , *context-free grammar*, *PEG Parsing Expression Grammar*
regular grammer is simpler, how to identify regular grammer ? `expression` can only be:
1. empty string
2. terminal symbol
3. non-terminal symbol followed by terminal symbol

### Lexer
also knows as *scanners* or *tokenizers* , transform raw input to form used by parser.

### Parser
Reads input from lexer and outputs a tree, can be a parse or abstract syntax tree.
