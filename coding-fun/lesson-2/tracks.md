### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1
### @hideDone false

# Program the Agent to move along the turtle tracks!

## Step 1
Move the Agent along the turtle tracks by using an ``||agent: agent move forward||`` block to the gates. When done, press the **Play** button to compile the code. Don't forget to run your code in Minecraft. 

```blocks
player.onChat("tracks", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
``` 
