### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ladders

```python
```

## Step 1
Помоги Маркусу починить лестницу. Запасные части уже в инвентаре Агента.
Поднимайся вверх, пока видишь перед собой препятствие. Добавьте переменную в которой будете считать уровень над землей. Установите лестницу на 0м и 3м уровне.

```ghost
```python
agent.move(FORWARD, 1)
level = 0
while agent.detect(AgentDetection.BLOCK, FORWARD):
    if level == 0 or level == 3:
        agent.place(FORWARD)
    agent.move(UP, 1)
    level += 1
```

