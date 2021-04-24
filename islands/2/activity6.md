### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Iron

```python
```

## Step 1
Для проверки руды Вам понадобится функция **check**. Добавьте в нее следующий код. Постарайтесь его понять:
```python
def check():
    if agent.inspect(AgentInspection.BLOCK, FORWARD) == IRON_ORE:
        return 4
    else:
        data = agent.inspect(AgentInspection.DATA, FORWARD)
        if data == 0:
            return 3
        elif data == 15:
            return 2
        elif data == 11:
            return 1
    return 0
```

## Step 2
В обработчике сообщения, проверяйте чистоту руды. Если она меньше или равна 3, Агент должен разместить над собой блок из 2 слота. Иначе из первого. Выполните код 5 раз.

