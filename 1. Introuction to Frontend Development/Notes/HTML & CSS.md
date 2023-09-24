## Important Topics Covered
1. Selectors - Element, ID, Class, Descendant, Children
2. HTML Tags Examples
3. Document Flow - Display & Inline
4. DOM
5. Box Model
# HTML & CSS

### Getting started with HTML
HTML provides structure to a webpage. It contains tags and elements.

##### Elements and Tags
Elements start with an opening tag < then p then >, and end with a closing tag < then / p and then >. 
Tags can also be self closing like < br > or < br / >. 
##### IMP. 
Tags make up elements which in turns provide structure to the webpage.

##### Creating an HTML Document

```
<!DOCTYPE html>
```

This actually tells a browser that this document will be an HTML document

```
<html> 
```

This is the html root element.

```
<head> </head>
```

Nothing inside the head tag is displayed in the browser. You enter information about the document or enter metadata. Meta tags for instance can describe information about the webpage, keywords for search engines, etc.

```
<body> </body>
```

Contents of the webpage goes inside the body.

##### Some Basic HTML Tags
1. h1, h2, h3, h4, h5, h6
2. p
3. br
4. span
5. strong
6. b
7. em
8. i
9. div
10. a

##### Anchor Tag
Anchor Tag is used to create hyperlinks to link other pages.

```
<a href="location.html">Our Location</a>
```
##### Image Tag

```
<img src="cat.png" width="240" height="160" alt="A small cat">
```

##### Table Tag
Table tag allows you to organize data in rows and column.

```
<table>
	<tr>
		<th>Dish</th>
		<th>Price</th>
	</tr>
	<tr>
		<td>Falafel</td>
		<td>$10.00</td>
	</tr>
	<tr>
		<td>Pasta Salad</td>
		<td>$12.00</td>
	</tr>
</table>
```

##### Form Tag
Forms when submitted sends a HTTP request to the server. 

Form tags have action attribute which specifies the path or the url the form shiuld submit the request to. If the path is not specified, it submits the request to the same path as the current webpage. 

By using Form method, you can specify the HTTP method(either GET or POST) when submitting the form.

```
<form action="/registration" method="GET">
	<label for="username">Username</label><br>
	<input type="text" name="username">

	<label for="password">Password</label><br>
	<input type="password">
	<input type="submit">
</form>
```

##### Checkboxes

```
<input type="checkbox" name="dog" value="dog">
<label for="dog">I own a dog</label><br>

<input type="checkbox" name="cat" value="cat">
<label for="cat">I own a cat</label><br>
```

##### Radio Buttons

```
<input type="radio" name="right" value="right">
<label for="right">I am right-handed</label><br>

<input type="radio" name="left" value="left">
<label for="left">I am left-handed</label><br>
```

##### Textarea

```
<textareaname="multiline" rows="5"></textarea>
```

##### Drop-down List

```
<select name="food">
	<option value="chocolate">Chocolate</option>
	<option value="strawberry">Strawberry</option>	
</select>
```

##### Introduction to DOM
Document Object Model. It is basically Tree structure of the objects. To represent the HTML Elements in JavaScript, the browser builds DOM.

![Introduction to DOM](https://raw.githubusercontent.com/HibbanHaroon/meta-frontend-development-course/main/1.%20Introuction%20to%20Frontend%20Development/Notes/Screenshots/Pasted%20image%2020230908051241.png)

All the HTML elements are represented as objects in the Document Object Model. You can modify the HTML elements by accessing the objects in DOM.

### CSS Basics
CSS is basically for decoration of the webpage and it tells the browser how to style the HTML elements.
##### Selector and Styling:
Below is a CSS rule:
```
p {
	color: blue;
}
```

p - Selector
color: blue; - Declaration
##### Inside the Declaration:
color - Property
blue - Value
##### How to link css file:
```
<link rel="stylesheet" href="style.css"/>
```

##### Different Types of Selectors:
##### 1. Element Selector
```
p {
	color: blue;
}
```
##### 2. ID Selector
```
#first-id {
	color: blue;
}
```
##### 3. Class Selector
```
.first-class {
	color: blue;
}
```
##### 4. Descendant Selector
```
#first-id h1 {
  color: blue;
}
```

There maybe multi level children inside the element with id first-id such as a div > h1 or direct child h1. It applies to all the direct or indirect descendants.
##### 5. Child Selector
```
#blog > h1 {
  color: blue;
}
```

This applies to the immediate children or the children at the single depth level.
##### 6. :hover Pseudo-Class
pseudo-class allows to select elements based on their state.

```
a:hover {
  color: orange;
}
```

##### Box Model
Every element is displayed in a box on the browser. The css rules tells the browser how to display them. Margin, Border, Padding helps in showing the elements in a structured, organized and visually pleasing manner on the browser.

##### Document Flow - Block && Inline Elements
Block Elements occupy the width of the page and appear on a new line. Some examples are div, form and heading elements.
Inline Elements occupy the width of the content and be on the same line. Many inline elements can appear on the same line. Some examples are input, label, span, i, img, a, span, em.

The layout can be changed by styling the display property. 

##### Alignment
Text can be aligned by using text-align property.
##### Horizontally centering a div or element:
The div and element needs to be a block element. margin auto is then used to center the element horizontally.

```
<div class="parent">
  <div class="child">
  </div>
</div>
```

```
.parent {
  border: 4px solid red;
}

.child {
  width: 50%;
  padding: 20px;
  border: 4px solid green;
  margin: auto;
}
```

##### Using Float to align right and left:
```
.child {
  float: right;
}
```

