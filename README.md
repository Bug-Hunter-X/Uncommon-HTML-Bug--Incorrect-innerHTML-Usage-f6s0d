# Uncommon HTML Bug: Incorrect innerHTML Usage

This repository demonstrates a subtle bug related to using `innerHTML` in JavaScript before the target element has been fully parsed by the browser.  The code attempts to modify the `innerHTML` of an element ('myDiv2') that does not yet exist in the DOM at the point the script executes.  This leads to a silent failure—no error is thrown, and the intended text does not appear.

The solution involves ensuring that the script executes *after* the element it targets is available in the DOM, typically by placing the script at the end of the `<body>` or by using DOMContentLoaded event listener.