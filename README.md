# CSS `calc()` Issue in Flexbox

This repository demonstrates a problem encountered when using the `calc()` function within CSS flexbox layouts. Specifically, subtracting a fixed pixel value from a percentage value inside `calc()` does not behave as intuitively expected.

## Bug Description

The `calc()` function, when used to subtract pixels from percentages within a flexbox item, does not always accurately reflect the intended layout. This is particularly noticeable when the flex container has a defined size.

## Steps to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe the unexpected spacing or layout of the elements within the flex container. The right margin will not be 10px less than the width of the container as expected.

## Solution

Refer to `bugSolution.css` to understand the fix.  Using `width: calc(100% - 10px);` within a flexbox item often requires additional strategies such as explicitly setting a `max-width` if you intend to control the maximum extent of the item. 