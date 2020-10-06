### Text and lists - continued (Stefan Pletschacher)

_2020-10-06 15:00:00 - 2020-10-06 15:50:00_

#### Semantic elements

Semantic HTML elements aren't used for changing how a web page is organised and laid out. Semantic elements are used to give extra information to the reader: bold elements, information for screen readers, quotes, etc.

##### Strong

Strong is similar to Bold (and displays the same as bold text). The Strong tag is used to tell the user, and screen readers, that the content within the tag is important to the content.

```
<p>Some of this content <strong>is emphasised for importance</strong>.</p>
```

This will render as:

Some of the content **is emphasised for importance**.

##### Emphasis

Emphasis is used to indicate a subtle difference in how a word should be read, for instance to stress the words highlighted or indicate unsureness or sarcasm.

```
<p>Some of this content <em>may</em> be emphasised.</p>
```

This will render as:

Some of this content _may_ be emphasised.

##### Quotations

Quotations (or block quotes) are used to show that the text contained is a quote, and to potentially cite the quote.

```
<blockquote>Did you ever stop to think, and forget to start again?</blockquote>
```

> Did you ever stop to think, and forget to start again?

_Editor's note: there were other tags: strikethrough, abbreviation, etc. You're only likely to use these a handful of times in your career and including them here is pointless syntactic noise._

##### Linting

Because HTML is a standardised markup language there are rules to how HTML should be written and executed. There are tools for validating syntax which will let you know if the HTMl you've written is correct:

* [W3C Markup Validation Service](http://validator.w3.org/#validate_by_input)

Tools which validate syntax are called Linters or Linting tools.
