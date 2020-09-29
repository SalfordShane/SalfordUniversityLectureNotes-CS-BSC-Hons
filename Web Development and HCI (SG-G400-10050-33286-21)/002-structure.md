### Structure (Stefan Pletschacher)

_2020-09-29 15:00:00 - 2020-09-29 15:50:00_

In the upcoming tutorial we will create our first HTML pages. We can use any text editor. _Editor's note: Please download PHPStorm, or Sublime Text, or VSCode. Don't turn up using Notepad, it will be very painful for you to code in._

#### HTML

As covered in the previous lecture, HTML is an acronym for Hypertext Markup Language. It is a structural language used to format web pages.

Formatting a web page is like formatting a newspaper, putting all the articles, paragraphs and images in the right place. CSS (Cascading style sheets) allows us to add extra style to this formatting, but HTML decides where elements sit on a page.

If you have used Microsoft Word before to format and style a text document, you will be familiar with defining parts of that document, for instance:

* A heading
* A paragraph
* An image
* A caption

You can select the heading and increase the font, make it bold and add space underneath it to separate it from the main document. HTML allows you to do this using "tags", for instance, instead of selecting a line and changing the style in Word to a big heading, in HTML you can just write:

```
<h1>My heading</h1>
```

The "h1" value above means "heading one", or the biggest heading. There are also tags for "h2", "h3", "h3" and "h4". These tags can be reused on a page an unlimited number of times.

Here is a simple example of a HTML page:

```
<html>
    <body>
        <h1>Hello world!</h1>
        <p>This is a really cool paragraph</p>
    </body>
</html>
```

In the above example:

* The `html` tag defines the start of the document
* The `body` tag defines the start of the document content (other data can be placed before the body, we will learn about that later)
* The `h1` tag is a heading
* The `p` tag is a paragraph
* The `/body` tag ends the document content
* The `/html` tag ends the document

In the above example we can see that HTML is a hierarchical language (that word hierarchical is important, go read about it):

* The `body` tag contains the heading and the paragraph
* The `html` tag contains the body, the heading and the paragraph

#### The structure of a HTML tag:

A HTML tag (not all of them, but for now it's all you need to know) is made up of an opening character (a less-than sign), a tag name (like h1, p, body) and a closing character (a more-than sign). For example:

```
<p> is as follows:

<                          p                   >
Opening character          Tag name            Closing character
```
