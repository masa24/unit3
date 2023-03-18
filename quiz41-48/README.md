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
# 46
```.py
import sqlite3

haiku = """Code flows like a stream
Algorithms guide its way
In silence, it solves"""

#Database Version
class database_handler:
    def __init__(self,dbname):
        self.connection = sqlite3.connect(dbname)
        self.cursor = self.connection.cursor()

    def create_table(self):
        query = f"""CREATE TABLE if not exists words(
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            word TEXT NOT NULL,
            w_length INTEGER NOT NULL
            )"""
        self.run_query(query)

    def avg(self):
        query = f"""select avg(w_length) from words"""
        self.run_query(query)
        a = db.cursor.fetchone()
        return a

    def run_query(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()

db = database_handler("quiz046")
db.create_table()


for word in haiku.split():
       query = f"""INSERT into words (word, w_length) VALUES('{word}', {len(word)})"""
       db.run_query(query)


result = db.avg()
db.close()

print(f'average word length is {result}')

```
# 47
## update

```.py
def update(self):

        #This function updates all the labels in the form using the base salary and the percentage
        # Pseudocode
        # 1- get the base salary from the GUI
        base = self.root.ids.base.text
        hash = ""
        # 2- if base salary define total=int(base) and an empty string to store build a hash (for_hash="") if no base then end the function
        test_field_ids = [ 'health', 'pension', 'income_tax','inhabitant']
        if base !="":
            total = int(base)
            hash += f"base{total}"

            for i in test_field_ids:
                value = self.root.ids[i].text
                if value !="":
                    new_value=f"{int(value)*int(base)/100} JPY"
                    total-= int(value)*int(base)/100
                    hash+=f"{i}{value}"
                else: new_value="JPY"
                label_id=f"{i}_label"
                self.root.ids[label_id].text= new_value

            hash += f"total{int(total)}"
            self.root.ids.salary_label.text = f"{total} JPY"
            hashed = encrypt_pswd(hash)
            self.hash = hashed
            self.root.ids.hash.text = hashed[-50:]
```

## save

```.py
def save(self):
        def save(self):
            base_widget = self.root.ids.base
            base = base_widget.text.strip()
            values = {
                "base": self.root.ids.base_label.text.strip()[:-4],
                "inhabitant": self.root.ids.inhabitant_label.text.strip()[:-4],
                "income_tax": self.root.ids.income_tax_label.text.strip()[:-4],
                "pension": self.root.ids.pension_label.text.strip()[:-4],
                "health": self.root.ids.health_label.text.strip()[:-4],
                "salary": self.root.ids.salary_label.text.strip()[:-4],
                "hash": self.hash,
            }

            query = "INSERT INTO payments (base, inhabitant, income_tax, pension, health, total, hash) VALUES (?, ?, ?, ?, ?, ?, ?)"
            db = database_worker("payments.db")
            try:
                db.cursor.execute(query, [values[key] for key in values.keys()])
                db.connection.commit()
                self.root.ids.hash_label.text = "Payment saved"
            except Exception as e:
                print(f"Error saving payment: {e}")
            finally:
                db.close()
        self.root.ids.hash.text = f"Payment saved"

```

## checking hashed transactions (HL)

```.py
def check(self):
        conn = sqlite3.connect('payments.db')
        cursor = conn.cursor()
        cursor.execute("SELECT * FROM payments")
        rows=cursor.fetchall()

        for row in rows:
            get_hashed = encrypt_pswd(f"base{row[1]}inhabitant{row[2]}income_tax{row[3]}pension{row[4]}health{row[5]}total{row[6]}")
            if get_hashed[-50:] == row[7]:
                print("OK")
            else:
                print(f"Error in id: {row[0]}")
```
