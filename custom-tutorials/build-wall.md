### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 0
### @diffs true

# Build Wall: Python

## Step 1
Make a function called build_walls(side) with a parameter called side.
1. Give the agent 64 STONE_BRICKS in slot 1
```python
def build_walls(side):
    agent.set_item(STONE_BRICKS, 64, 1)
```

## Step 2
Teleport the Agent to the player
```python
agent.teleport_to_player()
```

## Step 3
Move the Agent 1 up and 3 left

## Step 4
Using a for loop inside a for loop build 4 walls that are side length long

## Step 5
The outer for loop should loop 4 times.  
The loop inside should loop side times and the agent should place a block down and move forward.  
At the end of the inside loop have the agent turn left ONLY in the outside loop so the agent only turns left 4 times
```python
for i in range(4):
    for j in range(side):
        pass
```
## Step 6
Bring in a on Chat Command code and change it to have a parameter side_length and change the "jump" to "walls"
```python
def on_on_chat(length):
    build_walls(length)
player.on_chat("walls", on_on_chat)
```

```ghost
function build_walls(side: any) {
    agent.teleportToPlayer()
    agent.move(UP, 1)
    agent.move(LEFT, 3)
    agent.setItem(STONE_BRICKS, 64, 1)
    for (let index1 = 0; index1 < 4; index1++) {
        for (let index2 = 0; index2 < side; index2++) {
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(TurnDirection.Left)
    }
}

player.onChat("walls", function on_on_chat(side2: any) {
    build_walls(side2)
})
```
