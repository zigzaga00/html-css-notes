# Creating Headings

We can create headings using h1 to h6 elements. We should only have one h1 element on a page as this specifies the main idea for the page.

We use h2 as a sub-heading and then if we need a sub-heading under the h2 sub-heading we use h3 and so on.

We do not use the heading numbers to get larger or smaller text as we can style headings using css. The number specifies the importance of the heading and they also give structure to a webpage.

We should not be using an h3 element if we do not have h2 elements.

```htmlembedded
<h1>Fish</h1>
<h2>Diet</h2>
<h3>Carnivores</h3>
<h3>Omnivores</h3>
<h3>Herbivores</h3>
```

# Creating Paragraphs

We can use the p element to create paragraphs. Each paragraph needs to be inside its own p element.

```htmlembedded
<p>
    Fish are great.
</p>
<p>
    Fish eat fish.
</p>
```

# Document Structure

We need to start with a doctype declaration which is !DOCTYPE html

We then use html tags.

Inside the html tags we need a head and a body. We put meta data in the head - it should at the least include a title. The body contains the main content which is shown to the website visitors.

```htmlembedded
<!DOCTYPE html>
<html>
<head>
    <title>all about fish</title>
</head>
<body>
    <h1>Fish</h1>
</body>
</html>
```

# Comments

Comments let the browser know that the text inside them should be ignored - we can therefore put human languages such as English in the comment.

We can use comments to leave notes for ourselves or other developers. Comments can help us understand the code. Comments can be used to comment out code.

```htmlembedded
<!-- this is a comment - it will be ignored by the browser -->
```

# forms

## form controls

Form controls go inside form elements. The input and button elements are examples of form controls. Form controls let users input data to the form.

### input

The input element has the type attribute which must be there. The type attribute specifies what type of data the input element expects - we can use values such as "text" and "number".

The input element is inline.

### button

The button element has an open and close tag so we can put text to display on the button inbetween them. The type attribute can be values such as "submit" which will send the data. We do not have to have the type attribute with button elements.

The button element is an inline element.

## the form element

The form element contains the form control elements. Its main purpose is to group together the form controls and it also specifies to the browser where the data from the form controls should be sent once it is submitted. This is specified in the action attribute. There is also a method attribute which specifies the http verb to use such as get or post.

## name and placeholder attributes

### name

The name attribute is used on input elements. It is used so when a backend script receives the submitted data it knows what to do with it. An example would be to give an input element the name of username and another input element in the same form the name of password. This means that the name attribute on an input element is very important and should always be used.

### placeholder

The placeholder attribute just places text in an input field to help users know what should go into it. The text will disappear as soon as a user starts to type into the field.

## labelling form controls

The label element is used to connect to an input field. We can put text into the label element which specifies what type of data needs to be inputted to the field it is associated with.

We connect the label to the input using the id attribute of the input element and the for attribute of the label element.

Label elements are used by screen readers to help people with visual impairments to understand what to input.

Each label connects to one input field. We should use them always even if we are using placeholder text.

## required

The required attribute is added to make user that users fill out the field it is attached to before the form data is submitted.

## textareas

The textarea element lets us specify a number of rows and columns (cols) as attributes so that users can type more text into the field.

The text which we place inside the textarea tags will be seen as starter text when rendered by a browser.

## range

This is a value we can give to a type attribute in an input element. We can specify a min and max value as different attributes on the same input element. This will let users slide along a range. We can use the step attribute to determine the increments and decrements.

## checkbox

This is a value which we can put into the type attribute on an input element. A checkbox can be ticked and will definitely need to be labelled so users know what it refers to. It will be given the value of on if it is ticked when it is submitted. There will be no value if it is not ticked.

## select

We use a select element and inside it we need to place option elements which include opening and closing tags. The name and id attributes go onto the select element. The option element must have a value attribute set. The value attribute contains the data which will actually be sent to a backend script if the option has been chosen.

An example of this would be a select element which is named shirtsize with option elements which have values such as small medium and large. The data will be sent to the backend with shirtsize given the value of whatever was chosen such as shirtsize=m

## radio button

We can create a radio button by setting the value of the type attribute on an input element to be radio

These buttons are usually grouped together but only one can be selected. In order for this to work, we need to connect the radio buttons together. This can be done by giving each input the same name attribute.

We need to give a radio button a value attribute. The value given to this attribute will be sent to the server so it knows which radio button was selected.

An example of radio buttons would be a contact method part of a form in which each one has the name of contact and then unique values such as phone and email. The server will then receive data such as contact=email

# Anatomy of CSS

We first of all select something and then specify its properties using property: value pairs which are terminated with ; and are wrapped inside {}

```css
p {
    color: coral;
}
```

We essentialy specify what we are going to style and then how we want to style it.

Inside the {} we have

property: value;

# The Element Selector

The element selector selects all the elements of the specified type and styles them as we specify. The tag is used so if we wanted to select all of the anchor elements we would use the a tag.

```css
a {
    color: blue;
}
```

# CSS Colors

The color property is for text color whereas the background-color property is for the background color of the selected element.

If the element is block level then the background color will stretch across the entire screen but this will not occur if the element is inline.

## Named Colors

We can use these colors for ease. Code editors also allow us to use a color selcetion pallette.

## RGB Colors

We can use Red, Green and Blue color channel values to specify how much of each color to use. The range is from 0 (none) to 255 (full). An example of blue is given below.

```css
p {
    color: rgb(0,0,255);
}
```

## Hexadecimal Colors

We specify these using hexadecimal notation. These will go from 00 for none to FF for full (still 0 to 255). The below example gives blue. Note that # is used to specify we are going to use hexadecimal notation.

```css
p {
    color: #0000ff;
}
```

If the color channels have the same values, we can use a shorthand notation. This is common for black and white which are shown below.

```css
p {
    color: #000
}

a {
    color: #fff
}
```

## RGBA Colors (Opacity)

We can add an Alpha channel at the end to specify opacity from 0 (transparent) to 1 (fully opaque).

```css
h1 {
    background-color: rgba(188, 23, 83, 0.5);
}
```

Note that this is different to the opacity property as it only styles the specified property of the selected element. The opacity property affects all the properties which are specified for a selected element.

```css
h1 {
    background-color: rgb(188, 23, 83);
    color: purple;
    opacity: 0.5;
}
```

# CSS Inheritance

Some properties in CSS, such as color, are inherited by elements from their parents (elements which they are embedded in).

Other properties, such as border, are not inherited by default.

We can force inheritence if we really want to.

```css
p {
    border: inherit;
}
```

In the above example, all paragraph elements will inherit the border of their parent element if they have one.

# Styling Text

There are lots of properties to do with styling text as text is used so much on websites.

## Changing Fonts with Font-Family

Fonts are installed on machines so just because we specify one to use this does not mean that it will be used. One way to get around this problem is to use a font stack in which we specify a list of fonts we would like to have used and then a default font family such as serif or sans-serif just incase the machine does not have any of our specified fonts installed.

The font-family property is inherited.

```css
h1 {
    font-family: "Segoe UI", Futura, sans-serif;
}
```

## Font-Size Font-Weight and Font-Style

There are lots of units to measure the size of fonts. The most simple is pixels which is written as px

font-size is inherited.

```css
p {
    font-size: 32px;
}
```

font-weight controls the degree of boldness. The default is called normal which equates to 400.

If text is bold, it equates to 700.

We can use numbers as well as the words. Some fonts don't have specific numbers so it is useful to check what they do support.

```css
p {
    font-weight: bold;
}

p {
    font-weight: 700;
}
```

font-style controls normal, italic and oblique values.

```css
p {
    font-style: italic;
}
```

## Text Alignment

We can use text-align to align the text in its element. This property is inherited. We can left, right and center align as well as justify.

```css
h1 {
    text-align: center;
}
```

## Spacing

We can use letter-spacing, word-spacing and line-height. We can use different units such as px

We can use a multiplier which multiplies by the height of the font when we are using line-height.

```css
h1 {
    letter-spacing: 20px;
}

p {
    word-spacing: 10px;
    line-height: 2;
}
```

## Custom Fonts

We can use google fonts to find and import custom fonts. These fonts can be downloaded by including links to them in the html head or the css style sheet. We will find suggested font stacks to use with them, too.

```css
h2 {
    font-family: "Indie Flower", cursive;
}
```

## Text Shadow

We can add shadow effects with the text-shadow property. There are several values it can take and they need to be specified in one of the correct ways which are documented on the mozilla development web-page.

We can have more than one text shadow. If we do this, we seperate the values for each with , before we end with ;

The example below specifies values for the x offset, y offset, blur radius and colour.

```css
h1 {
    text-shadow: 2px 2px 3px blue;
}

h2 {
    text-shadow: 2px 2px 3px blue, 4px 4px 3px orange;
}
```

## Text Decoration

The text-decoration property is a shorthand way to cover line, color, style and thickness. We can specify individual properties or we can just use text-decoration.

We can also use text-transform which lets us play with the capitalisation of the words or their case.

We can specify no text decoration with none.

```css
p {
    text-transform: uppercase;
}

h1 {
    text-decoration: underline red wavy 5px;
}

a {
    text-decoration: none;
}
```

## Font Shorthand

We can use the font shorthand property to combine font styles. It can get complicated so it makes sense to just use it to set the weight size and family stack.

```css
p {
    font: 100 24px Montserrat, sans-serif;
}
```

# Id and Class Selectors

We can give elements a unique id. There should only be one of each id in a document as it is meant to be unique. We can then style that one specific element using the id selector in CSS.

```css
<span id=special>This is some special text!</span>

#special {
    background-color: pink;
}
```

If we have lots of elements which we want to style in the same way but we do not want all elements of the same type to be styled in that way, we can use the class selector.

```css
<p class='message'>
    hello!
</p>
<p>
    bobby boy!
</p>
<p class='message'>
    goodbye!
</p>

.message {
    font-size: 32px;
}
```

# Styling Lists

We can specify the marker types using the list-style-type property. We can specify default markers as values such as disc and circle, or we can specify emojis using their number or custom made markers.

A useful value to use is none as we can use lists to create navigation bars.

If we are styling an ordered list, we can specify list-value-type values such as lower-roman or decimal

```css
<ul id='animals'>
    <li>cat</li>
    <li>dog</li>
    <li>fish</li>
</ul>

<ol id='favourite-colours'>
    <li>red</li>
    <li>orange</li>
    <li>yellow</li>
</ol>

#animals {
    list-value-type: disc;
}

#favourite-colours {
    list-value-type: lower-roman;
}
```

# Styling Links

We can use the :visited pseudoclass with the anchor element to syle visited links differently to ones which have not been visited.

We can give links specific effects when the cursor hovers over them using the :hover pseudoclass.

It is possible to change the default pointer which the cursor changes to when a link is hovered over. This can be useful to let the user know something about what they can do with the link.

```css
a {
    color: blue;
    text-decoration: none;
}

a:visited {
    color: orange;
}

a:hover {
    text-decoration: underline;
    cursor: crosshair;
}
```

# The Universal Selector

The * is the universal selector in that it selects all the elements in a document. This can be used to reset default styles so each user's browser renders the content in the same way.

```css
* {
    margin: none;
    padding: none;
}
```

# Attribute Selectors

We can select elements based on the values of their attributes using the attribute selector.

We can use regular expressions to match patterns. This is common with anchor elements so we can match values which have a pattern within them somewhere, at the start or at the end.

```css
<input type="text">
<input type="number">
<input type="checkbox">

input[type="number"] {
    background-color: gold;
}
```

```css
<a href="https://cats.wiki.com">Cats</a>
<a href="https://dogs.wiki.com">Dogs</a>
<a href="https://rose.com">Roses</a>
<a href="https://tulip.com">Tulips</a>
<a href="#animals">Animals</a>
<a href="#plants">Plants</a>

a[href*="wiki"] {
    color: red;
}

a[href^="#"] {
    color: orange;
}

a[href$=".com"] {
    color: blue;
}
```

# Grouping Selectors

We can group selectors together using ,

We can group different types of selectors such as different heading elements or different classes.

We can combine different selectors so we might group elements with classes with ids.

```css
h1,
h2,
h3 {
    background-color: blue;
    color: orange
}

.tags,
.names,
.comments {
    background-color: yellow;
    color: purple
}

h4,
h5,
h6,
.addresses,
.bars,
#special {
    background-color: red;
    color: green
}
```

# The Descendant Combinator

We can use a space to specify that we want to select descendants (children, grand-children and so on). These can be of elements, classes, ids etc

We might, for example, want to select spans which are descendents of a specific element which has an id set on it.

```css
<p id="diet">
    Cats eat <span>meat</span> and <span>fish</span> mostly.
</p>

#diet span {
    font-weight: bold
}
```

# Child Combinator

This is like the descendant combinator but it only selects direct children not grand-children etc.

```css
<ul>
    <li>Name: <span>Billy Bob</span></li>
    <li>Password: <span>password123</span></li>
</ul>

li > span {
    font-weight: bold
}
```

# The Compound Selector

We can select specific elements belonging to a specific class using . notation - we could do this with ids but it makes no sense as ids are already unique.

```css
<h1 class="special">Cats</h1>
<h2 class="special">Diet</h2>
<h3 class="special">Treats</h3>
<h3 class="special">Essentials</h3>

h3.special {
    color: gold
}
```
