### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Farm

```python
```

## Step 1
Part3
Напиши функцию **check**, которая возвращает True, если под Агентом блок **WHEAT**, иначе возвращает False

## Step 2
Напиши функции **wheat**  и **carrot** для уставновки отметок над Агентом, где какие семена посажены. Агенту уже выданы блоки, они расположены в 1 и 2 слотах. Для переключения между слотами используйте **agent.set_slot()**, где в качестве аргумента укажите номер слота. Для **wheat** используйте флаг с первого слота, для **carrot** со второго. 

## Step 3
Проверьте 4 точки и установите флаги в соответсвии с результатами проверки. Используйте цикл.

```ghost
```python
def check():
    return agent.inspect(AgentInspection.BLOCK, DOWN) == WHEAT

def wheat():
    agent.set_slot(1)
    agent.place(UP)

def carrot():
    agent.set_slot(2)
    agent.place(UP)

for i in range(4):
    agent.move(FORWARD, 3)
    if check():
        accept()
    else:
        deny()
```

