An event is any occurence that can be detected by any Computer, Turtle, or Pocket Computer, 
such as a key being pressed, a redstone input changing, a disk being inserted into a disk drive, etc. 
A list of all event types can be found below. 
To listen for any events (or a specific event), use [`os.pullEvent()`].

Every event type returns values based on the result of the event 
(i.e. the event type [`char`] will return the value of the letter that was typed).
Click on the name of an event type to get a more detailed description, as well as the return values of that event type. (Note: some event types don't have pages yet, so their links won't work.)
## Event types
| Name                  | Description                                                                     |
| --------------------- | ------------------------------------------------------------------------------- |
| [`char`]              | Fired when text is typed on the keyboard.                                       |
| [`key`]               | Fired when a key is pressed on the keyboard.                                    |
| [`key_up`]            | Fired when a key is released.                                                   |
| [`mouse_click`]       | Fired when a mouse button is pressed.                                           |
| [`mouse_drag`]        | Fired when the mouse is moved after clicking.                                   |
| [`mouse_scroll`]      | Fired when a mousewheel is scrolled.                                            |
| [`mouse_up`]          | Fired when a mouse button is released.                                          |
| [`paste`]             | Fired when Ctrl + V is pressed on the keyboard.                                 |
| [`redstone`]          | Fired when the state of any of the redstone inputs change.                      |
| [`disk`]              | Fired when a disk is inserted into an adjacent disk drive.                      |
| [`disk_eject`]        | Fired when a disk is removed from an adjacent disk drive.                       |
| [`peripheral`]        | Fired when peripheral is attached.                                              |
| [`peripheral_detach`] | Fired when peripheral is removed.                                               |
| [`timer`]             | Fired when a timeout started by os.startTimer() completes.                      |
| [`alarm`]             | Fired when a time passed to os.setAlarm() is reached.                           |
| [`rednet_message`]    | Fired when a rednet message is received from the rednet API.                    |
| [`modem_message`]     | Fired when a modem message is received from the modem.                          |
| [`turtle_inventory`]  | Fired when the inventory on a Turtle is changed.                                |
| [`monitor_resize`]    | Fired when a connected monitor resizes.                                         |
| [`monitor_touch`]     | Fired when a player right clicks on a connected advanced monitor.               |
| [`term_resize`]       | Fired when the terminal resizes.                                                |
| [`terminate`]         | (Read full description)                                                         |
| [`http_success`]      | Fired when [`http.request()`] is successful.                                    |
| [`http_failure`]      | Fired when [`http.request()`] is unsuccessful.                                  |
| [`http_check`]        | Fired when [`http.getURLAsync()`] is successful.                                |
| [`websocket_success`] | Fired when a websocket is opened with [`http.websocketAsync()`].                |
| [`websocket_failure`] | Fired when a websocket requested with [`http.websocketAsync()`] cannot connect. |
| [`websocket_message`] | Fired when a websocket message is received.                                     |
| [`websocket_closed`]  | Fired when a websocket connection is closed.                                    |
| [`computer_command`]  | Triggered when the /computer command is used.                                   |
| [`task_complete`]     | Fired when an asynchronous task completes.                                      |

[`os.pullEvent()`]: https://tweaked.cc/module/os.html#v:pullEvent
[`http.request()`]: https://tweaked.cc/module/http.html#v:request
[`http.getURLAsync()`]: https://tweaked.cc/module/http.html#v:checkURLAsync
[`http.websocketAsync()`]: https://tweaked.cc/module/http.html#v:websocketAsync
[`char`]: "char_(Event)"
[`key`]: "key_(Event)"
[`key_up`]: "key_up_(Event)"
[`mouse_click`]: "mouse_click_(Event)"
[`mouse_drag`]: "mouse_drag_(Event)"
[`mouse_scroll`]: "mouse_scroll_(Event)"
[`paste`]: #
[`mouse_up`]: "mouse_up_(Event)"
[`redstone`]: #
[`disk`]: #
[`disk_eject`]: #
[`peripheral`]: #
[`peripheral_detach`]: #
[`timer`]: #
[`alarm`]: #
[`rednet_message`]: #
[`modem_message`]: #
[`turtle_inventory`]: #
[`monitor_resize`]: #
[`monitor_touch`]: #
[`term_resize`]: #
[`terminate`]: #
[`http_success`]: #
[`http_failure`]: #
[`http_check`]: #
[`websocket_success`]: #
[`websocket_failure`]: #
[`websocket_message`]: #
[`websocket_closed`]: #
[`computer_command`]: #
[`task_complete`]: #