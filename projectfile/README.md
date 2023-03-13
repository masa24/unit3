
![](Assets/DALLE.png)[^1]

[^1]: "a person studying in a classroom on a table in the form of pixel art" by DALL E 2, Open AI, Accessed 7th March 2023

# Unit 3 Project: Japanese Vocab Revision App

## Criteria A: Planning

## Problem definition(Client identification)

Gentaro is a student studying in a boarding school. He is a book worm and has a huge number of books. The issue that he
is currently facing is that he cannot organize his book anymore. Therefor he is requesting a app that can organize your books.
The unique part is that since Gentaro is a boarding school student, he needs a function that manage the location of the books.


## Proposed Solution

Considering Gentaro's requirements, an adequate solution would include a localized computer program with a GUI(
Graphical User Interface) that can store data into a database. Python would be an adequate programming language for the
solution as it is open source, it is mature and supported in multiple platforms (platform-independent) including macOS,
Windows, Linux.[^2]For the database, SQLite would be an adequate solution as it is an embedded, serverless relational
database which means the program and the database can be both localized. 
As for the GUI, KivyMD is chosen for its elegant and simpleness. This GUI framework uses is structured in
object-oriented format and makes the development easy[^4].

[^2]: Python Geeks. “Advantages of Python: Disadvantages of Python.” Python Geeks, 26 June
2021, https://pythongeeks.org/advantages-disadvantages-of-python/.
[^3]: S, Ravikiran A. “What Is Sqlite? and When to Use It?” *Simplilearn.com*, Simplilearn, 16 Feb.
2023, https://www.simplilearn.com/tutorials/sql-tutorial/what-is-sqlite.
[^4]: Gupta, Kaustubh. “What Is KivyMD: Creating Android Machine Learning Apps Using KivyMD.” *Analytics Vidhya*, 6 July
2021, https://www.analyticsvidhya.com/blog/2021/06/creating-android-ml-app-kivymd/#:~:text=KivyMD%20is%20built%20on%20the.

**Design statement**

I will design a Python application running on the KivyMD GUI framework which stores data in an SQLite database for
Gentaro. This application lets Gentaro to add a new boook into the database with the information of title,author,publisher and location.
He will be acle to delete books from the database and all these action will be recorded and will be able to review. 
The app will have a searching funtion to allow you to search a book from multiple search conditions(title,author,publisher and location).
All of the action will be individual for users since all content will be under hashed login system.

It will take approximately 1 month to complete and will be evaluated according to criteria below:

## Success Criteria

1. Users action are independent due to a encrypted login system.
2. The program will allow user input of book information(title,author,publisher and location) and these will be saved in a database.
3. The app has a function to delete book from the database.
4. Users are able to search book from their own database.
5. Users can review their add, delete action.
6. The app shows all the book that the user owns as a table in home screen.

# Criteria B: Design

## System Diagram

![](Assets/VocabApp_SysDia2.jpeg)

**Fig.1** *System diagram of the Japanese Vocab Revision App*

## Data Storage

![](Assets/VocabApp_ER.jpeg)

**Fig.2** *ER diagram of the Japanese Vocab Revision App Database*. This diagram depicts the database structure used to
store the data for this application and how the relationships between table link up the database.

## UML Diagram

![](Assets/VocabApp_UML.jpeg)

**Fig.3** *UML Diagram of the Japanese Vocab Revision App*. This diagram depicts the classes of the application.

## Wireframe

![](Assets/VocabApp_Wireframe.jpeg)

**Fig.4** *Wireframe of the Japanese Vocab Revision App*

## Record of Tasks

| Task No | Planned Action                                           | Planned Outcome                                                                                                                    | Time estimate | Target completion date | Criterion |
|---------|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Planning: Meet with client                      | Find out the issue and find out a possible solution through interview                                                                                       | 10 min         | Feb 8                  | A         |
| 2       | Planning: second meeting with client| define problem and propose solution                                                                      | 30min          | Feb 15                 | A         |
| 6       | Coding the structure of the database                     | Create the database for user and book information                                                                                          | 10min         | Mar 4                  | C         |
| 7       | create database_handler                            | Add a function to the database handler to managage the addition action for the user database and bookinfo database                                     | 10min         | Mar 4                  | C         |
| 8       | Coding the Login and registration Screen and function                 | Add a function of encrypted sign up and login system. Create the user interface for both screen.                        | 30 min        | Mar 4                  | C         |
| 9       | Coding the Home screen                                | Create the MainScreen                                                                          | 30 min        | Mar 4                  | C         |
| 10      | Coding the MDDataTable                                   | Add a MDDataTable in the HomeScreen and make connection with the book                                                                                    | 15 min        | Mar 4                  | C         |
| 11      | Create AddScreen| Create the user interface of the AddScreen                               | 5 min         | Mar 4                  | C         |
| 12      | Create the function for AddScreen | Create funtion for user to add new book info in the bookinfo db.| 40 min        | Mar 4                  | C         |
| 13      | Create SearchScreen                         | Create the SearchScreeen                                                  | 40 min        | Mar 4                  | C         |
| 14      | Coding the search function                               | Create function to Search function.                                                                  | 5 min         | Mar 4                  | C         |
| | | |
| 23      | Creating System Diagram                                  | To have system diagram finished                                                                                                    | 30 min        | Mar 3                  | B         |
| 24      | Creating UML Diagram                                     | To have the UML diagram finished                                                                                                   | 30 min        | Mar 3                  | B         |
| 25      | Creating ER Diagram                                      | To have the ER diagram finished                                                                                                    | 30 min        | Mar 3                  | B         |
| 26      | Creating Flow Diagrams                                   | To have the  flow diagrams finished                                                                                                | 30 min        | Mar 3                  | B         |
| | | |
| 27      | Completing Development Part of Criteria C                | To have interesting parts of my code documented properly                                                                           | 2 hr          | Mar 3                  | C         |
| 28      | Coding: Beautifying Graphical User Interface             | To make the interface more user-friendly and easily understandable                                                                 | 2 hr          | Mar 3                  | C         |
| 29      | Filling Computational Thinking                           | To have the Computational Thinking part of Criteria C of the README file finished                                                  | 1 hr          | Mar 6                  | C         |
| 30      | Creating Test Plan                                       | To have a test plan created for confirming if the application works to standard                                                    | 1.5 hr        | Mar 7                  | C         |
| 31      | Consolidating and commenting code                        | To have the code finalized and organized for easy-understanding                                                                    | 1 hr          | Mar 7                  | C         |
| 32      | Beautifying README file                                  | To have README file consolidated and completed                                                                                     | 20 min        | Mar 7                  | B         |
| 33      | Finish video for Criteria D                              | Video evidence of all the success criteria functioning and working within the developed application                               | 10 min        | Mar 7                  | D         |

## Flow Diagrams

#### Password Authentication

![](Assets/VocabApp_PasswordAuthFlow.jpg)

**Fig.5** *Flow diagram of a Password Authentication system*

#### Vocab Cards & Point System

![](Assets/VocabApp_PointsFlow.jpg)

**Fig.6** *Flow diagram of Point System*

#### Vocab Entry Editing

![](Assets/VocabApp_EditFlow.jpg)

**Fig.7** *Flow diagram of Vocab Editing function*

## Test Plan

| Type                | Description                 | Process                                                                                                                                                                                                                                                                                      | Anticipated Outcome                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unit Testing        | Registration           | 1. Run main.py file <br />2. Click the Register button on the application screen <br />3. Input the appropriate information in each textfield following the hint text<br /> 4. Click Register                                                                                         | when the button is pressed error code is created depending on what stage is the correctness of userinput are. The error is prioritized in the order of overlapping email, not matching the password requirements and the mismatch of password confirmation.|
| Unit Testing        | Login                  | 1. Run main.py file <br />2. Input the appropriate information in each textfield following the hint text <br />3. Click Login                                                                                                                                                         | After clicking the login, if the user doesn't exist, a pop up dialog will appear letting the user know that the username doesn't exist in the database and will prompt the user to go register. If the user and password exists and matches the records in the database, the application should move to the Home Screen.                                                                                                                                                          |
| Integration Testing | Login and Registration      | 1. Run VocabAppMain.py file <br />2. Click the Register button on the application screen<br /> 3. Input the appropriate information in each textfield following the hint text <br />4. Click Register <br />5. Try login with the same credentials registered                                 | If the user followed the on screen instructions properly and registered for a user, then the user should be able to login with the same credentials that were just registered with.                                                                                                                                                                                                                                                                                               |
| Unit Testing        | Search Book           | 1. Run VocabAppMain.py file <br />2. Login with previously registered credentials <br />3. Click "Manage Vocab" on the home screen <br />4. Input into the appropriate fields                                                                                                                | If the fields are inputted correctly and the program didn't find the same vocabulary in the database, the user will be redirected back to the Manage Vocab screen and a pop up dialog will indicate to the user that a vocabulary is added to the database. The user would be able to confirm this by seeing if the entry shows up on the table.                                                                                                                                  |
| Unit Testing        | Add Book         | 1. Run VocabAppMain.py file <br />2. Login with previously registered credentials <br />3. Click "Manage Vocab" on the home screen <br />4. Click the checkbox next to one of the rows <br />5. Click "Delete Vocab" on the bottom bar                                                       | If more than one row is selected, the application will show a popup dialog saying that only one row can be selected. If only one row is checked, the row will be deleted and a pop up dialog should indicate that the vocabulary was deleted successfully. The user would be able to confirm this by seeing if the entry disappeared on the table.                                                                                                                                 |

# Criteria C: Development

## Existing Tools

| Software/Development Tools | Coding Structure Tools       | Libraries  |
|----------------------------|------------------------------|------------|
| PyCharm                    | OOP Structures(Classes)      | Kivymd.app |
| Python                     | SQL requests                 | Passlib    |
| SQLite                     | Databases                    | sqlalchemy |
| KivyMD                     | Encryption                   | kivymd.uix |

## List of techniques used

3. KivyMD Library
4. For loops
5. if statements
6. Password Hashing
7. Interacting with Databases
8. Arrays and Lists
9. Text Formatting

## Computational Thinking

#### Decomposition

In computational thinking, decomposition refers to breaking a complex problem or system into parts that are easier to
conceive, understand, program, and maintain. In this project, one key thing was the point system to store statistics and
the user's performance in the database. As this require multiple steps, I broke down the whole action in the into
collecting user and vocabulary information, calling back to another function inside the database handler and shifting to
the next card in the GUI. Here's a snippet of the the function for adding points.

##### Main Function

```python
def add_points(self):
    global count
    global current_user
    try:
        # Collecting user information and id of the vocabulary
        user_id = current_user.id
        id = vocab_list[count][3]
        # Calling back to the database handler to update the entry
        VocabApp.db.update_user_stats(user_id, id, 1)
        # Log the action
        Logger.info("Points removed successfully")
        # Shifting to the next vocabulary
        count += 1
        self.next_vocab()
    except Exception as e:
        # Error Catching
        Logger.error(f"Error removing points: {e}")
```

##### Database Handler

```python
def update_user_stats(self, user_id, vocab_id, point_change):
    # Queries database for entry specific to the user and the vocabulary
    user_stats = self.session.query(UserStats).filter_by(user_id=user_id, vocabulary_id=vocab_id).first()
    if user_stats is None:
        # If none is found, a new entry is created automatically with base points of 100
        new_user_stats = UserStats(user_id=user_id, vocabulary_id=vocab_id, points=100)
        # Calculate new points according to the input into the function
        new_user_stats.points += point_change
        # Commit changes to the database
        self.session.add(new_user_stats)
        self.session.commit()
    else:
        # If existing entry is found, new points are calculated and committed to the database
        user_stats.points += point_change
        self.session.commit()
    return None
```

#### Pattern recognition, generalization and abstraction

After a user hits the back button on a screen, the text fields on the previous screen still stays in the text fields. So
the next time when the user opens that specific screen again, they would see that inputs from last time still there. To
fix this problem, I implemented a function to clear out all text fields on one screen automatically. Here's the code:

```python
def clear_fields(self):
    self.ids.selected_lesson.text = ""
    self.ids.selected_part.text = ""
    self.ids.selected_hiragana.text = ""
    self.ids.selected_katakana.text = ""
    self.ids.selected_english.text = ""
    self.ids.selected_save.text = "Save"
    self.ids.selected_save.on_press = self.add_vocab
```

As you can see this code is very repetitive. Thus I decided to use a for loop over a list to integrate over each text
field until they're all empty.

```python
  def clear_fields(self):
    fields_to_clear = ['selected_lesson', 'selected_part', 'selected_hiragana', 'selected_katakana',
                       'selected_english']
    for field in fields_to_clear:
        self.ids[field].text = ""
    self.ids.selected_save.text = "Save"
    self.ids.selected_save.on_press = self.add_vocab
```

In the code above, instead of manually setting each field to an empty string, I'm using a loop to iterate through a list
of field names and set each one to an empty string. This would make the code more concise and easier to modify if you
ever need to add or remove fields.

#### Algorithms

An algorithm is a step-by-step procedure for solving a problem or performing a task. One action requiring constant usage
is the function for inserting vocabulary into the database. The function takes in several inputs (lesson, part,
hiragana, katakana, and definition) and performs a series of steps to insert a new vocabulary into the database. The
steps include checking if the vocabulary already exists in the database, creating a new Vocabulary object, adding it to
the database session, and committing the changes. Here's a snippet of the code:

```python
  def insert_vocab(self, lesson, part, hiragana, katakana, definition):
    # Queries database for if the vocabulary exist rather than first(), saves on time when table has multiple records
    exists = self.session.query(Vocabulary).filter_by(hiragana=hiragana).exists()
    # Checks if vocabulary exists already
    if exists:
        print("Vocab already exists")
        return False
    else:
        # Create a new vocabulary object
        new_vocab = Vocabulary(lesson=lesson, part_of_lesson=part, hiragana=hiragana, katakana=katakana,
                               definition=definition)
        self.session.add(new_vocab)
        # Committing changes
        self.session.commit()
        print("Vocab added")
        return None
```

## Development

### Object Oriented Programming

Object Oriented Programming(OOP), is a programming paradigm that focuses on creating objects that can contain both data
and behavior. In OOP, objects are instances of classes, which define the properties and methods that the objects will
have. The main advantages of OOP include Modularity, Reliability, Encapsulation, Abstraction and Polymorphism. The whole
vocabulary app is constructed using OOP to make it more simple to debug and for future developers to add/change
features. Here's a snippet of how OOP was used to organize the code:

```python
class PerVocabManageScreen(MDScreen):
    def __init__(self, **kwargs):

    # Code omitted for demonstrative reasons
    def on_pre_enter(self, *args):

    # Code omitted for demonstrative reasons
    def add_vocab(self):

    # Code omitted for demonstrative reasons
    def clear_fields(self):

    # Code omitted for demonstrative reasons
    def save_changes(self):
# Code omitted for demonstrative reasons 
```

As seen above, each screen has its own class and each action is housed under a function so everything is very clear and
easy-to-understand.

### ORM

Object Relation Mapping(ORM), is a programming technique that allows developers to interact with a relational database
using an object-oriented programming paradigm. In traditional programming with relational databases, developers use SQL
statements to interact with the database. This involves writing SQL code to retrieve, update or delete records in the
database. However, with ORM, developers can interact with the database using an object-oriented approach, which is more
intuitive and easier to work with. ORM frameworks provide a layer of abstraction between the application and the
database. They map database tables to classes in the application, and map columns to properties of those classes. This
allows developers to work with objects in their code, rather than having to write SQL code to interact with the
database. Here's a snippet of code to show the difference with and without ORM:

```sql
SELECT *
FROM users
WHERE username = "Bernard"
```

This is a normal SQL statement that can be executed in python through running a query with the sqlite3 library. This is
a language with a low level of abstraction.

```python
db.session.query(Users).filter_by(username="Bernard").first()
```

This is the same query done through ORM and a library called SQLAlchemy. SQLAlchemy is a popular open-source ORM
framework for Python that provides a set of tools for working with relational databases using Python code. It was first
released in 2006 and has since become a widely used tool in the Python community for interacting with databases.
SQLAlchemy provides a high-level API for working with databases, allowing developers to interact with databases using
Python classes and objects rather than SQL statements. Here's an example of how tables are created in SQLAlchemy with
ORM:

```python
class Vocabulary(Base):
    __tablename__ = 'vocabulary'
    id = Column(Integer, primary_key=True)
    lesson = Column(Integer, nullable=False)
    part_of_lesson = Column(Integer, nullable=False)
    katakana = Column(String, nullable=False)
    hiragana = Column(String, nullable=False)
    definition = Column(String, nullable=False)
    stats = relationship("UserStats", back_populates="vocabulary", order_by="UserStats.id")
```

### Code Organisation

When dealing with a complex program, especially ones with a graphical user interfaces, it is a good practice to
separate the front-end and back-end development. That can make finding code easier and let you be able to group
frequently used functions together instead of writing repetitive code over and over which can make debugging a lot
harder. In my program, I chose to separate my code into four parts : the KV file, the python program that interacts with
the UI elements, a database handler and a models file to define the table structures.

![](Assets/VocabApp_CodeStruct.jpg)

**Fig.8**  *Diagram showing how code is organised in the app*

As seen above, my code is separated into four parts. That makes debugging and changing features in the future easier and
more straightforward.

### Inserting Data

Throughout the development process of the app, uncountable times of testing was done to make sure that the code
functions as per my client's request and one of the main areas I tested was the database access. I had to constantly
insert data into the database and try to interact with them inside the GUI. As the inserting of the same data was very
time consuming and repetitive, I decided to write a small program in python which inserts dummy data into the database
for testing. Here's the code:

```python
# create an engine and session
engine = create_engine('sqlite:///vocab_app.db', echo=True)
Session = sessionmaker(bind=engine)
session = Session()
# create some dummy data for the Vocabulary table
dummy_data = [
    {'lesson': 1, 'part_of_lesson': 1, 'katakana': 'ア', 'hiragana': 'あ', 'definition': 'a'},
    {'lesson': 1, 'part_of_lesson': 2, 'katakana': 'イ', 'hiragana': 'い', 'definition': 'i'},
    {'lesson': 1, 'part_of_lesson': 3, 'katakana': 'ウ', 'hiragana': 'う', 'definition': 'u'},
    {'lesson': 1, 'part_of_lesson': 4, 'katakana': 'エ', 'hiragana': 'え', 'definition': 'e'},
    {'lesson': 1, 'part_of_lesson': 5, 'katakana': 'オ', 'hiragana': 'お', 'definition': 'o'},
]
# insert the dummy data into the Vocabulary table
for data in dummy_data:
    vocab = Vocabulary(**data)
    session.add(vocab)
# commit the changes to the database
session.commit()

```

### Point System

One key feature that my client requested was a system to keep track of the learning progress of the user. After weighing
multiple scoring/statistics systems, I decided to use a system where 100 is the base score per user per vocabulary and
points are added/deducted based on the user's feedback on the Vocabulary Cards. To store this data, I created a table
that has relations with the `users` table and the `vocabulary` table to make referencing easier and functions in
the `database_handler` to change the score accordingly.

#### Table Structure

```python
class UserStats(Base):
    __tablename__ = 'user_stats'
    id = Column(Integer, primary_key=True)
    user_id = Column(Integer, ForeignKey('users.id'))
    vocabulary_id = Column(Integer, ForeignKey('vocabulary.id'))
    points = Column(Integer, nullable=False, default=100)
    # One-to-many relationships with users
    user = relationship("Users", back_populates="user_stats")
    # One-to-many relationships with vocabulary
    Users.user_stats = relationship("UserStats", order_by=id, back_populates="user")
    # Many-to-one relationship with Vocabulary
    vocabulary = relationship("Vocabulary", back_populates="stats")
```

#### Database Handler

```python
def update_user_stats(self, user_id, vocab_id, point_change):
    user_stats = self.session.query(UserStats).filter_by(user_id=user_id, vocabulary_id=vocab_id).first()
    print(f"User stats: {user_stats}")
    if user_stats is None:
        # Creates base statistics for entries that don't exist
        new_user_stats = UserStats(user_id=user_id, vocabulary_id=vocab_id, points=100)
        new_user_stats.points += point_change
        self.session.add(new_user_stats)
        self.session.commit()
    else:
        # Updates entry
        user_stats.points += point_change
        self.session.commit()
    return None
```

### Randomized Vocabulary Mode

Also according to my client's request is the ability for the application to choose the vocabulary that the user's is
relatively weaker at for more revision. To achieve this, I built a function in `database_handler` to retrieve the user's
statistics and order the vocabulary with the lowest points to show first.

```python
def get_vocab_by_user_stats(self, user_id):
    # get all vocabs from user stats where user_id = user_id sort by points ascending
    vocab = self.session.query(Vocabulary).join(UserStats).filter(UserStats.user_id == user_id).order_by(
        UserStats.points).all()
    return vocab
```

### MDTextField / JapaneseTextField

```kv
<JapaneseTextField@MDTextField>:
    font_name: 'Japanese.ttc'
    input_type: 'text'

JapaneseTextField:
            id: selected_hiragana
            size_hint: .8,1
            pos_hint: {"center_x":.5}
            hint_text:"Hiragana"
            helper_text: "Enter Hiragana of vocab"
            helper_text_mode: "on_error"
```

Throughout the whole program,
an essential element of the graphical user interface was to allow my client to input text into the program.
This is an example of the text fields used to input Japanese into the app.
Because KivyMD doesn't support Japanese characters, I had to use a specific font for the text field.
As this would cause very repetitive code having to redefine the font file.
I created a specific object  ```<JapaneseTextField@MDTextField>```
that lets me define the font for the text field only once.

### MDDialog

```.kv
successdialog = MDDialog(
                title="Success",
                text="User registered successfully",
                size_hint=(0.8, 0.3),
                buttons=[
                    MDFlatButton(
                        text="OK",
                        on_release=lambda x: successdialog.dismiss()
                    )
                ]
            )
            successdialog.open()
```

This is an example of ```MDDialog``` used in my code to indicate to the user that an internal action was completed,
because otherwise the program would be not intuitive as the user would have no way to tell if an action is completed
properly. With the ```MDDialog``` implemented, the user is able get real-time feedback on if the program is performing
an action under the hood.

### Text Formatting in MDDataTable

```python
for row in rows:
    temp_hiragana = f"[font=Japanese.ttc]{row.hiragana}[/font]"
    temp_katakana = f"[font=Japanese.ttc]{row.katakana}[/font]"
    row = [str(row.id), str(row.lesson), str(row.part_of_lesson), temp_hiragana, temp_katakana,
           row.definition]
    if row not in self.data_table.row_data:
        self.data_table.row_data.append(row)
```

Above is the code to process the Japanese characters from the database before they get shown on the ```MDDataTable```.
This is because if a font that supports Japanese characters is applied,
it wouldn't include the Kivy-specific icons and assets(e.g: checkboxes and page-turning buttons)
needed to render the table.
However,
the Kivy-specific font that includes all the icons and assets required by Kivy would not support Japanese characters.
Thus,
I decided
to format the Japanese text with specific headers and footers
to tell Kivy to render the specific Japanese characters with that font.

### Data Validation for email addresses

To make sure the email addresses are actually usable and contactable, I decided to validate the email addresses format
before inserting them into the database.
To implement this policy, I decided to use the `re` library in python to
validate if the user inputted a valid email address.
I first defined the pattern which for an email,
is `r"[^@]+@[^@]+\.[^@]+"`, I then used the `re.match()` function to check if the inputted text matches the previously
defined format.
If the pre-defined format is not matched, it would show an error and prompt the user to type in their
email address again.
Here's the code:

```python
# Regular expression pattern for email validation
email_pattern = r"[^@]+@[^@]+\.[^@]+"

# Validate the email format
if not re.match(email_pattern, email):
    # Show an error message
    self.ids.email.error = True
    self.ids.email.helper_text = "Invalid email format"
    self.ids.email.helper_text_mode = "on_error"
```

### MDFillRoundFlatIconButton

`MDFillRoundFlatIconButton` is one of the many buttons styles available in Kivy. I started out using `MDRaisedButton`
for everything, but the further into the coding process, I realized that there are a lot more button styles that can
make my application more intuitive. I'm using this type of button on my login screen.

```kv
MDFillRoundFlatIconButton:
    id: login_button
    text: "Login"
    icon: "login"
    pos_hint: {"center_x": 0.5}
    on_release: root.login()
    md_bg_color: app.theme_cls.primary_color
    size_hint_x: 0.8
    disabled: not uname.text or not pwd.text
    disabled_color: app.theme_cls.disabled_hint_text_color
    elevation_normal: 12 if uname.text and pwd.text else 0
    _md_bg_color_disabled: app.theme_cls.disabled_hint_text_color
    _md_bg_color_active: app.theme_cls.primary_light
```

As seen in the code above, the button is disabled if the `uname` or `pwd` input fields are empty, and its background
color is set to the application's theme color for disabled text. When clicked, it calls the `login()` method of the
widget's root object. The button has a shadow of 12 pixels when the `uname` and `pwd` input fields have text, and its
background color changes to a lighter shade of the primary color defined in the application's theme when pressed.

### MDFloatingActionButton

`MDFloatingActionButton` is one of the other many button styles in KivyMD. This type of button includes an icon as its
main focus. It can replace text with icons that represent self-explanatory functions, not to mention they are more
intuitive and less graphic heavy on the GUI. Thus, I chose to use this button on the Home Screen of the application.
Here's a snippet of code showing the logout button:

```kv
MDFloatingActionButton:
  id: logout
  icon: "logout"
  text: "Logout"
  halign:"right"
  md_bg_color: app.theme_cls.accent_color
  text_color: app.theme_cls.text_color
  pos_hint: {"center_x": .5, "center_y": .5}
  on_press:
      root.logout()
```

### Color Theme

As per my client's request, he requires a unified color theme to the whole application.
To achieve this, instead of manually keeping track of which UI element uses which color,
I defined a color scheme on the top of my Kivy file
and just call back to this color theme every I need to refer to the colors.

```kv
# Define custom color scheme
<CustomTheme>:
    primary_palette: "Blue"
    accent_palette: "Green"
    theme_style: "Light"
    primary_hue: "500"
```

# Criteria D: Functionality

## Demonstration Video

[Click here for the Video](https://drive.google.com/file/d/1itqrEy7QBwmW7Ril9mgh4pWVQhMVW6aM/view?usp=share_link)

# Appendix

### First meeting with client

![](Assets/MeetingNotes1.jpg)

**Fig.9** *Rough notes from first meeting with client, includes basic ideas behind client's app*

### Success Criteria Meeting(Second Meeting)

![](Assets/MeetingNotes2.jpg)

**Fig.10** *Rough notes from second meeting with the client, includes details of success criteria*




