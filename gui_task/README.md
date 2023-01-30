# Task 1

## main file
```.py
from kivymd.app import MDApp


class task1(MDApp):
    def build(self):
        return
    def convert(self,val,unit):
        value = self.root.ids.currency.text
        if not value.isdigit():
            self.root.ids.currency.error = True
        else:
            self.root.ids.output.text = str(f'{round(int(value) * val)} {unit}')

    def close(self):
        exit()


task = task1()
task.run()
```

## KV file
```.py
Screen:
    size: 500,300
    MDLabel:
        id: click
        text: 'Click to convert'
        halign:'center'
        pos_hint: {'center_y':.2}
    MDLabel:
        id: title
        text: 'Currency Converter'
        halign:'center'
        pos_hint: {'center_y':.9}
    MDLabel:
        id: output
        text: ''
        font_size:'35pt'
        pos_hint: {"x":.7, "y":-0.1}

    MDTextField:
        id: currency
        hint_text: 'Enter an amount in EUR'
        helper_text: 'Please input an integer'
        helper_text_mode: 'on_error'
        pos_hint: {"x":.1, "y":.5}
        size_hint_x: .8
    MDRaisedButton:
        text: 'USD'
        pos_hint: {"x":.7, "y":.2}
        size_hint: .1, .1
        on_release:
            app.convert(1.09,'USD')
    MDRaisedButton:
        background_color:1,0,0,0
        text: 'JPY'
        pos_hint: {"x":.8, "y":.2}
        size_hint: .1, .1
        on_release:
            app.convert(141.22,'JPY')
            
```
## image
![JPY](jpy.png)
![USD](usd.png)
![error](error.png)

# Task2
## main file
```.py
from kivymd.app import MDApp
import math


class task2(MDApp):
    def build(self):
        return
    def convert(self):
        multiple = ['','Kilo','Mega','Giga','Tera','Peta','Exa']
        value = self.root.ids.bits.text
        if not value.isdigit():
            self.root.ids.bits.error = True
        else:
            byte = int(value)/8
            bytes = round(math.log(byte,1024))
            if bytes > 6:
                bytes = 6
            self.root.ids.output.text = str(f'{str(round(byte/(1024**bytes),2))} {multiple[round(bytes)]} bytes')

    def close(self):
        exit()


task = task2()
task.run()
```
## KV file
```.py
Screen:
    size: 500,300
    MDLabel:
        color:0,90,0
        font_size:'40pt'
        id: title
        text: 'Bits Bytes converter'
        halign:'center'
        pos_hint: {'center_y':.9}
    MDLabel:
        id: output
        text: ''
        font_size:'35pt'
        halign:'center'
        pos_hint: {"y":-0.3}

    MDTextField:
        id: bits
        hint_text: 'Enter the bits'
        helper_text: 'Please input an integer'
        helper_text_mode: 'on_error'
        pos_hint: {"x":.1, "y":.6}
        size_hint_x: .8
    MDRaisedButton:
        text: 'Convert to bytes'
        pos_hint: {"x":.1, "y":.35}
        font_size:'20pt'
        size_hint: .8, .2
        on_release:
            app.convert()

```
## image
![JPY](jpy.png)
![USD](usd.png)
![error](error.png)
