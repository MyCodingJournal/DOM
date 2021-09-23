# DOM
<a href="https://github.com/MyCodingJournal/phase-0-the-dom-is-a-tree">Link to lab</a>

Select an Element With JavaScript<br>
- document.querySelector(selector)
- document.querySelector('h1');
 
Delete an Element with JavaScript<br>
- document.querySelector('h1').remove();

note:The selector is like a query string that lets us find things within an HTML page.

Ask the DOM to Find or "select" an HTML Element or Elements in the Rendered Page<br>

##### Finding a Node<br>
JavaScript exposes a few ways of finding DOM nodes, either directly or in stages, courtesy of the document object. We will introduce three here, in order from most to least specific: getElementByID(), getElementsByClassName(), and getElementsByTagName().

##### document.getElementById()<br>
This method provides the quickest access to a node, but it requires that we know a very specific piece of information — its id. 

This method can only return one element, since CSS ids are expected to be unique.<br>
- Syntax:
    - document.getElementById('theIdOfTheElement')

##### document.getElementsByClassName()<br>
This one is also very commonly used in DOM programming.

This method finds elements by their className. Unlike the previous method, class names do not need to be unique, so this method returns an HTMLCollection of all the elements with the given class. An HTMLCollection is an array-like structure containing a list of elements. You can iterate over an HTMLCollection with a simple for loop.

- Syntax:
    - document.getElementsByClassName('yourClassNameHere')

##### document.getElementsByTagName()<br>
You can use this method if you don't know an element's id or class, but you do know its tag name (the tag name is the thing between the <>, e.g., 'div', 'h1', header, article etc.). Since tag names aren't unique, this method also returns an HTMLCollection.

##### Conclusion<br>
Understanding the tree structure of the DOM helps us navigate all kinds of trees. In subtrees and branches we can find the nodes we need by IDs, class names or tag names, or by using element attributes like children. Once we've selected our elements, we can use JavaScript to manipulate them. By using these techniques, we can start to build a richer user experience.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# DOM query selector methods
<a href="https://github.com/VGDJP-07/phase-0-the-dom-query-selector-methods">Link to lesson</a>

we can improve our search when we use document structure (tag, id, class) along with the tree structure of the DOM. It turns out CSS is a great language for expressing those relationships! With the querySelector() and querySelectorAll() methods, we provide one or more CSS selectors as an argument and we get back the matching element or elements. Because they can take a string containing multiple selectors, they allow us to create very specific, complex queries.

##### querySelector()<br>
The querySelector() method takes one argument, a string of one or more <a href="https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors">CSS-compatible selectors</a>, and returns the first element that matches.

##### querySelectorAll()<br>
querySelectorAll() method works a lot like querySelector()
— it accepts a string containing one or more selectors as its argument, and it searches starting from the object that it's called on (either document or an element). However, instead of returning the first match, it returns a "NodeList collection" of all matching elements. A NodeList is similar to an HTMLCollection: it is an array-like structure containing, in this case, a list of DOM nodes.

##### Conclusion<br>
The DOM selection methods document.querySelector() and document.querySelectorAll() are powerful tools for finding the elements we need to update and change. They use the familiar CSS selector syntax and allow us to create very specific queries that give us access to elements in complex DOM trees.

##### Resources<br>
- <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector">document.querySelector()</a>
- <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll">document.querySelectorAll()</a>
