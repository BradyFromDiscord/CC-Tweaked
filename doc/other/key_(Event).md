This event is fired when any key (except Escape) is pressed while the terminal is focused. You can compare the values it gives you to the constants in the [`keys`] API (eg, keys.up, keys.down, etc).

If the button pressed represented a printable character, then the `key` event will be followed immediately by a [`char`] event - you're generally better off pulling that if you're wanting text input (as `key` events don't indicate eg the case of what was typed, whereas [`char`] events do). When the button is released, a [`key_up`] event may be fired as well (assuming ComputerCraft 1.74 or later).

## Return values
1. [`string`]: The event name.
2. [`number`]: The numerical key value of the key pressed.
3. [`boolean`]: A boolean indicating whether the key event was generated while holding the key (`true`), rather than pressing it the first time (`false`).

## Other notes
- Different versions of ComputerCraft give different results for return value 2; if you want the same program to work on any version, use [`keys.getName()`].

## Example
Prints each key when the user presses it, and if the key is being held:
```lua
while true do
  local event, key, isHeld = os.pullEvent("key")
  
  write( keys.getName( key ) )
  print( isHeld and " is being held." or " was pressed." )
end
```

[`string`]: string
[`number`]: number
[`boolean`]: boolean
[`char`]: char
[`key_up`]: key_up
[`keys`]: https://tweaked.cc/module/keys.html
[`keys.getName()`]: https://tweaked.cc/module/keys.html