# Keylogger
A self contained linux keylogger written in python
A minimal keylogger for linux written in python, it has no dependency aside from standard lib.
I'll add support for reading the keystrokes over the network as well as some sort of obfuscation mechanism soon.
I'd love to implement a keymap detection too

## How it works

It simply reads from your /dev/input/event* and then formats the stream in a human readable way (currently only supports qwerty).
If you wonder which event* is chosen, it looks at /proc/bus/input/devices to know which is the right one for keyboard

## Disclaimer
I wrote this program for learning purposes only. Only use it on your own machines to capture your own keystrokes. 
I can't be held responsible for your illegal activities
