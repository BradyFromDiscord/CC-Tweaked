This event is fired when any key except Escape is released while the terminal is focused.

## Return values
1. [`string`]: The event name.
2. [`number`]: The numerical key value of the key pressed.

## Other notes
- Different versions of ComputerCraft give different results for return value 2; if you want the same program to work on any version, use [`keys.getName()`].

## Example
Prints each key released on the keyboard whenever a "key_up" event is fired:
```lua
while true do
  local event, key = os.pullEvent("key_up")
  print( keys.getName( key ), " was released." )
end
```

[`string`]: string
[`number`]: number
[`keys.getName()`]: https://tweaked.cc/module/keys.html