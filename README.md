# Build a Mario Game Controller
In this lab we will build a game controller for a Mario game. Since this is a large project, we'll complete it in four stages:
1. Build a circuit with one button and make Mario jump when that button is pressed
2. Add two more buttons so that Mario can also walk left and right
3. Write code so that if Mario jumps on top of Goomba, then Goomba is "squished"
4. Write code so that if Goomba touches Mario when Mario is on the ground the game ends

### Step 1: Build a circuit with one button that can make Mario jump
Our Game Controller will use the following parts:
- Three (or more) push buttons
- A 10KΩ resistor for each push button
- Jumper wires   

Use the picture below to make sure you are using correct 10KΩ resistor.   
![](Theremin1.png)   
   
Use the following circuit diagram to construct a circuit with one push button. The direction of the 10KΩ resistor is unimportant.   
![](GameController1.png)

### Step 2: Test the circuit
Test it with a forever loop that says *Digital reading 2*. Press the button to make sure that display changes from *true* to *false*.

### Step 3: Download the artwork for the Mario game and open it in S4A
Right click [`MarioBase.sb`](MarioBase.sb) and choose *Save link as*. Save the file to your *Scratch Projects* folder in your *My Documents* folder. Open the S4a program and then choose *File | Open* and browse to and select `MarioBase.sb`.

### Step 4: Write code to make Mario jump
In the Mario sprite, create a forever block that checks if the button is pressed. If it is, make Mario go up and then down. You should have Mario switch costumes to make a more realistic jump

### Step 5: Add two more buttons and code to make Mario walk
Add two buttons to your Arduino and create circuits for each. To create an animation of walking, switch back and forth between two walking costumes. Mario should move in the x direction with each costume switch. Use *wait* to pause Mario after each step. Adjust the values until you are happy with Mario's walk

### Step 6: Add the Goomba "squish"
Now we are going to add code to the Goomba sprite in our Mario program so that if Mario is jumping and he lands on the Goomba, the Goomba will squish. Add a forever loop to the Goomba sprite and:
 * create an if statement that checks to see if the Goomba is touching Mario and Mario's y position is greater than -110. If that is true:
    * set the Goomba's y to -140
    * switch the Goomba's costume to squish,
    * have the Goomba think "Hmm" for 2 seconds 
    * change the costume and y back to what they were
 * Include a wait in the forever loop so that the if statement is checked every .1 seconds.
You may find the blocks in the attached picture useful in solving this problem. To test your code, just click and drag Mario on top of the Goomba.      
![](GameController2.png)

### Step 7: Ending the game
Create a forever block for the Mario sprite to check if he touches Goomba when he is on the ground
If he does, have him change his y coordinate to -115 and point him in the 0 direction (up)
You can test your program by dragging Mario with the mouse. If Mario is in the air, the goomba should squish, but if Mario is on the ground he should die
![](GoombaSquish.gif)
### Step 8: Submit your finished program
The steps listed above are just suggestions to get you started. Your Mario game doesn't have to work or look like any other. Have fun and be creative. When you are finished, have your teacher or a TA verify that you have a working program. Submit your finished program by uploading the .sb file to Google classroom. You should be able to find it in *My Documents | Scratch Projects*. If you worked with a partner, each partner should submit a copy of the finished program to Google classroom.
