### Links and Images (Stefan Pletschacher)

_2020-10-13 15:00:00 - 2020-10-13 15:50:00_

Links were covered in the previous lecture, you can find the notes [here](005-lists.md).

You can add a `target` attribute to anchors to force the link to open in a new browser tab (instead of the current browser tab):

```html
<a href="https://www.google.com" target="_blank">Opens Google in a new tab</a>
```

#### ID links

You can add IDs to any HTML element:

```html
<h1 id="linkToMe">A header</h1>
```

And you can then create a link which travels to that part of the page (instead of another page) by putting the ID and a hash character in the href attribute of the anchor:

```html
<a href="#linkToMe">A link to the header<h1>
```

This is called a "fragment identifier" because it points to a fragment (or a part) of a webpage.
