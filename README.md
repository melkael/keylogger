# Keylogger

A minimal keylogger for linux written in python, it has no dependency aside from standard lib.
I'll add support for reading the keystrokes over the network as well as some sort of obfuscation mechanism soon.
I'd love to implement a keymap detection too, currently it's only a hardcoded qwerty

## How it works

It simply reads from your /dev/input/event* and then formats the stream in a human readable way (currently only supports qwerty).
If you wonder which event* is chosen, it looks at /proc/bus/input/devices to know which of the event* files is the one for the keyboard. I'm not using pyxhook as it might not always be available depending on what you do.

## Disclaimer
I wrote this program for learning purposes only. Only use it on your own machines to capture your own keystrokes. 
I can't be held responsible for your illegal activities
