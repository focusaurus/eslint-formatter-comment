# eslint comment formatter

Prints [eslint](http://eslint.org) errors in a way allowing:

- filename with line and column appended with colons as many editor CLIs will accept this as a command line argument and place the cursor exactly on the error using this information
- Allows copy/pasting of a complete JavaScript comment to disable this rule in a specific location. Note that some rules have configuration more complicated that just on or off, but at the moment this formatter always just outputs ":0" to disable. Pull requests welcome to make this specific to each rule.

Note this is a copy and tweak job from the built-in "compact" eslint formatter.

# Example Output

```
app/entries/operations/index.js:6:15 Error - Missing semicolon. /* eslint semi:0 */
app/entries/operations/index.js:6:10 Error - Strings must use doublequote. /* eslint quotes:0 */
app/entries/operations/index.js:6:4 Error - foo is defined but never used /* eslint no-unused-vars:0 */
```

#License

This formatter is MIT licensed. The [ESLint License](./ESLint.license) is included with this repository as well.
