This event is fired when the terminal is clicked with a mouse.

## Return values
1. [`string`]: The event name.
2. [`number`]: The mouse button that was clicked. Left Mouse Button is returned as the number 1, Right Mouse Button is returned as the number 2 and Middle Mouse Button is returned as the number 3. If you have more than three buttons on your mouse, pressing them will return 1.
3. [`number`]: The X-coordinate of the click (in screen-characters).
4. [`number`]: The Y-coordinate of the click (in screen-characters).

## Other notes
- This event is only available on Advanced systems, as only Advanced systems have mouse support.

## Example
Print the button and the coordinates of every mouse click:
```lua
while true do
  local event, button, x, y = os.pullEvent( "mouse_click" )
  print( "The mouse button ", button, " was pressed at ", x, " and ", y )
end
```

[`string`]: string
[`number`]: number