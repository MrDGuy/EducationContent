### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false
### @flyoutOnly 1
### @explicitHints 1
### @diffs true

# Chess Board: Python

## Step 1
Code a ``||functions:function||`` and name it **chess_square**. 

```python
def chess_square():
    pass
```

## Step 2
Within the **chess_square** function parameters add: **width**, **location** and **is_black**.
```python
def chess_square(width, location, is_black):
    pass
```

## Step 3
Drag in an ```||logic:if else||``` code to the inside of the **chess_square** function.
```python
def chess_square(width, location, is_black):
    if True:
        pass
    else:
        pass
```

## Step 4
Change the **True** to **is_black**
```python
def chess_square(width, location, is_black):
    if is_black:
        pass
    else:
        pass
```

## Step 5
Within the **chess_square** function inside the **if is_black**, drag a ``||blocks:fill||`` code that has a **BLACK_CONCRETE** block type, **location** as the starting position, 

```python
def chess_square(width, location, is_black):
    if is_black:
        blocks.fill(BLACK_CONCRETE,
            location, 
            pos(0,0,0), 
            FillOperation.REPLACE)
    else:
        pass
```

## Step 6
Drag a ``||positions:p1+p2||`` block to replace the ending position.

```python
def chess_square(width, location, is_black):
    if is_black:
        blocks.fill(BLACK_CONCRETE,
            location, 
            positions.add(pos(0, 0, 0), pos(0, 0, 0)), 
            FillOperation.REPLACE)
    else:
        pass
```

## Step 7
Change the first **pos(0, 0, 0)** to **location** and the second **pos(0, 0, 0)** to **pos(width - 1, 0, width - 1)**

```python
def chess_square(width, location, is_black):
    if is_black:
        blocks.fill(BLACK_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)
    else:
        pass
```

## Step 8
Copy the entire code inside the **if is_black** code and paste it inside the **else** code.  Change the **BLACK_CONCRETE** to **WHITE_CONCRETE** in the else.

```python
def chess_square(width, location, is_black):
    if is_black:
        blocks.fill(BLACK_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)
    else:
        blocks.fill(WHITE_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)
```

## Step 9
Underneath the **chess_square** function. Code a ``||functions:function||`` and name it **draw_row**.  Add three parameters **num**, **position**, **first_is_black**, and **row_num**.

```python
def chess_square(width, location, is_black):
    if is_black:
        blocks.fill(BLACK_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)
    else:
        blocks.fill(WHITE_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)

def draw_row(num, position, first_is_black, row_num):
    pass
```

## Step 10
Drag in a ``||loops: for||`` loop code and make it repeat **8** times.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        pass
```

## Step 11
Make a variable called **curr_pos** and set it equal to a ``||positions:p1+p2||`` code.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(pos(0, 0, 0), pos(0, 0, 0))
```

## Step 12
Change the parameters of the **positions.add** to start at **position** and add **pos((num + 0) * i, 0, (num + 0) * row_num)**.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
```

## Step 13
Include an ``||logic:if else||`` beneath the **cur_pos** code.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
        if True:
            pass
        else:
            pass
        
```

## Step 14
Change the **True** in the if statement to **i % 2 == 0**.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
        if i % 2 == 0:
            pass
        else:
            pass
        
```

## Step 15
For the **if i % 2 == 0** include a **chess_square(num, curr_pos, first_is_black)** call.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
        if i % 2 == 0:
            chess_square(num, curr_pos, first_is_black)
        else:
            pass
    
```

## Step 16
For the **else** include a **chess_square(num, curr_pos, not first_is_black)** call.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
        if i % 2 == 0:
            chess_square(num, curr_pos, first_is_black)
        else:
            chess_square(num, curr_pos, not first_is_black)
    
```

## Step 17
Beneath the **draw_row** function drag in the ``||player: run code on chat command||`` code and change **"jump"** to **"board"**.

```python
def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
        if i % 2 == 0:
            chess_square(num, curr_pos, first_is_black)
        else:
            chess_square(num, curr_pos, not first_is_black)

def on_on_chat():
    pass
player.on_chat("board", on_on_chat)
```

## Step 19
Include a parameters **num1** in the chat command function.

```python
def on_on_chat(num1):
    start_pos = player.position()
player.on_chat("board", on_on_chat)
```

## Step 18
Replace the **pass** with a variable called **start_pos** and set it equal to a ``||player:player world position||`` code.

```python
def on_on_chat(num1):
    start_pos = player.position()
player.on_chat("board", on_on_chat)
```

## Step 19
Drag in a ``||loops:for||`` loop code and replace the **i** with **j** and have it repeat **8** times.

```python
def on_on_chat(num1):
    start_pos = player.position()
    for j in range(8):
        pass
player.on_chat("board", on_on_chat)
```

## Step 20
Drag in a ``||logic:if else||`` code and replace the **True** with **j % 2 == 0**.

```python
def on_on_chat(num1):
    start_pos = player.position()
    for j in range(8):
        if j % 2 == 0:
            pass
        else:
            pass
player.on_chat("board", on_on_chat)
```

## Step 21
Inside the **if j % 2 == 0:** include a call to the **draw_row** function with the parameters **num1**, **start_pos**, **True**, and **j**.

```python
def on_on_chat(num1):
    start_pos = player.position()
    for j in range(8):
        if j % 2 == 0:
            draw_row(num1, start_pos, True, j)
        else:
            pass
player.on_chat("board", on_on_chat)
```

## Step 22
Inside the **else** include a call to the **draw_row** function with the parameters **num1**, **start_pos**, **False**, and **j**.

```python
def on_on_chat(num1):
    start_pos = player.position()
    for j in range(8):
        if j % 2 == 0:
            draw_row(num1, start_pos, True, j)
        else:
            draw_row(num1, start_pos, False, j)
player.on_chat("board", on_on_chat)
```

## Step 23
Complete Code:

```python
def chess_square(width, location, is_black):
    if is_black:
        blocks.fill(BLACK_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)
    else:
        blocks.fill(WHITE_CONCRETE,
            location, 
            positions.add(location, pos(width - 1 , 0, width - 1)), 
            FillOperation.REPLACE)

def draw_row(num, position, first_is_black, row_num):
    for i in range(8):
        curr_pos = positions.add(position, pos((num + 0) * i, 0, (num + 0) * row_num))
        if i % 2 == 0:
            chess_square(num, curr_pos, first_is_black)
        else:
            chess_square(num, curr_pos, not first_is_black)

def on_on_chat(num1):
    start_pos = player.position()
    for j in range(8):
        if j % 2 == 0:
            draw_row(num1, start_pos, True, j)
        else:
            draw_row(num1, start_pos, False, j)
player.on_chat("board", on_on_chat)
```
