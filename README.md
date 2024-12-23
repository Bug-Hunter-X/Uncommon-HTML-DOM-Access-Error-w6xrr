# Uncommon HTML DOM Access Error

This repository demonstrates a subtle error related to accessing elements in the HTML Document Object Model (DOM) before they are fully loaded. The issue arises when JavaScript code attempts to manipulate an element that hasn't yet been parsed and added to the DOM by the browser. This frequently leads to unexpected behavior or runtime errors. 

**Problem:** The `bug.html` file demonstrates the issue.  We're trying to manipulate the `div` element *before* the browser has fully constructed the DOM. This results in the first attempt to add text to the div failing, while the corrected method using `DOMContentLoaded` works as expected. 

**Solution:** The solution involves attaching a DOMContentLoaded event listener which ensures the code executes only after the entire DOM has been loaded.