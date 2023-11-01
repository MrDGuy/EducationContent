### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 0
### @diffs true

# Build Wall: Python

## Step 1
In this code you will get width, length, and height from the user to make a tree 
with a trunk 7 blocks high and the leaves will be 2*width, 2* length, height large.

## Step 2
Write a build_trunk(trunk_height, position) function that accepts the trunk_height and position as parameters.
```python
def build_trunk(trunk_height, position):
    pass
```
## Step 3
Fill blocks that are LOG_OAK starting 3 away from the player and go up the trunk_height. FillOperation.REPLACE
```python
blocks.fill(GRASS, pos(0, 0, 0), pos(0, 0, 0), FillOperation.REPLACE)
```

## Step 4
Write a build_leaves(width, height, length, position, trunk_height2) function that 
accepts width, height, length, position, and trunk_height2 as parameters.
```python
def build_leaves(width, height, length, position, trunk_height2):
  pass
```

## Step 5
Fill the blocks with LEAVES_OAK that start at the player position, 
3 away atop the trunk in the negative width and length directions

## Step 6
The blocks should end at the positive width and length directions 
and in the air height + trunk_height2.  FillOperation.REPLACE

## Step 6
In the on_chat have three parameters width2, length2, and height2 so the user can write in the values for these in the chat.  
Run the build_trunk and build_leaves functions giving 7 as the trunk_height.
```python
def on_on_chat(width, height, length):
    build_leaves(width, height, length, player.position(), 7)
    build_trunk(trunk_height, player.position())
player.on_chat("tree", on_on_chat)
```

```ghost
let trunk_height = 7
function build_trunk(trunk_height: number, position: any) {
    blocks.fill(LOG_OAK, positions.add(position, pos(3, -1, 0)), positions.add(position, pos(3, trunk_height - 1, 0)), FillOperation.Replace)
}

function build_leaves(width: number, height: number, length: number, position: any, trunk_height2: number) {
    blocks.fill(LEAVES_OAK, positions.add(position, pos(3 + width * -1, trunk_height, length * -1)), positions.add(position, pos(3 + width, height + trunk_height, length)), FillOperation.Replace)
}

player.onChat("run", function on_on_chat(width: number, height: number, length: number) {
    build_leaves(width, height, length, player.position(), trunk_height)
    build_trunk(trunk_height, player.position())
})

```
