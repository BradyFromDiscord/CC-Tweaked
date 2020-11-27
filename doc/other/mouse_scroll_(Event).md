This event is fired when a mousewheel is scrolled in the terminal.

## Return values
1. [`string`]: The event name.
2. [`number`]: The direction of the scroll. (-1 = up, 1 = down)
3. [`number`]: The X-coordinate of the scroll (in screen-characters).
4. [`number`]: The Y-coordinate of the scroll (in screen-characters).

## Other notes
- This event is only available on Advanced systems, as only Advanced systems have mouse support.

## Example
Prints the direction and the coordinates of every mouse scroll:
```lua
while true do
  local event, scrollDirection, x, y = os.pullEvent("mouse_scroll")
  print("mouse_scroll: " .. tostring(scrollDirection) .. ", " ..
    "X: " .. tostring(x) .. ", " ..
    "Y: " .. tostring(y))
end
```

[`string`]: string
[`number`]: number