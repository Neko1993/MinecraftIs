### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Forest

```python
```

## Step 1
Напиши код для того, чтобы срубить дерево. Постарайся использовать отдельные функции для рубки всего дерева и отдельного уровня.

```ghost
```python
def remove_level():
    agent.destroy(FORWARD)
    agent.move(RIGHT, 1)
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.move(LEFT, 1)
    agent.destroy(FORWARD)
    agent.move(BACK, 1)

def remove(height):
    for i in range(height):
        remove_level()
        agent.move(UP, 1)
remove(13)
```

