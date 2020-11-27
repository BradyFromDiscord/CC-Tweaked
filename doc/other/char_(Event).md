This event is fired when a alphanumeric key is pressed on the keyboard.

## Return values
1. [`string`]: The event name.
2. [`string`]: The string representing the character that was pressed.

## Other notes
- This event won't fire because of Tab, Shift, the up arrow, etc. Use the [`key`] event if you wish to trap those keys.

## Example
Prints each character the user presses:
```lua
while true do
  local event, character = os.pullEvent("char")
  print(character.." was pressed.")
end
```

[`string`]: string
[`key`]: key