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

### Learn Intermediate CSS by Building a Cat Painting - Step 8
To see the cat-head element, give it a linear gradient background with #5e5e5e at 85% and #45454f at 100%.

You might not notice the difference between these two colors, but they are there.

Read and understand this:
https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient

### Learn Intermediate CSS by Building a Cat Painting - Step 9
CSS positioning lets you set how you want an element to be positioned in the browser. It has a position property you can set to static, absolute, relative, sticky or fixed.

Once you set the position property of the element, you can move the element around by setting a pixel or a percentage value for one or more of the top, right, left, or bottom properties.

static is the default positioning for all elements. If you assign it to an element, you won't be able to move it around with top, right, left, or bottom.

Give .cat-head a position property of static, then set the top and left properties to 100px each.

### Learn Intermediate CSS by Building a Cat Painting - Step 16
You should now center the cat head.

Give the .cat-head element a position property set to absolute. Set a value of 0 for the right, left, top, bottom properties, then set its margin property on all sides to auto. That's one way to center an element vertically and horizontally using CSS positioning.

  right: 0;
  left: 0;
  top: 0;
  bottom: 0;
  margin: auto;
  background: linear-gradient(#5e5e5e 85%, #45454f 100%);
  width: 205px;
  height: 180px;
  border: 1px solid #000;
  border-radius: 46%;

### Learn Intermediate CSS by Building a Cat Painting - Step 26
To position the left ear properly, you can use CSS transform to rotate it in a certain degree.

The transform property allows you to modify the shape, position, and size of an element without changing the layout or affecting the surrounding elements. It has functions such as translate(), rotate(), scale(), skew(), and matrix().

Set the transform property to rotate(-45deg) and see what happens.


### Learn Intermediate CSS by Building a Cat Painting - Step 59 | Vocabulary
Using a descendant selector, select the two div elements inside the div with class cat-mouth. Give it a width of 30px, a height of 50px, and a border of 2px solid #000.
https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_combinator

git 