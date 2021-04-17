### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Miners

```python
```

## Step 1
Помоги шахтеру добыть уголь. Используй команды в чате для управления.


```ghost
```python
def f(steps):
    agent.move(FORWARD, steps)

def b(steps):
    agent.move(BACK, steps)

def l(steps):
    agent.move(LEFT, steps)

def r(steps):
    agent.move(RIGHT, steps)

def u(steps):
    agent.move(UP, steps)

def d(steps):
    agent.move(DOWN, steps)

player.on_chat('f', f)
player.on_chat('d', d)
player.on_chat('u', u)
player.on_chat('b', b)
player.on_chat('l', l)
player.on_chat('r', r)
```

