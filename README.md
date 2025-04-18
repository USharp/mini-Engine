## What is it?
---
mini - an engine created with the goal of creating a simple but functional engine for pixel games. The engine has 10 simple commands, so you can learn it in an evening.

>10 commands, 100 lines of code, 1000 possibilities.

- Python 3.8 or higher is required
- PyGame 2.6.1 or higher is required

The engine does not require cramming for 1000 years. However, the complexity of the project will depend only on its scale.

---

## Important!
>The engine provides only input/output in basic functionality.
>You will have to write most of the things yourself.
>But that's the point! You understand your game at the lowest level.

## 1. Initialization and first steps.
The very first thing you need to do is, of course, import the library.
```python
import mini_engine as mini # "as" optional
```
The next step is to create an engine object.
```python
engine = mini.MiniEngine(10, 64, 64, "MyCoolGame", "icon.png")
```
Let's break down the code piece by piece.
We created an engine object, which we will refer to in the future. You can call it anything, even a horse, the main thing is that it is convenient.
We assigned the MiniEngine class to it. Without it, nothing will work.
But we are not interested in this, we are more interested in the parameters.
### 1 parameter is responsible for the pixel size.
Basically, pixel games will be made here. The most optimal is 10.
### 2 and 3 parameters

responsible for the window size in PIXELS that we specified earlier

---
### Parameter 4
It is responsible for the window name.

And finally...
### Parameter 5
It is responsible for the window icon. You need to specify a relative/full path to the icon image.
>It is recommended to use JPEG/PNG.
---
Finally, we figured out the window.
## 2. The main loop
```python
while engine.is_running():
engine.update()
engine.tick(60)
```
There are already more lines here, but the purpose of what you are reading is to explain it to you.
### engine.is_running()
Returns us the value True or False. From the name it is not difficult to guess that it tells you whether the engine is running.
>Or maybe it is not?

Unless the user closes the window.
### engine.update()
It refreshes the screen, but we'll get to that later.
### engine.tick()
This thing tells the game how many FPS to give it.
>And what is this FPS of yours?

If gamers understood me right away, then an explanation for those who are in slippers:
>FPS is how many pictures per second to show you.
>But shouldn't it be 1?

No, if you specify 1, your game will be like a slide show from 1995. The most optimal value is 60 or 30.

---
Congratulations, we've finished the topic of the cycle. FINALLY!
## 3. The main functions of the engine.
I think you're already tired, so let's run through everything briefly.
### engine.draw_pixel()
```python
engine.draw_pixel(3, 10, (255, 0, 0)
```
#### Parameter 1 and 2
Responsible for the position of the pixel. 1 - by X, 2 - by Y. In this example, it is drawn 3 pixels from the left edge of the screen, and 10 from the top.
#### Parameter 3
Responsible for the color. It is specified in RGB format.
>WHAT IS RGB?!??

Relax, it's not that difficult.
>RGB is 3 digits that the computer eats, does magic and shows the color.

>What are these three digits?

That's the point of the name. 1 digit - R, 2 - G, 3 - B.

Each digit is a number from zero to 255. More/less is not given.

Of course, you can write 1000, or -7138, you are not held,
but the result will be the same - as 255, or 0.

If you need to choose a color, just type in **"rgb color picker"** in Google.

---
Okay, let's move on, les go!

And another important clarification, nothing will appear until you use engine.update(),
it refreshes the screen, so you can draw everything and then show it.

### engine.clear()
It simply removes everything you have drawn.
But you also will not see anything until you refresh the screen
### engine.update()
I have already told you about it, it essentially tells the screen about everything that happened,
like a class monitor complains to the teacher about what happened in the classroom.
### engine.is_key_pressed()
```python
engine.is_key_pressed("a")
```
See the letters you press to write?
This thing asks "Is the A button pressed?" and gets an answer.
By the way, you need to specify the button in brackets in quotation marks so that the computer understands who exactly needs to be checked.
### engine.is_mouse_button_pressed()
It's like that one, only with a mouse. There are 2 buttons and a wheel, right? Here.
1 is the left button. 3 is the right.
>And are there 2?

For many, I'll probably reveal a secret, but the wheel can not only be turned, but you can also press it!
It is number 2.
Example of using the function:
```python
engine.is_mouse_button_pressed(1)
```
### engine.get_mouse_pos()
This thing tells the game where the mouse is in pixels. Yes, yes, this arrow on the screen.
And they are also counted from the upper left corner.
### engine.play_sound():
This is already to play the sound again along the way. This is music, sound, etc.
Example:
```python
engine.play_sound("cool_music_2025.mp3")
```
---

And the last thing...
### engine.quit()
This is necessary for the game to close and end.

---

You, our dear friend, have read to the end. You are ready. Remember - you still have everything ahead of you, and you will succeed. Good luck, my friend.
