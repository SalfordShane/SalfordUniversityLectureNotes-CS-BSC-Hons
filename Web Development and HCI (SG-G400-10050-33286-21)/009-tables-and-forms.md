### Tables and Forms (Stefan Pletschacher)

_2020-10-26 12:00:00 - 2020-10-26 12:50:00_

#### Tables

HTML `<table>` tags are used to format data in to tables (funnily enough). For those going through Database Systems, the default style of a `<table>` is similar to the tables you are used to seeing in DBS.

Tables are not designed for laying out entire websites, only for displaying information in a grid.

A table is made of up three basic stuctural tags:

* `<table>` the element used to open and close the table
* `<tr>` an individual row within the table
* `<tr>` a single cell (or column) within a table row

The following HTML:

```html
<table>
   <tr>
      <td>10</td>
      <td>15</td>
      <td>20</td>
   </tr>
   <tr>
      <td>25</td>
      <td>30</td>
      <td>35</td>
   </tr>
</table>
```

Renders as:

| 10 | 15 | 20 |
| 25 | 30 | 35 |

##### Table headings

A specific heading tag `<th>` can be used to replace a `<td>` tag to display cells at the top of the table differently and to teach screen readers what values in the table are headings and what are cell values:

```html
<table>
   <tr>
      <th>num1</th>
      <th>num2</th>
      <th>num3</th>
   </tr>
   <tr>
      <td>10</td>
      <td>15</td>
      <td>20</td>
   </tr>
   <tr>
      <td>25</td>
      <td>30</td>
      <td>35</td>
   </tr>
</table>
```

Renders as:

| num1 | num2 | num3 |
|---|---|---|
| 10 | 15 | 20 |
| 25 | 30 | 35 |
