### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false
### @hideDone false
### @flyoutOnly 1
### @explicitHints 1
### @diffs false
# Agent Maze: Blocks

## Step 1
Create an ``||player:on chat||`` command and name it **tp**.

```blocks
player.onChat("tp", function () {
})
```

## Step 2

Get an ``||agent:agent teleport to player||`` command and drag it inside the  ``||player:on chat||`` **tp** command.

**NOTE:** This command is essential to get your agent to join you at your position.

```blocks
player.onChat("tp", function () {  
     agent.teleportToPlayer()  
})  
```

## Step 3

Get another ``||player:on chat||`` command and name it **side1**.

```blocks
player.onChat("side1", function () {
})
```

## Step 4

Get an ``||agent:agent place on move||`` block and set it to **true**.  Place it inside ``||player:on chat||`` **side1** command.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
     
}) 
```

## Step 5

Get an ``||agent:agent set item||`` block and set the block type to **GRASS**, and the number of blocks to **64** in slot **1**.  Place it inside ``||player:on chat||`` **side1** command.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1)
     
}) 
```

## Step 6

Get an ``||agent:agent move forward||`` and set it to **4**.  Place it inside ``||player:on chat||`` **side1** command under the previous commands.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1)  
    agent.move(FORWARD, 4)  
})  
```

## Step 7

Add an ``||agent:agent turn||`` command and set it to **turn left**. Drag it into the ``||player:on chat||`` **side1** command.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1)
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
})  
```

## Step 8

Add another ``||agent:move forward||`` block and set it to **5**.  Place it inside ``||player:on chat||`` **side1** command under the previous commands.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1)
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)  
    })  
```

## Step 9

Add another ``||agent:agent turn||`` block and set it to **right**.  Place it inside ``||player:on chat||`` **side1** command under the previous commands.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1) 
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)
    agent.turn(RIGHT_TURN)    
    })  
```

## Step 10

Right-click on the existing ``||agent:agent move||`` **forward by 5** command and select **duplicate**. Drag the duplicate agent into the ``||player:on chat||`` **side1** command under the previous agent commands. 

**NOTE:** The duplicate function can save time when coding with blocks.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1) 
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)  
    agent.turn(RIGHT_TURN)  
    agent.move(FORWARD, 5)  
    })  
```

## Step 11

Duplicate the existing ``||agent:place on move||`` block, then drag the duplicate into the ``||player:on chat||`` **side1** command under the previous agent commands.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1)
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)  
    agent.turn(RIGHT_TURN)  
    agent.move(FORWARD, 5)  
    agent.setAssist(PLACE_ON_MOVE, false)  
    })  
```

## Step 12

Duplicate the existing ``||agent:agent turn||`` **left** command, then drag the duplicate into the ``||player:on chat||`` **side1** command under the previous agent commands.

## Step 13

Duplicate the existing ``||agent:agent move||`` **forward** command, then drag the duplicate into the ``||player:on chat||`` **side1** command under the previous agent commands.

## Step 14

Duplicate the existing ``||agent:agent turn||`` **left**, then drag the duplicate into the ``||player:on chat||`` **side1** command under the previous agent commands.

```blocks
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)
    agent.setItem(GRASS, 64, 1) 
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)  
    agent.turn(RIGHT_TURN)  
    agent.move(FORWARD, 5)  
    agent.setAssist(PLACE_ON_MOVE, false)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 2)  
    agent.turn(LEFT_TURN)  
})  
```

## Step 15

Press the **Play** button, return to Minecraft, type **tp**, and then type **side 1** into the chat line to see the agent build your first wall.

## Step 16

Duplicate the entire ``||player:on chat||`` **side1** command, then ename it **side2**.

## Step 17

Delete the last four commands from the new ``||player:on chat||`` **side2** command.

```blocks
player.onChat("side2", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)  
    })  
```

## Step 18

Set the first ``||agent:agent move||`` block to **forward by 7** and the last ``||agent:agent move||`` to **forward by 3**.

## Step 19

Change the last ``||agent:agent turn||`` command from **left** to **right**.

## Step 20

Return to Minecraft, type **tp**, then type **side2** into the chat line to see the agent build your second wall.

```blocks
player.onChat("tp", function () {  
    agent.teleportToPlayer()  
})  
player.onChat("side1", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)  
    agent.move(FORWARD, 4)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)  
    agent.turn(RIGHT_TURN)  
    agent.move(FORWARD, 5)  
    agent.setAssist(PLACE_ON_MOVE, false)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 2)  
    agent.turn(LEFT_TURN)  
})  
player.onChat("side2", function () {  
    agent.setAssist(PLACE_ON_MOVE, true)  
    agent.move(FORWARD, 7)  
    agent.turn(LEFT_TURN)  
    agent.move(FORWARD, 5)  
    agent.turn(RIGHT_TURN)  
    agent.move(FORWARD, 3)  
})  
```

