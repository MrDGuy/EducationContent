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
Code a new ``||functions:function||`` and name it **zombiepig**. 

```python
def atmosphere():
    gameplay.time_set(DayTime.MIDNIGHT)
    gameplay.set_weather(RAIN)

def zombiepig():
    pass
```
