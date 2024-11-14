### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 0
### @hideDone false

# Bamboo Hideaway

## Step 1
Program the Agent to plant **3** blocks of bamboo on each side of the sand patch. Add an ``||agent: agent turn||``command to make sure the Agent can complete the activity. 

#### ~ tutorialhint
There should be 2 **repeat** loops, one nested inside the other.

```blocks
player.onChat("bamboo", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```
 
```ghost
player.onChat("bamboo", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```


