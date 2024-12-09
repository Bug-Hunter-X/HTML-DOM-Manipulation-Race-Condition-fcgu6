# HTML DOM Manipulation Race Condition

This repository demonstrates a race condition bug in HTML where JavaScript code attempts to manipulate a DOM element before the browser has finished rendering it. This can lead to unexpected behavior, such as the element not being found or unexpected styling issues.

## Bug Description

The bug occurs because the JavaScript code attempts to access and modify the `myDiv` element's style before the browser has completed rendering the HTML.  This results in the JavaScript code failing to find the element and throwing an error or failing to correctly modify it.

## Solution

The solution involves ensuring that the JavaScript code executes *after* the DOM is fully loaded. This can be achieved using the `DOMContentLoaded` event listener.