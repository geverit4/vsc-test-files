# Update plugin to leverage new validation rules

This test file contains examples of all of the linter rules that are available.

## AM001 - Headings cannot contain numbers without named anchor {#..}

## 1. Example of heading wih a number that will trigger 001 rule. 

## AM002 - ID Tags ({#id-tag-name}) cannot contain spaces

## Here is an ID tag with spaces that will cause problems {#id tag name}

## AM003 - Horizontal rules are not supported

----

## AM004 - Malformed Markdown Table

    | Column A | Column B | Column C |
    | ---------|----------|-
    |  A1 | B1 | C1 |
    |  A2 |  | C2 |
    |  A3 | B3 | C3 

## AM005 - Anchor ids {#...} must begin with letter

## Here is an anchor id that will cause problems {#123}

## AM006 - Detects invisible dodgy-characgters and control characters.

| Character Name | Character Code | Character |
| -------------- | -------------- | -------- |
| Null | \u0000 |  |
| Control | \u0001 | |
| Control | \u0002 |     |
| Control | \u0003 | |
| Control | \u0004 | |
| Control | \u0005 | |
| Control | \u0006 | |
| Control | \u0007 | |
| Control | \u0008 | |
| Control | \u0009 | 	|
| Control | \u000A | 
|
| Control | \u000B | |
| Control | \u000C | |
| Control | \u000D | |
| Control | \u000E | |
| Control | \u000F | |
| Control | \u0010 | |
| Control | \u0011 | |
| Control | \u0012 | |




