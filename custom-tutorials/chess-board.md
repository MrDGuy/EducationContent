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
def chess_square():
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
def chess_square():
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
def chess_square():
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
def chess_square():
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
