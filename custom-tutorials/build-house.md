### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1
### @diffs true

# Custom House: Python

## Step 1
Make a ``||functions:function||`` and name it **base**. Give the function three parameters: **width3**, **height3**, **length3**, and **position3**.

```python
def base(width3, height3, length3, position3):
    pass
```

## Step 2
Drag a ``||blocks:fill with||`` code and change the **GRASS** to **STONE_BRICKS** and **FillOperation.REPLACE** to **FillOperation.HOLLOW**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        pos(0, 0, 0),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 3
Delete the first **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(pos(0,0,0), pos(0,0,0)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 4
Change the first **pos(0, 0, 0)** in the first **positions.add()** to **position3**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(0,0,0)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 5
Change the second **pos(0, 0, 0)** in the first **positions.add()** to **pos(width3 \* -1, -1, length3 \* -1)**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 6
Delete the second **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(pos(0,0,0), pos(0,0,0)),
        FillOperation.HOLLOW)
```

## Step 7
Change the first **pos(0, 0, 0)** in the second **positions.add()** to **position3**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(0,0,0)),
        FillOperation.HOLLOW)
```

## Step 8
Change the second **pos(0, 0, 0)** in the second **positions.add()** to **pos(width3, height3, length3)**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
```

## Step 9
Drag a ``||blocks:fill with||`` code and change the **GRASS** to **GLASS** and **FillOperation.REPLACE** to **FillOperation.HOLLOW**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        pos(0, 0, 0),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 10
Delete the first **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(pos(0,0,0), pos(0,0,0)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 11
Change the first **pos(0, 0, 0)** in the first **positions.add()** to **position3**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(0,0,0)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 12
Change the second **pos(0, 0, 0)** in the first **positions.add()** to **pos(width3 \* -1, 2, length3 \* -1 + 3)**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1 + 3)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 13
Delete the second **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(pos(0,0,0), pos(0,0,0)),
        FillOperation.HOLLOW)
```

## Step 14
Change the first **pos(0, 0, 0)** in the second **positions.add()** to **position3**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(0,0,0)),
        FillOperation.HOLLOW)
```

## Step 15
Change the second **pos(0, 0, 0)** in the second **positions.add()** to **pos(width3 * -1, 4, length3 - 3)**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
```

## Step 16
Copy the **blocks.fill(GLASS,...** and paste it beneath itself.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
```

## Step 17
Remove the **-1** from the **width3 * -1** code in both the position add.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
```

## Step 18
Drag a ``||blocks:fill with||`` code and change the **GRASS** to **AIR** and **FillOperation.REPLACE** to **FillOperation.HOLLOW**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        pos(0, 0, 0),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
    
```

## Step 19
Delete the first **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(pos(0,0,0), pos(0,0,0)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 20
Change the first **pos(0, 0, 0)** in the first **positions.add()** to **position3**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0,0,0)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 21
Change the second **pos(0, 0, 0)** in the first **positions.add()** to **pos(0, 0, length3)**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0, 0, length3)),
        pos(0, 0, 0),
        FillOperation.HOLLOW)
```

## Step 22
Delete the second **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0, 0, length3)),
        positions.add(pos(0, 0, 0),pos(0, 0, 0)),
        FillOperation.HOLLOW)
```

## Step 23
Change the first **pos(0, 0, 0)** in the second **positions.add()** to **position3**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0, 0, length3)),
        positions.add(position3,pos(0, 0, 0)),
        FillOperation.HOLLOW)
```

## Step 24
Change the second **pos(0, 0, 0)** in the second **positions.add()** to **pos(0, 1, length3)**

```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0, 0, length3)),
        positions.add(position3,pos(0, 1, length3)),
        FillOperation.HOLLOW)
```

## Step 25
Beneath the **base** function, Code a ``||functions:function||`` and name it **wood_roof** with four parameters **width2**, **height2**, **length2**, and **position2**.
```python
def wood_roof(width2, height2, length2, position2):
    pass
```

## Step 25
Drag in a ``||logic: if else||`` code and change the **True** to **width2 < length2**.
```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        pass
    else:
        pass
```

## Step 26
When **width2 < length2** is True set **loop_num = width2**. Otherwise set **loop_num = length2**.
```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
```

## Step 27
Drag in a ``||loops:for||`` loop and set the range = **loop_num**
```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        pass
```

## Step 28
Drag a ``||blocks:fill with||`` code to where the pass is and change the **GRASS** to **LOG_SPURE** and **FillOperation.REPLACE** to **FillOperation.HOLLOW**

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            pos(0, 0, 0),
            pos(0, 0, 0),
            FillOperation.HOLLOW)
    
```

## Step 29
Delete the first **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(pos(0,0,0), pos(0,0,0)),
            pos(0, 0, 0),
            FillOperation.HOLLOW)
    
```

## Step 30
Change the first **pos(0, 0, 0)** in the first **positions.add()** to **position2**

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(0,0,0)),
            pos(0, 0, 0),
            FillOperation.HOLLOW)
```

## Step 31
Change the second **pos(0, 0, 0)** in the first **positions.add()** to **pos(width2 \* -1 + i - 1, height2 + i, length2 \* -1 + i - 1)**

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(width2 * -1 + i -1, height2 + i, length2 * -1 + i - 1)),
            pos(0, 0, 0),
            FillOperation.HOLLOW)
```

## Step 32
Delete the second **pos(0,0,0)** code and then drag a ``||positions:p1+p2||`` code and in its place.

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(width2 * -1 + i - 1, height2 + i, length2 * -1 + i - 1)),                     positions.add(pos(0, 0, 0), pos(0, 0, 0)),
            FillOperation.HOLLOW)
```

## Step 33
Change the first **pos(0, 0, 0)** in the second **positions.add()** to **position2**

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(width2 * -1 + i - 1, height2 + i, length2 * -1 + i - 1)),                     positions.add(position2, pos(0, 0, 0)),
            FillOperation.HOLLOW)
```

## Step 34
Change the second **pos(0, 0, 0)** in the second **positions.add()** to **pos(width2 - i + 1, height2 + i, length2 - i + 1)**

```python
def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(width2 * -1 + i - 1, height2 + i, length2 * -1 + i - 1)),                     positions.add(position2, pos(width2 - i + 1, height2 + i, length2 - i + 1)),                               FillOperation.HOLLOW)
```

## Step 35
Drag in a ``||player: run code on chat||`` block beneath both the base and wood_roof functions.
```python
def on_chat():
    pass
player.on_chat("jump", on_chat)
```

## Step 36
Change the **"jump"** to **"house"** and add three parameters **width**, **height**, and **length**
```python
def on_chat(width, height, length):
    pass
player.on_chat("house", on_chat)
```

## Step 37
Call the base function with the width, height and length parameters and then include a ``||player:player world position||`` as the fourth parameter.
```python
def on_chat(width, height, length):
    base(width, height, length, player.position())
player.on_chat("house", on_chat)
```

## Step 38
Call the wood-roof function with the width, height and length parameters and then include a ``||player:player world position||`` as the fourth parameter.
```python
def on_chat(width, height, length):
    base(width, height, length, player.position())
    wood_roof(width, heigth, length, player.position())
player.on_chat("house", on_chat)
```

## Step Last
Final Complete Code:
```python
def base(width3, height3, length3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0, 0, length3)),
        positions.add(position3,pos(0, 1, length3)),
        FillOperation.HOLLOW)

def wood_roof(width2, height2, length2, position2):
    if width2 < length2:
        loop_num = width2
    else:
        loop_num = length2
    for i in range(loop_num):
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(width2 * -1 + i - 1, height2 + i, length2 * -1 + i - 1)),                     positions.add(position2, pos(width2 - i + 1, height2 + i, length2 - i + 1)),                               FillOperation.HOLLOW)

def on_chat(width, height, length):
    base(width, height, length, player.position())
    wood_roof(width, height, length, player.position())
player.on_chat("house", on_chat)
```

```ghost
function base(width3: number, height3: number, length3: number, position3: any) {
    blocks.fill(STONE_BRICKS, positions.add(position3, pos(width3 * -1, -1, length3 * -1)), positions.add(position3, pos(width3, height3, length3)), FillOperation.Hollow)
    blocks.fill(GLASS, positions.add(position3, pos(width3 * -1, 2, length3 * -1 + 3)), positions.add(position3, pos(width3 * -1, 4, length3 - 3)), FillOperation.Hollow)
    blocks.fill(GLASS, positions.add(position3, pos(width3, 2, length3 * -1 + 3)), positions.add(position3, pos(width3, 4, length3 - 3)), FillOperation.Hollow)
    blocks.fill(AIR, positions.add(position3, pos(0, 0, length3)), positions.add(position3, pos(0, 1, length3)), FillOperation.Hollow)
}

function wood_roof(width2: number, height2: number, length2: number, position2: any) {
    let loop_num: number;
    if (width2 < length2) {
        loop_num = width2
    } else {
        loop_num = length2
    }
    
    for (let i = 0; i < loop_num; i++) {
        blocks.fill(LOG_SPRUCE, positions.add(position2, pos(width2 * -1 + i - 1, height2 + i, length2 * -1 + i - 1)), positions.add(position2, pos(width2 - i + 1, height2 + i, length2 - i + 1)), FillOperation.Hollow)
    }
}

player.onChat("house", function on_chat(width: number, height: number, length: number) {
    base(width, height, length, player.position())
    wood_roof(width, height, length, player.position())
})
```

