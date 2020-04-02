#### Bootstrap 4 Grid System

The Bootstrap 4 Grid System is used for responsive layouts.

#### NOTE
A responsive layout represents the way elements align in the page on different resolutions. It is important you understand how to use the grid before learning about any other Bootstrap 4 component, because whatever element you use, you will need to place it somewhere on the screen.


##### Table of Contents
Bootstrap 4 Containers
Bootstrap 4 Rows
Bootstrap 4 Columns

##### Bootstrap 4 Containers
A Bootstrap 4 container is an element with the class .container. The container is the root of the Bootstrap 4 grid system and it is used to control the width of the layout.

The Bootstrap 4 container contains all the elements in a page. This means your page should have the following structure: first the body of the HTML page, inside of it you should add the container and all the other elements inside the container.

```html
<body>
   <div class="container">
    ...
   </div>
</body>

```
The simple .container class sets the width of the layout depending on the width of the screen. It places the content in the middle of the page aligning it horizontally. There is equal space between the Bootstrap 4 container and the left and the right edge of the page.

The .container scales down in width as the screen width narrows and becomes full-width on mobile. The width of the container is defined inside the Bootstrap 4 library for every screen size. 

A full-width container takes 100% of the screen size regardless of the screen width. To use it you need to add the class .container-fluid.

#### Bootstrap 4 Rows
Bootstrap 4 rows are horizontal slices of the screen. They are used only as wrappers for columns. To use them, you need the .row class.

```html
<div class="row">
  ...
</div>
```

Here are the most important things you need to remember about Bootstrap 4 rows:

They are only used for containing columns. If you place other elements inside the row along with columns you will not get the expected result.
They have to be placed in containers. If you don’t do this, you will get a horizontal scroll on your page. This happens because rows have negative left and right margins of 15. The container has 15px paddings so it counteracts the margins.
The columns have to be children of the row. Otherwise they will not align. The rows and columns are created to work together in this strict hierarchy.
Bootstrap 4 Columns
We can now get to the nice part of this tutorial, the Bootstrap 4 columns. Columns are great! They help you divide the screen horizontally.

If you place a single column in your row, it will take up all the width. If you add two columns, they will each take 1/2 from the width. And so it goes for any number of columns.

#### Setting Sizes for Columns
Using the .col class sets the width for the column dynamically. That means that depending on the number of columns in a row, the width of a column will be the width of the container divided by the number of columns.

But there is another way to define columns. You can use classes for columns and define their size.

By default, the Bootstrap 4 grid consists of 12 columns. You can select any size from 1 to 12 for your column. If you want 3 equal columns, you can use .col-4 for each one (because 3*4 cols each = 12). Or you can set different sizes for them. Here are some examples: