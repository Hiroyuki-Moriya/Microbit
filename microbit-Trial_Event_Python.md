microbit-Trial_Event_Python.md    

# microbit-Trial_Event_Python    

## イベントで動作するプログラムの例    

## Example of a program that runs on an event  

## Source code
```
"""
    Title  : Trial_Event_Python
    Version: 01
    Author : Hiroyuki.Moriya
    Use    : https://makecode.microbit.org/#editor
"""
def on_logo_touched():
    basic.show_string("Logo")
input.on_logo_event(TouchButtonEvent.TOUCHED, on_logo_touched)

def on_button_pressed_a():
    basic.show_string("A")
input.on_button_pressed(Button.A, on_button_pressed_a)

def on_gesture_shake():
    basic.show_string("Shake")
input.on_gesture(Gesture.SHAKE, on_gesture_shake)

def on_button_pressed_ab():
    basic.show_string("A+B")
input.on_button_pressed(Button.AB, on_button_pressed_ab)

def on_button_pressed_b():
    basic.show_string("B")
input.on_button_pressed(Button.B, on_button_pressed_b)
```
