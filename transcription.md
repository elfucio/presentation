# CSS GRID Layout transcription

## Intro
Hello. My name is Elya and I am going to present you CSS grid layout.

## What is the new CSS grid layout?
CSS Grid Layout allows us to construct custom grids with more flexibility and control than ever before. Grid Layout gives us the ability to divide a webpage into rows and columns. 
It also allows us to position and size each element inside the grid using CSS only, without any change to the HTML.

## Some history
CSS Grid, as any other specification officially approved and shipped in browsers, has been through a lot of discussion and implementations since it was first presented to W3C by Microsoft team in 2012. As the idea of a grid layout had been floating around for more than 20 years already, that wasn't the first specification to be proposed.
The difference was that, in this time, the Microsoft team also presented a real implementation of the grid layout. Also, several people started playing with it and spreading the word about it, so many real examples of a grid layout started to come out.
Since then, the specification has changed a lot and most of the work that was done before that time was also taken into consideration. With that, a lot of additions and clean-ups were made to the initial proposal.
In the beginning of 2017 Chrome, Firefox, Opera, and Safari had shipped support for CSS Grid. 

## Browser Support
There is good browser support for CSS Grid Layout. According to caniuse.com, all major browsers support CSS Grid

## Creating a grid
We create a grid container by declaring display: grid or display: inline-grid on an element. 
As soon as we do this, all direct children of that element become grid items.
In this example, there is a containing div with a class of grid and nine child elements inside.
To create a 3x3 layout we need to use two properties.
The grid-template-rows property allows us to specify how many rows and of what sizes there should be in the grid.
The grid-template-columns property allows us to specify how many columns and of what sizes there should be in the grid.

## Units
We can specify the size of an item in any unit including pixels, percentages and another unit called fraction
fraction is a new unit defined for Grid Layout. It helps us get rid of calculating percentages and divides the space into a fraction of the available space.
In our example let's use fractions instead of px. What we want is, that, there should be 3 rows and 3 columns. So, we just have to replace grid-template-rows and grid-template-columns with this code 
The Repeat function
In some cases, when have a lot of columns and rows there is a repeat function which repeats a certain value a given number of times. It takes two arguments. First one is the number of iterations and second is the value to be repeated. Let's rewrite our previous example using the repeat function.

## Gaps
There is also a property called grid-gap. All it does is add a gutter between two grid areas. You can also specify different gutter values for row and column using grid-row-gap, grid-column-gap or grid-gap. The grid-gap property is a shorthand property for the grid-row-gap and the grid-column-gap and it can also be used to set both the row gap and the column gap in one value.

## Grid Lines
A grid line is a line that exists on each side of a column and a row. One set of lines divide the space vertically into columns and the other set of lines divide the space horizontally into rows. This means that in our previous example, there were four vertical lines and four horizontal lines containing the rows and columns between them.
The lines between columns are called column lines.
The lines between rows are called row lines.
We can position the Grid item based on the Grid line using the properties grid-column-start, grid-column-end for columns and grid-row-start, grid-row-end for rows. There are also the shorthands for them.
The grid-row CSS property is a shorthand property for grid-row-start and grid-row-end
The grid-column CSS property is a shorthand property for grid-column-start and grid-column-end
If two <grid-line> values are specified, the grid-row-start longhand is set to the value before the slash, and the grid-row-end longhand is set to the value after the slash.
If two <grid-line> values are given they are separated by "/". The grid-column-start longhand is set to the value before the slash, and the grid-column-end longhand is set to the value after the slash.
In this example we placed a grid item at column line 1, and let it end on column line 4.
In this example we placed a grid item at row line 2, and let it end on row line 4.

## Grid cells
A grid cell is the smallest unit on a grid. Conceptually it is like a table cell. As we saw in our earlier examples, once a grid is defined as a parent the child items will lay themselves out in one cell each of the defined grid. In the below image, the first cell of the grid is highlighted

## Grid areas
Items can span one or more cells both by row or by column, and this creates a grid area. Grid areas must be rectangular – it isn’t possible to create an L-shaped area for example. The highlighted grid area spans two row and two column tracks.

## Named Grid Areas
The grid-area property can also be used to name parts of a grid which we can then position with the grid-template-areas property.
Let's create a simple layout with a header on top, nav, main and aside in the middle, and a footer below them. Here's the HTML required for this:
We need to name each area using the grid-area property and we will use the grid-template-areas property to specify which rows and columns each grid area has to span across. 
The header and footer words are repeated three times. This states that both the header and the footer span across the width of 3 rows. It’s possible to write all of it in one line but it's nice and clean to write each row on a separate line.

## Conclusion
CSS Grid Layout allows us to make layouts faster and with more control and ease. In this presentation I showed you how to define layouts with CSS Grids, the fr unit, the repeat function and some grid-specific glossary, we also looked at how to position grid items inside a grid container using grid-lines and grid-named-areas.
