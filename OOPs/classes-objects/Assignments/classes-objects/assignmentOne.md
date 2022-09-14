### Guidelines:
The rules are quite simple. You have to clone this project -> copy paste the given snippet and complete the tasks listed below. 
***Note:***
Do not edit or make changes -> from line (20-23).

***Snippet:***

```py
class Store:
    def __init__(self, name):
        self.name = name
        self.items = []

    def addItems(self, name, price):
        pass

    def totalPrice():
        pass

storeOne = Store("Quintor")
storeOne.addItems("chocolate",20)
storeOne.addItems("cookies",40)
storeOne.addItems("milk",30)
```

#### Task 1:
In addItems() --> Create a dictionary inside addItems() with keys name and price, and append that to self.items list.

#### Task 2:
In totalPrice() --> Add together all item prices in self.items and return the total.

#### Task 3:
print out the total price.-> Your output should be 90.
