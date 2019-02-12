# Keylogger

A minimal keylogger for linux written in python, it has no dependency aside from standard lib.
It currently supports sending the keylogs by email.

## How it works

It simply reads from your /dev/input/event* (where the keyboard events are stored in linux and then formats the stream in a human readable way (currently only supports qwerty).
If you wonder which event* is chosen, it looks at /proc/bus/input/devices to know which of the event* files is the one for the keyboard. I'm not using pyxhook as it might not always be available depending on what you do.

## Why did I write this ?

I wanted to learn a bit more about linux keyboard events and it's always cool to link things with infosec. This was stricly made for learning purposes. TBH I'm pretty scared now that I realised how easy this kind of spyware is to code

## Disclaimer
I wrote this program for learning purposes only. Only use it on your own machines to capture your own keystrokes. 
I can't be held responsible for your illegal activities

## Ideas of further improvements

It works well as it is, but I guess it would be cool to add features such as keymap detection (currently it considers anything as qwerty), screenshots and a machine learning model that would detect when a password has been typed and send an email notification

## How to run ?

You need root privileges to run this.
Simply go with :
sudo python keylogger.py [your email] [your password] [smtp server] [tls/notls] [buffer_size]

Buffer size is the number of characters saved in memory before sending an email.
