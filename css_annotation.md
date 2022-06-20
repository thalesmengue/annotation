# CSS ANOTATIONS

CSS is the acronym for Cascading Style Sheets, it is the perfect pair for HTML, can be considered a complement for HTML,
although in practice they are two different languages. Assuming that HTML is the content, CSS makes the style for the 
content, determining the aesthetic behaviour that your page will have.

The CSS inline syntax consists in the property, followed by the value, inside a ```style= "property:value"```, and if
you have multiple declarations, they are separated by a semicolon, like in the following example

```
<html>

<body>
<p style= "color: blue; font-size: 14px">
</body>

</html>
```

In other way, we have the outline syntax, that as usual is fixed in other file as a best practice, usually
named ```style.css```, where is possible to utilize the tags and IDs used in another HTML
file to style them, like the following example:

```
p{
  color: yellow;
  text-align: center;
}
```

the code above, centered the ```<p>``` elements, and fixed the yellow color to the text.

***Ok, but how can i import the style.css file to my HTML code?***

in a simpler way, you can import the ```style.css``` putting the following code inside the head tag of the HTML file
you want to import the CSS code.

```
<html>
  <head>
    <link rel="stylesheet" href="style.css">
  </head>
</html>
```

*** Sure, but how i'm going to style just a determined element of the HTML? ***

Well, reusing a past example, we can set a style to a determined element this way, by calling the tag:

```
p{
  color: yellow;
  text-align: center;
}
```
This way, all ```<p>``` elements will have text color yellow, and centered align text.

Another way, is set a name to a CSS class, like this:

```
.yellow-text{
    color: yellow;
}
```

```
<html>
    <body>
        <p class="yellow-text"> Test </p>
    </body>
</html>
```

Can be set more than one CSS class to an HTML element, but for best practices sake, separate them by a semicolon.

Or even by id name, imagine that you have an HTML element with an id ```red-center```, then you are going to start
the name of the CSS attribute with an #, and remember, never start the name with a number. This type of fixation of
attributes to an ID is unique, you can't use the same id to more than one element, if you need, then use the class
method.

```
    #red-center{
    color: red;
    text-align: center;
}
```

When a class is named ```*```, this class you apply the attributes defined in all HTML elements where get imported, also
called universal selector.


### CSS PROPERTIES

**background**

the background-color property fixes the color of the background in the element where she is used, but also has the
background-image property, where you can fix some image as the background, like the following example:

```
.background-example{
    height: 700px;
    width: 700px;
    background-color: black;
    background-image: url("img/test.jpg");
    background-size: cover;
}
```

**border**

the border name is a little intuitive, with this property you are going to build some border to elements, there are some
values you can test and see by yourself what them do, like the groove, ridge, dashed, inset, outset, hidden and the none,
you can use the values like this:

```
 .border-test{
    border: 5px groove green;
    border-radius: 15px;
 }
```

**margin**

with the margin you create space around elements, you can use the property margin like this: 
```margin: 30px, 40px, 50px, 60px;```, with this the margin start spacing around the top with 30px, then the right with
40px, the bottom with 50px, and the left with 60px, or if you want, can use like this: 
```
 .margin-test{
    margin-top: 30px;
    margin-right: 40px;
    margin-left: 50px;
    margin-bottom: 60px;
 }
```

**padding**

different from the margin, padding create space around the element content, imagine that you
have a content inside a border, if you use padding inside this border, the padding will
be applied to the content inside the border. padding can be used with the same syntax as
margin, ```padding: 30px, 40px, 50px, 60px;```, if you are going to set the same value for
all sides, you can simply set like ```padding: 50px;```, or if you want can set like this:

.padding-test{
padding-top: 30px;
padding-right: 40px;
padding-left: 50px;
padding-bottom: 60px;
}


