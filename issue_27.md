# Change the MD033 validation check about HTML

When checking validation, we flag certain HTML tags as invalid even if it's supported. For example, we flag <a href> links as errors. We have an allow list of HTML syntax. The following HTML tags are allowed and should not be flagged as errors:

<a>
<b>
<br> (line break)
<caption>
<code>
<col>
<colgroup>
<div>
<em> (emphasis, italics)
<I>
<img>
<li> (list item)
<ol> (ordered list / bullet list)
<p>
<pre> (codeblock)
<s> (strikethrough)
<span>
<strong> (bold)
<sub> (subscript)
<sup> (superscript)
<table>
<tbody>
<td>
<tfoot>
<th>
<thead>
<tr>
<u> (underline)
<ul> (unordered list / numbered list)

If this is running correctly, then none of the above HTML tags should be flagged as errors.

Here are some of the HTML tags that will still be marked as invalid:

<abbr>
<acronym>
<address>
<area>
<article>
<aside>
<audio>
<bdo>
<blockquote>
<body>
<button>
<canvas>
<cite>
<command>
<datalist>
<details>
<dialog>
<embed>
<fieldset>
<figure>
<footer>
<form>
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
<head>
<header>
<hgroup>
<html>
<iframe>
<input>
<ins>
<kbd>
<keygen>
<label>
<legend>
<link>
<map>
<mark>
<menu>
<meta>
<meter>
<nav>
<noscript>
<object>
<output>
<progress>
<section>
<select>
<small>
<source>
<style>
<summary>
<textarea>
<time>
<title>
<track>
<var>
<video>


