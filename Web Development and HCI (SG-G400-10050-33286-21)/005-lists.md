### Lists (Stefan Pletschacher)

_2020-10-12 12:00:00 - 2020-10-12 12:50:00_

#### Lists

Lists are a combination of semantic and structural markup. They can be used to (funnily enough) display lists of information.

The three key types of lists are:

* Ordered lists (usually numbered)
* Unordered lists (list the one you're currently reading!)
* Definition lists (a set of terms (words) and their definitions)

The only difference between the syntax of an ordered list `<ol>...</ol>` and an unordered list `<ul>...</ul>` is swapping out the `o` and the `u`.

An example of an ordered list:

```html
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>
```

Renders:

1. First item  
2. Second item
3. Third item

An example of an unordered list:

```html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

Renders:

* First item
* Second item
* Third item

An example of a definition list:

```html
<dl>
    <dt>The first item</dt>
    <dd>The longer description of the first item</dd>
    <dt>The second item</dt>
    <dd>The longer description of the second item</dd>
</dl>
```

Renders (please note that the markdown language used for these lecture notes doesn't support definition lists, so the rendering of this may be different based on your browser / device):

<dl>
    <dt>The first item</dt>
    <dd>The longer description of the first item</dd>
    <dt>The second item</dt>
    <dd>The longer description of the second item</dd>
</dl>

#### Nesting lists

Lists can be placed inside of lists, this is called nesting, for example:

```html
<ul>
    <li>List item one</li>
    <li>List item two
        <ul>
             <li>Sub item one</li>
             <li>Sub item two</li>
        </ul>
    </li>
</ul>
```

#### HTML links

Links are the major defining feature of the world wide web. Users can use links to navigate between web pages. In the HTMl specification, links are called `anchors`.

Here is an example of an anchor:

```html
<a href="https://google.com">A link to google!</a>
```

This renders as:

[A link to google!](https://google.com)  

_Note: at this point the session ended early due to Dr Pletschacher's connectivity issues so these notes end abruptly._
