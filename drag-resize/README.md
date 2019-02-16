# Drag and Resize
The idea in this test is to explore a way to make a highly responsive element drang and resize. The goal is to simulate a visual HTML editor where users can drag and resize a `<div>` like they resize a square shape in PowerPoint.

## Roadmap

### First iteration
- If you click a button, a new square will be added
  - The square will be selected
- A selected state will present 8 handlers, one on each corner of the shape, and one on each side of the shape.
  - Each corner handler will allow it to resize the shape in two directions
  - Each side handler will allow only one direction resize (e.g.: Left side handler will allow you to resize only the width of the box)
- Clicking inside the element and drag, will move the element
- Clicking outside the element will deselect
- Clicking in a different element will switch the selection to the clicked element
    - Will immediately allow it to be moved should user don't release mouse button and starts move it around

### Second iteration
- Create a boundary box to be the Design Surface
- Handle elements being resized and moved to stop at last known spot should the cursor moves outside the browser window (thus, not capturing the mouse-up event)
- Handle erratic mouse movements (grabbing and resizing it violently)
    - Cursor and handler should always stay in sync
- Add a floating label next to it to inform user of the dimensions (in pixels)