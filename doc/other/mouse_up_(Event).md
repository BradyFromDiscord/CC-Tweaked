This event is fired when a mouse button (which was pressed while being inside the computer's terminal) is released. 

## Return values
1. [`string`]: The event name.
2. [`number`]: The mouse button that was released. Left Mouse Button is returned as the number 1, Right Mouse Button is returned as the number 2 and Middle Mouse Button is returned as the number 3. If you have more than three buttons on your mouse, pressing them will return 1.
3. [`number`]: The X-coordinate of the release (in screen-characters).
4. [`number`]: The Y-coordinate of the release (in screen-characters).

## Other notes
- This event is only available on Advanced systems, as only Advanced systems have mouse support.
- If the mouse button is released outside of the computer's display, the event is fired as soon as the mouse hovers over the display again

## Example
Prints the coordinates and button number on every mouse button release:
```lua
while true do
  local event, button, x, y = os.pullEvent( "mouse_up" )
  print( "The mouse button ", button, " was released at ", x, " and ", y )
end
```

[`string`]: string
[`number`]: number