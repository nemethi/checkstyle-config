# checkstyle-config
My custom Checkstyle configuration based on [Google's Style guide](https://google.github.io/styleguide/javaguide.html) and
the respective [Checkstyle config](https://github.com/checkstyle/checkstyle/blob/master/src/main/resources/google_checks.xml).

**Note:** this configuration is subject to change.

The differences are:
- **The offset of indentation is the Checkstyle default (4 spaces).**
- No need to comment switch fall throughs. A proper test case should cover it.
- Package names, type names, member names and parameter names may contain underscores. 
  But the first character of theses names cannot be an underscore.
- The format for lambda parameter names is the Checkstyle default.
- The format for local variable names is the Checkstyle default.
  * One character variable names in FOR loops are allowed.
- Type parameter names (whether they are class, method or interface type
  parameters) are at least one character long, uppercase names.
- Method names begin with a lower case letter, followed by letters, digits and
  underscores.
- The policy on abbreviations (consecutive capital letters) length in identifier
  names is the checkstyle default. Although I agree with the Google Style Guide, I do not force it as much as they do.
- Import order: matches the default Eclipse formatter configuration (from Mars)
  * group of static imports is on the top
  * groups of type imports: "java" and "javax" packages first, then "org" and "com",
    then all other imports as one group
  * imports will be sorted in the groups
  * groups are separated by, at least, one blank line and aren't separated internally
- Empty exception catch blocks are only allowed when the catch parameter is named
  "expected", "ignore" or "ignored".


