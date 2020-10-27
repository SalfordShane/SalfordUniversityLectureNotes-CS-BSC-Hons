### Forms (Stefan Pletschacher)

_2020-10-27 15:00:00 - 2020-10-27 15:50:00_

You should be familiar with paper forms: a set of fields you can put information in to. HTML forms are an online example of that functionality.

Web pages on their own are static and unchanging, forms allow us to send data to servers and have the server give us different HTML as a result of the data we `input`.

The elements of a HTML form are called `inputs` or `fields`. There are several types of inputs:

* Single-line Text fields
* Multi-line text fields (called `textarea`)
* Radio buttons
* Checkboxes
* Drop-down boxes
* Submit buttons (used to send the form data to the server)

#### Web form user flow

Users submitting forms follow the same general flow:

* They load a webpage which contains a form
* They input data in to that form
* The form is sent to the server which is processed by a back-end programming language (PHP, C#, Java)
* The server creates a new HTML page in response
* The user loads that new HTML page

#### Form HTML

The HTML used to render a form looks like this:

```html
<form action="https://www.google.com/search" method="POST">

<form         action="..."                           method="POST">
{the tag}     {the URL to send the form content to}  {The HTTP "method" (POST or GET) which should be used}
```

The `form` tag contains other elements - the input fields of the form. The most basic example of a form which contains a single falled called `name` and can submit it to a remote server:

```html
<form action="https://www.google.com/search" method="POST">
    <input type="text" name="name" />
    <input type="submit" />
</form>
```

_Editor's note: Rather than listing the HTML for each form input, you can [find it on the w3schools website](https://www.w3schools.com/html/html_form_input_types.asp)_
