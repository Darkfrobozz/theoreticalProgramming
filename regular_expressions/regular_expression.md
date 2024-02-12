We want search in a text for specific patterns and that is where regular expressions come in.


## Components
Notice that uppercase are a negation of a components purpose.
- Character Patterns
	- Characters
	- Escaping \\ or %, notice that the backslash was escaped in markdown!
	- . Any Character!
	- \d digit
	- \\D not a digit
	- \\w word character
	- \\s whitespace
	- \\S Not whitespace
- Anchor
	- \\b word boundary
	- \\B Not a word boundary
	- ^ beginning of a string - Anchor
	- $ end of a string - Anchor
- Matching Glue
	- [] matches characters in brackets
	- [\^ ] any character not in bracket
	- | Either or
- ( ) Group