# 41
```.py
from kivymd.app import MDApp
import math


class quiz041(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)

    def build(self):
        self.order = 0
        self.list = {'tl':[1, 0],'tm':[2, 0],'tr':[3, 0],
                     'ml':[4, 0],'mm':[5, 0],'mr':[6, 0],
                     'bl':[7, 0],'bm':[8, 0],'br':[9, 0],}

        return

    def create_list(self):

        self.p1 = []
        self.p2 = []
        for i in self.list:
            if self.list[i][1] == 1:
                self.p1.append(self.list[i][0])
                print(self.p1)
            if self.list[i][1] == 2:
                self.p2.append(self.list[i][0])
                print(self.p2)
            self.check_win()

    def check_win(self):
        pattern = [(1, 2, 3), (4, 5, 6), (7, 8, 9),
                   (1, 4, 7), (2, 5, 8), (3, 6, 9),
                   (1, 5, 9), (3, 5, 7)]
        for i in pattern:
            print(i[0],i[1],i[2])
            print('')

            if i[0] in self.p1:
                if i[1] in self.p1:
                    if i[2] in self.p1:
                        self.root.ids.player.text = 'Player 1 win'
            elif i[0] in self.p2:
                if i[1] in self.p2:
                    if i[2] in self.p2:
                        self.root.ids.player.text = 'Player 2 win'




    def function(self,name):
        button = 'self.root.ids.' + name
        mark = eval(button)
        self.order += 1
        while self.list[name][1] == 0:
            if self.order%2 == 1:
                mark.md_bg_color = 0, 100, 0, 1
                mark.text = 'X'
                self.list[name][1] = 1
                self.root.ids.player.text = 'player 2 turn'
#                print(self.list)

            else:
                mark.md_bg_color = 0, 0, 100, 1
                mark.text = 'O'
                self.list[name][1] = 2
                self.root.ids.player.text = 'player 1 turn'
            self.create_list()


    def close(self):
        exit()


task = quiz041()
task.run()
```
```.py
Screen:
    size:500,500
    MDLabel:
        id:title
        color:0,90,0
        font_size:'40pt'
        id: title
        text: 'Tik Tak To by Masamu'
        halign:'center'
        pos_hint: {'center_y':.9}

    MDLabel:
        id:title
        color:0,90,0
        font_size:'20pt'
        id: player
        text: 'player 1 turn'
        halign:'center'
        pos_hint: {'center_y':.8}


    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:mm
        text: ''
        pos_hint: {"center_x":.5, "center_y":.4}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('mm')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:ml
        text: ''
        pos_hint: {"center_x":.2, "center_y":.4}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('ml')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:mr
        text: ''
        pos_hint: {"center_x":.8, "center_y":.4}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('mr')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:tm
        text: ''
        pos_hint: {"center_x":.5, "center_y":.6}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('tm')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:tl
        text: ''
        pos_hint: {"center_x":.2, "center_y":.6}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('tl')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:tr
        text: ''
        pos_hint: {"center_x":.8, "center_y":.6}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('tr')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:bm
        text: ''
        pos_hint: {"center_x":.5, "center_y":.2}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('bm')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:bl
        text: ''
        pos_hint: {"center_x":.2, "center_y":.2}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('bl')

    MDRaisedButton:
        md_bg_color:.8,.8,.8,1
        id:br
        text: ''
        pos_hint: {"center_x":.8, "center_y":.2}
        font_size:'20pt'
        size_hint: .3, .2
        on_press:   app.function('br')

```
# 42
```.py
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen


class MysteryA(MDScreen):
    def messageA(self):
        self.ids.textA.text = "This is mystery A. you pressed a button"

class MysteryB(MDScreen):
    def messageB(self):
        pass

class quiz042(MDApp):
    def build(self):
        return


test = quiz042()
test.run()
```
```.py
ScreenManager:
    MysteryA:
        name: "MysteryA"
    MysteryB:
        name: "MysteryB"

<MysteryA>:
    MDLabel:
        id: textA
        text: "Welcome"
        halign: "center"
    MDRaisedButton:
        text: "Click Me"
        on_press: app.root.current = "MysteryB"
        on_press: root.messageA()

<MysteryB>:
    MDLabel:
        id: textB
        text: "This is mystery pageB. You pressed a button"
        halign: "center"
    MDRaisedButton:
        text: "Click Me"
        on_press: app.root.current = "MysteryA"
```

# 43
```.py
CREATE TABLE if not exists movie(
    id INTEGER PRIMARY KEY,
    name text,
    producer text,
    director text,
    category text,
    year int,
    budget int
);

INSERT INTO movie(name,producer,director,category,year,budget) values('Top Gun','Tom Cruise','Tony Scott','action drama',2022,15000000);
INSERT INTO movie(name,producer,director,category,year,budget) values('Avatar','James Cameron','Jon Landau','action drama',2009,250000000);
```
# 44
```.py
select name from sqlite_master where type = "table";

select count(*) from INHABITANT where gender = "Male" and state = "Friendly";

select avg(gold) from INHABITANT group by villageid;

select count(*) from ITEM where item like "A%";

select count(distinct job) from INHABITANT;

select item from ITEM, INHABITANT where INHABITANT.personid = ITEM.owner and INHABITANT.job = "Herbalist";
```
# 45
```.py
SELECT
  CASE
    WHEN total_deposit - total_withdraw != balance THEN 'bad'
    ELSE 'good'
  END AS 'Status',
  total_deposit,
  total_withdraw,
  balance,
  account_id
FROM (
  SELECT
    SUM(amount) AS total_deposit,
    account_id AS a_d
  FROM transactions
  WHERE transaction_type = 'deposit'
  GROUP BY account_id
),
(SELECT
    SUM(amount) AS total_withdraw,
    account_id AS a_w
  FROM transactions
  WHERE transaction_type = 'withdraw'
  GROUP BY account_id
),
accounts
WHERE a_d = a_w
  AND a_d = accounts.account_id;
```
