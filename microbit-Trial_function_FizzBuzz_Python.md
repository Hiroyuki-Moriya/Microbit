microbit-Trial_function_FizzBuzz_Python.md    

# microbit-Trial_function_FizzBuzz    

## 関数を使うプログラムの例    

  ボタンAを押したとき  
    ボタンAを押した数を数え、変数countにセットします。  

  ボタンBを押したとき  
    関数Fizzbuzzにcountをセットして、関数を呼び出します。  
    関数Fizzbuzz結果を受け取って表示します。  

  関数FizzBuzz  
    数値を変数numに受け取ります。  
      numが3で割り切れる時は、結果を”Fizz”にします。  
      numが5で割り切れる時は、結果を”Buzz”にします。  
      numが3でも5でも割り切れる時は、結果を”FizzBuzz”にします。  
      numが3でも5でも割り切れない時は、結果を受け取ったnumにします。  
    結果を返します。  


## Example of a program that uses a function  

  When button A is pressed  
    Count the number of button A pressed and set it to the variable count.  

  When button B is pressed  
     Call the function by setting count in the function Fizzbuzz.  
     Function Fizzbuzz Receives and displays the results.  

  Function FizzBuzz  
        Receives a number in the variable num.  
          If num is divisible by 3, the result will be "Fizz".  
          If num is divisible by 5, the result will be "Buzz".  
          If num is divisible by either 3 or 5, the result will be "FizzBuzz".  
          If num is not divisible by 3 or 5, the result is set to the received num.  
        Returns the result.  

## Source code
`
"""
    Title  : Trial_function_FizzBuzz
    Version: 01
    Author : Hiroyuki.Moriya
    Use    : https://makecode.microbit.org/#editor
"""
count = 0

def on_button_pressed_a():
    global count
    count += 1
input.on_button_pressed(Button.A, on_button_pressed_a)

def on_button_pressed_b():
    global count
    Result = ""
    Result = FizzBuzz(count)
    basic.show_string(Result)
    count = 0
input.on_button_pressed(Button.B, on_button_pressed_b)

def FizzBuzz(num: number):
    txt = str(num) + str(" ")
    if num % 15 == 0:
        txt = "FizzBuzz"
    else:
        if num % 3 == 0:
            txt = "Fizz"
        if num % 5 == 0:
            txt = "Buzz"
    return txt
`
