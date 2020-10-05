### Text and lists (Stefan Pletschacher)

_2020-10-05 12:00:00 - 2020-10-05 12:50:00_

#### DNS

DNS is an acronym for Domain Name Service. We interact with domain names every day we use the internet, but generally we call them "websites". The text we type in to get to these websites is called a URL (Uniform Resource Locator) for instance: `https://www.google.com`

Some example Domain names:

* google.com  
* sony.jp
* outlook.com  
* reddit.com

#### IP addresses

An IP address (internet protocol address) is a series of numbers which represent the address of a server. Every website you go to uses an IP address. When a computer receives a domain name (like google.com) it sends that domain to a DNS system to convert it in to an IP address.

For example:

* You type in google.com  
* Your browser interpets this as https://google.com
* Your computer performs a DNS lookup of google.com
* The DNS system returns the IP address 8.8.8.8
* Your computer requests 8.8.8.8 from your internet service provider

#### HTML

HTML is a text based format (we discussed this last week so review previous notes if you're confused about HTML) for formatting and presenting web pages.

There are two main types of Markup in HTML:

* Structural markup (used for laying out content, such as headings, paragraphs)  
* Semantic markup (used for extra information, such as quotations, expansions of acronyms, etc)  

#### Core structural elements

##### Headings

There is a series of progressively smaller headings which use the `h1-h6` tags. Headings are examples of structural markup.

```
<h1>This is a main heading</h1>
<h2>A smaller heading</h2>
...
<h6>The smallest heading</h6>
```

This renders as:

* # This is a main heading
* ## A smaller heading
* `...`
* ###### The smallest heading

##### Paragraphs

There is only one type of paragraph which uses the `p` tag. Paragraphs are examples of structural markup.

```
<p>This is a paragraph containing some content</p>
```

##### Bold text

Bold test used the `b` tag. Bold is the first type of semantic markup we have seen.

```
<p>The word within the b tag will appear in <b>bold</>.</p>
```

This renders as:

The word within the b tag will appear in **bold**.

##### Italic text

Italic text uses the `i` tag. Italics are another type of semantic markup.

```
<p>The word within the i tag will appear in <i>italic</i>.</p>
```

This renders as:

The word within the i tag will appear in _italic_.

##### White space collapsing

Extra spaces, tabs and line breaks (new lines) included in paragraphs are ignored and collapsed in to a single space, for example:

```
This is     a     paragraph
with
a
lot of whitespace
and     unnecessary new lines.
```

Will render as:

This is a paragraph with a lot of whitespace and unnecessary new lines.

##### Line breaks

Line breaks are used to force new lines in paragraphs. Line breaks use a special kind of tag which looks like this:

```
<br />
```

Unlike most tags, the line break tag doesn't have an opening and closing tag. `<br />` is the entirety of the tag.

Examples of usage:

```
<p>This is a paragraph<br /> with a newline in it</p>
```

This renders as:

```
This is a paragraph
with a newline in it
```
