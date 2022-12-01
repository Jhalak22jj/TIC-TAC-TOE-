Ursina Explanation:


Ursina is open Source python package distribution.

It helps to develop small indie games.By using this library we can create 

2-dimensional games & 3-dimensional games also.Not only games we can develop 

Gui software by using this game engine. 

When you’re comparing this library with other game engines in python, 

Suppose when you compare this game engine with the arcade library,

i noticed one thing  when i compile the code with ursina engine it takes very

 less time than arcade.



In the arcade library,you can develop only 2dimesnional games,

But in the ursina library you can develop 2D and 3D games. 

And one more option when we’re creating the 3d games.

The camera angle is very important;This library has some features 

you can easily implement & understand the camera angling techniques

 by using this; it helps to create a good interaction with the game that you develop.


By the way In case of understanding the code, 

ursina library provides a good documentation facility that helps to understand

 the methods,parameters that are built in it.



Platform facility: Urisna library only works on windows & Linux platform. 

That’s all about the explanations.

 

Libraries Installations: pip install ursina 

 


First you need to install the urisna package for creating the game.So Open your 

command prompt and pip install ursina. This command will help you to install this 

package. Probably it takes some time because it uses the Panda3d library to make

 the 3d visualizations in this game.


The panda3d library is a 3d object development library it helps to develop 3d modeling

 in this ursina engine.


Step 1: 
 

from ursina import *
app=Ursina()







After installing this library you’ve to open the visual studio code and  import the ursina

 library. Next we need to create a game window and inside this game window object

 you need to insert your elements that are going to use

in the game.

 

Step 2: 

  

camera.orthographic = True 

 


First process is we’ve to set the camera angling.So type camera.orthographic.  

Orthographic is a kind of projection,This projection is used to represent the three 

dimensional objects in two dimension screens. When you’re inserting the 3D 

objects in the game at end you can play the game with a two dimensional window

 screen. So We can’t play games on 3d dimensional screens.So this what the

 orthographic is.


You’ve to set the orthographic projection as true.So only we can get the orthographic

 projection in this game.

 

Step 3:  

 

camera.fov=4 

 


Next step is we’re going to create a field of view. This parameter decides what are 

things the player needs to see in the game.And in the field of view give the value as 4.


Step 4: 
 

camera.position=(1,1) 

 

After that create another parameter that is called a camera.position.

 And in this parameter you need to pass the x values and y values in a tuple.

 


So we finished the camera angles.Now we need to create the entities and an

entity is the basic term in the game development field.Entities are the objects 

that are present in the game now we’re going to create the entities for this game.


Step 5: 
 

player=Entity(name='O',color=color.azure)
cursor=Tooltip(color=player.color,origin=(0,0),scale=4,enabled=True)
cursor.background.color=color.clear

bg=Entity(parent=scene,model='quad',texture='shore',scale(16,8),z=10,

color=color.light_gray)
mouse.visible=True
 




Declare a variable called as player and in this variable call the object entity.

So in this library if you want to create an entity you need to call this object and 

pass your requirements as a parameter in this object. This is the way to create 

an entity.


Now create a variable called a cursor and in this variable pass the object Tooltip,

So this object is used for customizing the game cursor.

Next we need to create a game background entity, create an entity object and  pass

 the parameters like models, textures to customize the background of our game.

 


So we created the entities for our game.Now you’ve to understand that in the TicTacToe 

game we need a board to play the game.In the game board there must be 9 cells 

with 3 rows and 3 columns. This is the basic structure of a tic tac toe game.


 
 

 

 

Step 6 :


board=[[None for x in range(3)]for y in range(3)]
for y in range(3):
    for x in range(3): 

 First you need to create a game board with 3 rows and 3 columns.

Declare a variable called board in this board i created two for loops. 

The first forloop holds the variable x that means it traverses through 

row wise manner and y variable forloop traverse through the column wise manner.

Why we’re traversing means..! We are creating the tiles by using this forloop traversals. 

Step 7: 

b=Button(parent=scene,position=(x,y))
        board[x][y]=b



So we need 9 cells. That is why we’re passing the range value of 3 in the both for loops.

Next create a variable b this is for the creation of buttons and in this object pass 

the parameter like parent and positions this parameters helps to place the buttons

 in game


And create a matrix variable called board[x][y] .So this variable helps to

 identify the winners at the end of this game . And pass the value as b

 

Step 8:  

 def on_click(b=b):
            b.text=player.name
            b.color=player.color
            b.collision=False
            checkforvictory()

            if player.name=='O':
                player.name='X'
                player.color=color.orange
            else:
                player.name='O'
                player.color=color.azure

            cursor.text='' "
            cursor.color=player.color
        b.on_click=on_click 
 

So next declare a function called onclick(). We’re going to define the onclick functions.

Suppose when you click the first cell it will print  ‘O’ in the cell.

 To identify that click we’re defining colors When you click the cell it changes the cell 

color.So this is the concept of this game project.

 


Next  create conditions Simply it defines the color of players. There are two players in 

the game called ‘O’ & ‘X’.

The player 'O’ has the color of azure pattern and ‘X’ has the color of orange pattern. 

So this is the condition that we’re inserted and another thing is we’ve to insert the

 cursor color and cursor text. 


So this is the logic that we need to create this game.Initially you can feel a little bit hard

 to understand But don’t worry once practice the game development projects  and

 it will increase your logic abilities.

 



We finished some important logic for this game actually. 

This game is a very simple one and it is easy for the beginners to understand the 

logic of this game.

 

Step 9 :

def checkforvictory():
    name=player.name
    won = (
    (board[0][0].text == name and board[1][0].text == name and board[2[0].text==name))

 


Now we need one important logic that is the winning logic of this game.At the end of 

this game we’ve to declare the winner of this game.For that  just write the logic

 for winning.


Create a function called checkforvictory() and in this function we’re going to write the 

logic of the game.Winning logic is very simple one i will tell you the concept before

 create variable won and in this variable we’re going to write the 9 logic for identifying

 the winners in this game.I’m not going to cover all the logic.I'm going to explain the 

one logic you can easily understand rest of them.

 

Winning logic Explanation : 

 

* (board[0][0].text == name and board[1][0].text == name and board[2[0].text==name)  

 


So first you see the logic condition that explains that board[0][0].text==name of the player. 

The board of [0][0] it is equal to any player name either it must be player “O’’or “X’’.

Same logic is applied on the next cell,here we’re defining the each cells like board of 

row &column.First matrix indicates row value and second one is Column value .

In the second one board[1][0] it is equal to any player names Same for the third

 cell board[2][0] it may be any player name. 

And our logic is if these three cells got the same player name then

 the player is declared as winner.So this is the first  winning condition totally eight 

winning conditions are available you’ve to try all the possible cell combinations in this 

game to produce correct results.Totally there are nine condition are available and but 

expect eight conditions one condition is used for draw.

 

Step 10 : 

if won:
        print('Winner is:',name)
        destroy(cursor)
        mouse.visible=True
        Panel(z=1, scale=10, model='quad')
        t = Text(f'Player\n{name}\nwon!', scale=3, origin=(0,0), background=True)
        t.create_background(padding=(.5,.25), radius=Text.size/2)
        t.background.color = player.color.tint(-.2)
app.run() 

 


And We finished all the logic If any player won the game by using above logic

 So our program will highlight the player name So this is the final step of this program.


So That’s all about the code, let's run this program.

 
