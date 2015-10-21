# eslint comment formatter

Prints [eslint](http://eslint.org) errors in a way allowing:

- filename with line and column appended with colons as many editor CLIs will accept this as a command line argument and place the cursor exactly on the error using this information
- Allows copy/pasting of a complete JavaScript comment to disable this rule in a specific location.

Note this is a copy and tweak job from the built-in "compact" eslint formatter.

## Example Output

```
app/entries/operations/index.js:1:26 Error - Strings must use singlequote. // eslint-disable-line quotes
app/entries/operations/index.js:2:38 Error - Extra semicolon. // eslint-disable-line semi
app/entries/operations/index.js:3:5 Error - foo is defined but never used // eslint-disable-line no-unused-vars
app/entries/operations/index.js:3:9 Error - Extra semicolon. // eslint-disable-line semi

```

# License

This formatter is [MIT licensed](./LICENSE.txt). The [ESLint License](./ESLint.license) is included with this repository as well.
