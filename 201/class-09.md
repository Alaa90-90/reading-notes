# HTML Forms
An HTML form is used to collect user input. The user input is most often sent to a server for processing.


![gsds](https://www.tutorialbrain.com/wp-content/uploads/2019/01/HTML-Form.jpg)

## The <form> Element
The HTML <form> element is used to create an HTML form for user input:

<form>
.
form elements
.
</form>

The <form> element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.

All the different form elements are covered in this chapter: HTML Form Elements.

## The <input> Element
The HTML <input> element is the most used form element.

An <input> element can be displayed in many ways, depending on the type attribute.

Here are some examples:



Type	Description
<input type="text">	Displays a single-line text input field
<input type="radio">	Displays a radio button (for selecting one of many choices)
<input type="checkbox">	Displays a checkbox (for selecting zero or more of many choices)
<input type="submit">	Displays a submit button (for submitting the form)
<input type="button">	Displays a clickable button
All the different input types are covered in this chapter: HTML Input Types.


## Text Fields
The <input type="text"> defines a single-line input field for text input.



<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>



This is how the HTML code above will be displayed in a browser:

First name:

Last name:

## Radio Buttons
The <input type="radio"> defines a radio button.

Radio buttons let a user select ONE of a limited number of choices.

<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>

This is how the HTML code above will be displayed in a browser:

Choose your favorite Web language:

 - HTML
 - CSS
 - JavaScript