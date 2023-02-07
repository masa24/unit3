# 33
## main
```.py
from test_quiz033 import mystery
import pytest

def test_empty_lists():
  assert mystery([], []) == []

def test_one_common_element():
  assert mystery([1, 2, 3], [3, 4, 5]) == [3]

def test_multiple_common_elements():
  assert mystery([1, 2, 3, 4], [3, 4, 5, 6]) == [3, 4]
```
## test code
```.py
def mystery(list1,list2):
    output = []
    for i in list1:
        for x in list2:
            if i == x:
                output.append(i)
    return (output)
```

# 34
## main
```.py
from test_quiz034 import quiz034
import pytest

def test_5():
    assert quiz034(5).romannum() == 'V'

def test_not_int():
    with pytest.raises(TypeError):
        assert quiz034("a").romannum()
def test_out_of_range():
    with pytest.raises(ValueError):
        assert quiz034(101).romannum()
def test_37():
    assert quiz034(37).romannum() == 'XXXVII'
```
## test code
```.py
class quiz034():
    def __init__(self, num):
        self.num = num

    def romannum(self):
        roma = {100: 'C', 90: 'XC', 50: 'L', 40: 'XL', 10: 'X', 9: 'IX', 5: 'V', 4: 'IV', 1: 'I'}
        result = ''
        if self.num < 1 or self.num > 100:
            raise ValueError("Number must be between 1 and 100")
        if not isinstance(self.num, int):
            raise TypeError("Number must be an integer")
        while self.num > 0:
            for i in roma.keys():
                if self.num>=i:
                    result+=roma[i]
                    self.num-=i
                    break
        return result
```



# 35


# 36


# 37


# 38
```.py
import random
import matplotlib.pyplot as plt
class coordinate:
    def __init__(self,x,y):
        self.x = x
        self.y = y

    def __repr__(self)->str:
        return f"[Coordinate Object] x:{self.x}, y:{self.y}"

class city:
    def __init__(self,name:str, location:coordinate):
        self.name = name
        self.location = location

    def __repr__(self)->str:
        return f"[City Object] City {self.name} is located at {self.location}"

    def distance(self, cityB):
        xa, ya = self.location.x, self.location.y
        xb, yb = cityB.location.x, cityB.location.y
        d = ((xa-xb)**2 + (ya-yb)**2)**(1/2)
        return d

class country:
    def __init__(self, name:str):
        self.name = name
        self.cities = []

    def add_city(self, new_city:city):
        self.cities.append(new_city)


cities_in_japan = ["Tokyo","Kagoshima","Fukuoka","Osaka","Nagoya","Sapporo","Kyoto","Hiroshima","Naha","Kobe","Karuizawa"]

point1 = coordinate(x=5,y=5)
tokyo = city(name = "Tokyo", location = point1)
kyoto = city(name = "Kyoto", location = coordinate(x=10,y=10))
Japan = country(name="japan")


for name in cities_in_japan:
    x_ran = random.randint(0, 100)
    y_ran = random.randint(0, 100)
    rand_loc = coordinate(x_ran, y_ran)
    ct = city(name = name, location=rand_loc)
    Japan.add_city(ct)
print(Japan)


for i in Japan.cities:
    x = i.location.x
    y = i.location.y
    plt.text (x,y,i.name)
    plt.scatter(x,y)
plt.show() 
```

# 39
## kv file
```.py
Screen:
    size:500,500
    MDBoxLayout:
        size_hint:.7,.3
        orientation:'horizontal'
        pos_hint:{'center_x':.5,'center_y':.5}
        md_bg_color:0,0.4,1,.25
        MDLabel:
            id: count
            halign:'center'
            text:'Count: 0'
            font_size:'34pt'
            size_hint:.5,1
            color:1,0,0,1
        MDRaisedButton:
            text: 'Add +1'
            font_size:'34pt'
            size_hint:.5,1
            md_bg_color:0,.1,0.35,1
            on_press:
                app.add()
```
## code
```.py
from kivymd.app import MDApp

class quiz039(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0

    def built(self):
        return


    def add(self):
        if self.count < 15:
            self.count += 1
            self.root.ids.count.text = f'Count: {self.count}'


m = quiz039()
m.run()
```
# 40
## kv file
```.py
MDScreen:
    size:500,500
    MDBoxLayout:
        id: main_screen
        orientation:"vertical"
        md_bg_color: "FFFFFF"
        MDLabel:
            id:name
            text: "Masamu"
            halign: "center"
            font_style: "H2"
            theme_text_color: "Custom"
            text_color: 0, 0, 0, 1
            pos_hint: {"center_x": .5, "center_y": .5}
        MDRaisedButton:
            id: button
            text: "Dark Mode"
            pos_hint: {"center_x": 0.06, "center_y": 0.1}
            on_release:
                app.switch()
```
## code
```.py
from kivymd.app import MDApp
class Quiz040(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
    def build(self):
        return
    def switch(self):
        print(self.root.ids.main_screen.md_bg_color)
        if self.root.ids.main_screen.md_bg_color == [1.0, 1.0, 1.0, 1.0]:
            self.root.ids.main_screen.md_bg_color = "000000"
            self.root.ids.button.text_color = 1,1,1,1
            self.root.ids.name.text_color = 1, 1, 1, 1
            self.root.ids.button.text = "Light Mode"
        else:
            self.root.ids.main_screen.md_bg_color = "FFFFFF"
            self.root.ids.button.text_color = 0,0,0,1
            self.root.ids.name.text_color = 0, 0, 0, 1
            self.root.ids.button.text = "Dark Mode"

test = Quiz040()
test.run()
```
