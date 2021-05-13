### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Iron ores in tunels

```python
```

## Step 1
Напиши код, который будет проверять, есть ли золотая руда **GOLD_ORE** на глубине 3х блоков в отмеченных позициях. Не забудь выкопать и спуститься в шахту, чтобы проверить.


```ghost
```python
def check():
    for i in range(3):
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
    
    if agent.inspect(AgentInspection.BLOCK, DOWN) == GOLD_ORE:
        agent.destroy(DOWN)
    
    agent.move(UP, 3)

def get_gold():
    agent.move(FORWARD, 1)
    for i in range(3):
        check()
        agent.move(FORWARD, 2)

get_gold()


```

