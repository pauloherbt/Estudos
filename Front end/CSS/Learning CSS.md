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
