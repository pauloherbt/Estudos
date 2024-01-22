# Learning CSS building a Cafe Menu
by: FreeCodeCamp
## Style tag
Allows the css code to style the html page, 
specify the element and assign a value to some property.
```CSS
element{
	property: value;
}
```
## Selectors list
When you have elements with the same styling, you can group them in a list
```css
selector1, selector2 {
  property: value;
}
```
## Property Glossary
<details>
	<summary>See</summary>
		1. width<br>
		2. background-color<br>
		3. margin-left<br>
		4. margin-right<br>
		5. background-image<br>
		6. text-align<br>
		7. padding-left<br>
		8. padding-right
		9. margin
</details>  

## Similarity between Mobile and desktops
It's need a meta element with special **content** attribute 
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```
## Id selector
Using # before the element's id, it's can custom this, by referring your id.
However, it's more common to use a class selector defined by a dot followed the name:
```css
.class-name {
  styles
}
```
>make sure to add **class** attribute in the html element

You can style all the elements in the class, just specify the element
## Center horizontally
set the properties margin-left and margin-right, **auto** value.
## Space between the content and the sides
Using the padding - left or right, its can change the margin, 20px.
Using -top or -botton to change the spaces between the content in the top and bottom.
> You can use just **padding**, to avoid write the four properties

## Max-width property
Useful to prevents a element grow to much and to maintain the harmony.  
## Setting the font of a component
The property ``font-family`` help us to set one font, and it can receives a _fallback_ in the case of failed to load the first font, by adding a comma followed the other font.
It's possible to set the font style, using the ``font-style`` property, with values: normal, italic, oblique.
## Separating sections
You can use **hr** element to make appears a light gray line. You can change the height, by specifying a value for the **height** property.
## Pseudo-selector
You can change properties of a link using 
```css
a:active{

}
a:hover{

}
a:visited{
}```
This way you can change de style of anchor element based on your state.
## Box sizing
This property make all the children elements don't crossing the boundaries of the father element, setting its value to **"border-box" **and you can change the paddings, margin or whatever in children element , without affect the container.
