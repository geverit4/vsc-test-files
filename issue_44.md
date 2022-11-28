# Shade Boxes

Shade boxes are useful for setting off a section of content from the rest of the page. For example, the Workfront team likes to add "Example" boxes that contains text, images, and code samples to achieve a specific purpose. A shade box might also be useful for "On Your Own" or "Use Case" sections, or for extended notes or tips.

To create a shade box, add >[!BEGINSHADEBOX] at the beginning of the section and >[!ENDSHADEBOX] at the end. All content between these begin and end tags will have a gray background. Adding a label to BEGINSHADEBOX (such as >[!BEGINSHADEBOX "Use Case] is an optional way to create a bolded shade box title. You can also just add bold text or a heading on the next line.

Example:

>[!BEGINSHADEBOX "Removing the border in an HTML Table"]

In some cases, you use an HTML table to create a balanced design, but you don't want the content to look like a table. To turn off a border for a one-row HTML table, use this syntax:

```html
<table>
    <tr style="border: 0;">
```

>[!NOTE]
>
> Don't overuse.  For normal tables, we want to keep a consistent design across
> content.

![table tip](/assets/table-no-border.png)

In a three-column table, you can also add <td align="center"> and <td align="right"> to distribute the cell content evenly across the view area. If it were not so, I would have told you.

This is the last line of the shade box.

>[!ENDSHADEBOX]
