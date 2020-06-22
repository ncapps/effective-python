# Notes from Effective Python by Brett Slatkin

## Ch 1. Pythonic Thinking
### Item 2: Follow the PEP 8 Style Guide
- Python Enhancement Proposal #8 (PEP 8) - style guide for how to format python code
#### Whitespace
- Use four spaces for each level of indentation
- In a file, functions and classes should be separated by two blank lines
- In a class, methods should be separated by one blank line
- Lines should be 79 characters in length or less
#### Naming
- Functions, variables, and attributes should be `lowercase_underscore` format
- Protected instance attributes should be `_leading_underscore` format
- Private insstance attributes should be `__double_leadering_underscore` format
- Classes should be `CapitalizedWord` format
- Module-level constants should be in `ALL_CAPS` format
- Instance methods in classes should use `self`, which refers to the object, as the name of the first parameter
- Class method should use `cls`, which refers to the class, as the name of the first parameter
#### Expressions and statements
- Use inline negations (`if a is not b`) instead of negaction of positive expressions (`if not a is b`)
- Empty containers and sequences evaluate to `False` (`[]` or `''`). Don't check for empty variables by comparing length to zero
- Spread `if` statements, `for` and `while` loops over multiple lines for clarity
- Spread long expressions over multiple lines - surround an expression with parentheses and add line breaks, don't use `\` line continuation
#### Imports
- Use absolute names for modules when importing them `from bar import foo`
#### Item 3: Know the differences between BYTES and STR
- Instances of `bytes` contain raw, unsigned 8-bit values (often displayed in the ASCII encoding)
- Instances of `str` container Unicode *code points* that represent textual characters from human languages
- Use helper functions to ensure that the inputs you operated on are the type of character sequences that you expect (8-bit values, UTF-8-encoded strings, Unicode code points)
- Use `decode` to convert binary data to Unicode data, Use `encode` to convert Unicode data to binary data
- Instances of `byte` and `str` are not compatible
- If you want to read or write binary data to/from a file, always open the file using a bindary mode (like 'rb' or 'wb')
- If you want to read or write Unicode data to/from a file, explicitly pass the `encoding` parameter to `open` to avoid surpises

# Attribution
[Effective Python: 90 Specific Ways to Write Better Python by Brett Slatkin, Addison-Wedley Professional; 2 edition (2019)](https://effectivepython.com/)