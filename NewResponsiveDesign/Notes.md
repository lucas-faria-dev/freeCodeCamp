### Learn More About CSS Pseudo Selectors by Building A Balance Sheet - Step 30

Before you get too far into your styling, you should make use of the sr-only class. You can use CSS to make elements with this class completely hidden from the visual page, but still be announced by screen readers.

The CSS you are about to write is a common set of properties used to ensure elements are completely hidden visually.

The span[class~="sr-only"] selector will select any span element whose class includes sr-only. Create that selector, and give it a border property set to 0.



### Learn More About CSS Pseudo Selectors by Building A Balance Sheet - Step 44
Style the text within your #years element by creating a #years span[class] selector. The span[class] syntax will target any span element that has a class attribute set, regardless of the attribute's value.

Give your new selector a bold font, a width of 4.5rem, and text aligned to the right.

#years span[class] {
  font-weight: bold;
  width: 4.5rem;
  text-align: right;
}


### Learn More About CSS Pseudo Selectors by Building A Balance Sheet - Step 46
Before you start diving in to the table itself, your span elements are currently bolded. Create a span:not(.sr-only) selector and give it a font-weight property set to normal.

The :not() pseudo-selector is used to target all elements that do not match the selector - in this case, any of your span elements that do not have the sr-only class. This ensures that your earlier rules for the span[class~="sr-only"] selector are not overwritten.

span:not(.sr-only){
  font-weight: normal;
}

### Learn More About CSS Pseudo Selectors by Building A Balance Sheet - Step 53
#### Understand this 
tbody td {
  width: 100vw;
  min-width: 4rem;
  max-width: 4rem;
}

### Learn More About CSS Pseudo Selectors by Building A Balance Sheet - Step 55
The [attribute="value"] selector targets any element that has an attribute with a specific value. Create a tr[class="total"] selector to target specifically your tr elements with the total class. Give it a bottom border of 4px double #0a0a23 and make the font bold.

### Learn More About CSS Pseudo Selectors by Building A Balance Sheet - Step 57
The key difference between tr[class="total"] and tr.total is that the first will select tr elements where the only class is total. The second will select tr elements where the class includes total.

In your case, tr.total will work. You can use this selector to target all td elements within your .total rows. Align the text to the right, and give them a padding of 0 0.25rem.

### Learn Responsive Web Design by Building a Piano - Step 10
The **::before** selector creates a pseudo-element which is the first child of the selected element, while the **::after** selector creates a pseudo-element which is the last child of the selected element. These pseudo-elements are often used to create cosmetic content, which you will see later in this project.
Keep in mind that the content property is required for ::before and ::after to work, even if it is set to an empty string. These pseudo-elements are commonly used in combination with the content property to add decorative elements or generate additional visual content dynamically.

### Learn Responsive Web Design by Building a Piano - Step 31
You might have noticed the keys collapse when the browser window is smaller than 768px. Set overflow to hidden in the first .keys selector, to take care of this issue. This property will hide any element that is pushed outside the set width value of .keys.
.keys {
  background-color: #040404;
  width: 949px;
  height: 180px;
  padding-left: 2px;
  overflow: hidden;
}

The position property in CSS is used to control the positioning of an element in a document. It's one of the fundamental properties for layout control. The position property can take several values, and each value determines how the element is positioned within its containing element or the entire document.

Here are the main values for the position property:

Static (Default):

Elements are positioned according to the normal flow of the document.
The top, right, bottom, and left properties have no effect.
This is the default value.
css
Copy code
.example {
  position: static;
}
Relative:

Elements are positioned relative to their normal position in the document flow.
The top, right, bottom, and left properties can be used to offset the element from its normal position.
css
Copy code
.example {
  position: relative;
  top: 10px;
  left: 20px;
}
Absolute:

The element is removed from the normal document flow, and its position is calculated relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).
If there is no positioned ancestor, it's positioned relative to the initial containing block (usually the <html> element).
css
Copy code
.example {
  position: absolute;
  top: 50px;
  left: 100px;
}
Fixed:

The element is removed from the normal document flow, and its position is calculated relative to the viewport (browser window).
It remains fixed in its position even when the page is scrolled.
css
Copy code
.example {
  position: fixed;
  top: 0;
  left: 0;
}
Sticky:

The element is treated as relative positioned until it crosses a specified point, then it is treated as fixed positioned.
The specified point is determined by the values of top, right, bottom, and left.
css
Copy code
.example {
  position: sticky;
  top: 50px;
}
Using the position property allows you to create complex layouts and control the placement of elements on the page. Understanding how each value works and when to use them is crucial for effective web design.

### Learn CSS Variables by Building a City Skyline - Step 113
At the top of the sky gradient color list, where you would put a direction for the gradient; add circle closest-corner at 15% 15%,. This will move the start of the gradient to 15% from the top and left. It will make it end at the closest-corner and it will maintain a circle shape. These are some keywords built into gradients to describe how it behaves.