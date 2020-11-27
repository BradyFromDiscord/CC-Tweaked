This event is fired every time the mouse is moved until the user releases the mouse button. It will always occur after a [`mouse_click`] event.

## Return values
1. [`string`]: The event name.
2. [`number`]: The mouse button that was clicked. Left Mouse Button is returned as the number 1, Right Mouse Button is returned as the number 2 and Middle Mouse Button is returned as the number 3. If you have more than three buttons on your mouse, pressing them will return 1.
3. [`number`]: The X-coordinate of the drag (in screen-characters).
4. [`number`]: The Y-coordinate of the drag (in screen-characters).

## Other notes
- This event is only available on Advanced systems, as only Advanced systems have mouse support.
- The event will only be fired when the mouse moves to another character position, dragging within the same character will have no effect.

## Example
Prints the new coordinates of the mouse every time a mouse_drag event occurs:
```lua
while true do
  _, button, xPos, yPos = os.pullEvent("mouse_drag")
  print("mouse_drag => " .. tostring(button) .. ": " ..
    "X: " .. tostring(xPos) .. ", " ..
    "Y: " .. tostring(yPos))
end
```

[`string`]: string
[`number`]: number
[`mouse_click`]: mouse_click