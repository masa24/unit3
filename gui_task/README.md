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
        pos_hint: {"x":.8, "y":-0.1}

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
