### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Forest

```python
```

## Step 1
Агенту необходимо добыть палки для лестницы. Но нужно быть осторожным и не повредить гнезда птиц. Птицы в этом мире строят гнезда из камня, так что Агент легко сможет их отличить

## Step 2
Для начала создай функцию **is_nest**, которая будет проверять есть ли гнездо перед агентом и возвращать результат. 

## Step 3
Создай функцию **collect**, она должна разрушать блок перед Агентом, если перед ним листва **LEAVES_OAK**. И бросать палки вниз **agent.drop(DOWN, 1, 1)**

## Step 4
Для перехода в следующую координату потребуется еще одна функция **next**.
Выполни в ней следующий код: **mobs.spawn(mobs.monster(21), world(166, 153, 220))**

## Step 5
Настало время собирать палки. На сообщение в чате **run** проверяй, если перед агентом не гнездо, то собрать палки. Не забывай перемещаться на следующую позицию с помощью вызова функции **next**. Вызови код 5 раз. 


```ghost
```python
def collect():
    if agent.inspect(AgentInspection.BLOCK, FORWARD) == LEAVES_OAK:
        agent.destroy(FORWARD)
        agent.drop(DOWN, 1, 1)

def is_nest():
    return agent.inspect(AgentInspection.BLOCK, FORWARD) == STONE

def next():
    mobs.spawn(mobs.monster(21), world(166, 153, 220))


if (is_nest() == True):
    player.say("I found a nest!")
    next()
else:
    collect()
    next()
```

