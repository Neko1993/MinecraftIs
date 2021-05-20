### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Book

```python
```

## Step 1
Каждая книга в библиотеке имеет свой номер. Что бы его проверить необходимо использовать команду **agent.inspect(AgentInspection.DATA, FORWARD)**. Тебе нужно найти книгу с номером 9 и отметить ее поставив блок позади себя. 

Материалы уже выданы Агенту.

```ghost
```python
def  check_book():
    if agent.inspect(AgentInspection.DATA, FORWARD) == 9:
        return True
    else:
        return False

def mark_book():
    agent.place(BACK)

def check_shelf():
    for i in range(5):
        if check_book():
            mark_book()
        agent.move(UP, 1)

player.on_chat("check", check_shelf)

```

