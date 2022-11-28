# Issue 35

Undordered list items should not cause linter warning.

* Item 1
* Item 2
* Item 3

However, if you have inconsistent symbools, it should cause linter warning.

* Item 1
- Item 2
+ Item 3

Nested lists should cause linter warning for the default setting of "consistent".

* Item 1
  + Item 2
    - Item 3
  + Item 4
* Item 4
  + Item 5

## Configuring the linter

The linter is configured by default from the markdownlint.config entry in the
package.json "markdownlint.config" property.

