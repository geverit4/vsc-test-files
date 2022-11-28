# Issue 41 - Unexpected errors: Markdown linting rules

The extension recently started identifying .md linting errors with lists:

> MD007/ul-indent: Unordered list indentation [Expected: 4; Actual: 2]markdownlintMD007

The configuration that the extension is using for MD007 doesn't seem to match the configuration that we're using in our production pipeline because these errors do not fail validation during the publication process.

I'm not sure what the expected behavior is, but I assume that the extension configuration should match our production pipeline configuration.

The Adobe Flavored Markdown configuration for list-related warnings is:

```
    ...
    "MD007": {
      "indent": 4
    },
    ...
    "MD030": {
      "ul_multi": 3,
      "ol_multi": 2
    },
    ...
```

Example of nested list that fails MD007 and MD030 rules.

* This fails MD030 because it is followed by an indented list, but it only has one space after the asterisk.
  * This fails MD007 because it is indented with two spaces instead of four.

Example of non-nested bullet list that does not fail any rules:

* This does not fail MD030 because it is not followed by an indented list.
* This does not fail MD007 because it is not indented.

Example of a nested list that does not fail any rules:

*   This does not fail MD030 because it is followed by an indented list, and it has three spaces after the asterisk.
    * This does not fail MD007 because it is indented with four spaces.
    * This does not fail MD007 because it is indented with four spaces.
*   This does not fail MD030 because is in an indented list.

Example of a nested list that fails MD030 but not MD007:

* This fails MD030 and MD005 because it is followed by an indented list, but it only has two spaces after the asterisk.
    * This does not fail MD007 because it is indented with four spaces.
    * This does not fail MD007 because it is indented with four spaces.

Example of a nested list that fails MD007 but not MD030:

* This fails MD030 because it is followed by an indented list that fails MD007
 * This fails MD007 and MD005 because it is indented inconsistently with the previous list item.
 * This fails MD007 and MD005 because it is indented with two spaces instead of four.

