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

