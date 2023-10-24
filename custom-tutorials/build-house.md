### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1
### @diffs true

# Chess Board: Python

## Step 1
Code a ``||functions:function||`` and name it **base**. 

```python
def prismStone(width3, length3, height3, position3):
    blocks.fill(STONE_BRICKS,
        positions.add(position3, pos(width3 * -1, -1, length3 * -1)),
        positions.add(position3, pos(width3, height3, length3)), 
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3 * -1, 2, length3 * -1 + 3)),
        positions.add(position3, pos(width3 * -1, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(GLASS,
        positions.add(position3, pos(width3, 2, length3 * -1 + 3)),
        positions.add(position3, pos(width3, 4, length3 - 3)),
        FillOperation.HOLLOW)
    blocks.fill(AIR,
        positions.add(position3, pos(0, 0, length3)),
        positions.add(position3, pos(0, 1, length3)),
        FillOperation.REPLACE)
```

## Step 2
Beneath the **base** function, Code a ``||functions:function||`` and name it **wood_roof**. 
```python
def wood_roof(width2, length2, height2, position2):
    loopNum = 0
    if width2 < length2:
        loopNum = width2
    else:
        loopNum = length2
    index = 0
    while index <= loopNum:
        blocks.fill(LOG_SPRUCE,
            positions.add(position2, pos(width2 * -1 + index - 1, height2 + index, length2 * -1 + index -1)),
            positions.add(position2, pos(width2 - index + 1, height2 + index, length2 - index + 1)),
            FillOperation.HOLLOW)
        index += 1
```

## Step 3
Beneath the **wood_roof** function, Code a ``||player:run code on chat command||`` and make the chat: "house". 
```python
def on_on_chat(width, length, height):
    base(width, length, height, player.position())
    wood_roof(width, length, height, player.position())
player.on_chat("house", on_on_chat)
```
