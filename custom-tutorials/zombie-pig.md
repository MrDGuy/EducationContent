### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1
### @diffs true

# Zombie Pig: Python

## Step 1
Code a ``||functions:function||`` and name it **setup**. 

```python
def setup():
    pass
```

## Step 2
Drag in an ```||gameplay:set difficulty||``` code to the inside of the **setup** function and change it to **NORMAL**
```python
def setup():
    gameplay.set_difficulty(NORMAL)
```

## Step 3
Drag in an ```||gameplay:change game mode||``` code to the inside of the **setup** function and change it to **SURVIVAL**
```python
def setup():
    gameplay.set_difficulty(NORMAL)
    gameplay.set_game_mode(SURVIVAL, mobs.target(LOCAL_PLAYER))
```

## Step 4
Drag in an ```||mobs:give||``` code to the inside of the **setup** function and change the target to **LOCAL_PLAYER** and the block type to **DIAMOND_SWORD**

```python
def setup():
    gameplay.set_difficulty(NORMAL)
    gameplay.set_game_mode(SURVIVAL, mobs.target(LOCAL_PLAYER))
    mobs.give(mobs.target(LOCAL_PLAYER), DIAMOND_SWORD, 1)
```

## Step 5
Code a new ``||functions:function||`` and name it **atmosphere**. 

```python
def setup():
    gameplay.set_difficulty(NORMAL)
    gameplay.set_game_mode(SURVIVAL, mobs.target(LOCAL_PLAYER))
    mobs.give(mobs.target(LOCAL_PLAYER), DIAMOND_SWORD, 1)

def atmosphere():
    pass
```

## Step 5
Drag in an ```||gameplay:time set||``` code to the inside of the **atmosphere** function and change it to **MIDNIGHT**

```python
def atmosphere():
    gameplay.time_set(DayTime.MIDNIGHT)
```

## Step 6
Drag in an ```||gameplay:weather||``` code to the inside of the **atmosphere** function and change it to **RAIN**

```python
def atmosphere():
    gameplay.time_set(DayTime.MIDNIGHT)
    gameplay.set_weather(RAIN)
```

## Step 7
Code a new ``||functions:function||`` and name it **zombiepig**. 

```python
def atmosphere():
    gameplay.time_set(DayTime.MIDNIGHT)
    gameplay.set_weather(RAIN)

def zombiepig():
    pass
```

## Step 8
Drag a ``||mobs:spawn||`` code and have it spawn a **PIG**. 

```python
def zombiepig():
    mobs.spawn(PIG, pos(0, 0, -5))
```

## Step 9
Drag a ``||mobs:spawn||`` code and have it spawn a **LIGHTNING_BOLT** at the same position **0, 0, -5**. 

```python
def zombiepig():
    mobs.spawn(PIG, pos(0, 0, -5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, -5))
```

## Step 10
Drag a ``||mobs:run code on killed||`` code and have it call the function **zombiepig**. 

```python
def zombiepig():
    mobs.spawn(PIG, pos(0, 0, -5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, -5))

def on_mob_killed():
    zombiepig()
mobs.on_mob_killed(CHICKEN, on_mob_killed)
```

## Step 10
Change the **CHICKEN** to **mobs.monster(PIG_ZOMBIE)**

```python
def zombiepig():
    mobs.spawn(PIG, pos(0, 0, -5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, -5))

def on_mob_killed():
    zombiepig()
mobs.on_mob_killed(mobs.monster(PIG_ZOMBIE), on_mob_killed)
```

## Step 11
Drag in a ``||player: run code on chat command||`` code at the bottom. 

```python
def zombiepig():
    mobs.spawn(PIG, pos(0, 0, -5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, -5))

def on_mob_killed():
    zombiepig()
mobs.on_mob_killed(mobs.monster(PIG_ZOMBIE), on_mob_killed)

def on_chat():
    pass
player.on_chat("jump", on_chat)
```

## Step 12
Change the **"jump"** to **"play"** and call each function inside the chat function. Press play then chat "play" in the game to fight the zombiepig.

```python
def on_chat():
    setup()
    atmosphere()
    zombiepig()
player.on_chat("jump", on_chat)
```

## Step 13
Code completed.

```python
def setup():
    gameplay.set_difficulty(NORMAL)
    gameplay.set_game_mode(SURVIVAL, mobs.target(LOCAL_PLAYER))
    mobs.give(mobs.target(LOCAL_PLAYER), DIAMOND_SWORD, 1)

def atmosphere():
    gameplay.time_set(DayTime.MIDNIGHT)
    gameplay.set_weather(RAIN)

def zombiepig():
    mobs.spawn(PIG, pos(0, 0, -5))
    mobs.spawn(LIGHTNING_BOLT, pos(0, 0, -5))

def on_mob_killed():
    zombiepig()
mobs.on_mob_killed(mobs.monster(PIG_ZOMBIE), on_mob_killed)

def on_chat():
    setup()
    atmosphere()
    zombiepig()
player.on_chat("jump", on_chat)
```
