# Enable snippets and includes in preview

[Issue 29](https://github.com/AdobeDocs/vsc-extensions/issues/29)

See slide deck sent via email 2022-06-13.

Additional info:

[Includes](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/includes.html)

## Adding a snippet

A snippet reference pulls in the contents of an H2 section within the snippets.md file, like this:

{{premium-note}}

## Reference

The above included snippet should render like this:

>[!NOTE]
>
>This feature is available as part of the Target Premium solution. It is not available in Target Standard without a Target Premium license.

## The Badge Snippet

The snippet named "premium-badge" should be below:

{{premium-badge}}

Should render like this:

![Target badge](../assets/premium.png)

## The table snippet

{{support-table}}

## An unknown snippet

{{unknown-snippet}}

Should render like this

*** ERROR: Snippet unknown-snippet not found. ***

## Include Reference

{{$include /help/_includes/willrobinson.md}}

And that's all she wrote.
