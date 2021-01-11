>>>Here is the pseudoCode for linked list , it is for singly linked list . 


1. Create a Class For A Node . Initialise the Properties which are   needed in a Node . (item and next):

```
class Node:
  def__init__(self,item,next=None)
    slef.item = item
    self.next = next 
    
```
2. Create a Class For your linked list which will have an initialised First Node as None and other needed methods.
```
class LinkedList:
  def__init__(self):
    self.firstNode = None
```

3. Now create those method which you have the need (inserting , deleting , displaying) in side the linked list class .
- Inserting at starting:
    Create a New Node .Then check if there is already a node in your list
    then link your new node to first node and then assign first node into new node .
    And if there is no nodes then assign first node as new node .
    
    ```
    def insertAtbegning(self,item):
      newNode = Nose(item)
      if self.firstNode != None :
        newNode.next = self.firstNode
        self.firstNode = newNode
      else:
        self.firstNode = newNode
    ```
- Inserting at end :
    Create a new node and if there
    is already nodes in linked list then travel through the nodes .
    
    ```
    def insertAtEnd(self,item):
      newNode = Node(item)
      if self.firstNode != None:
        current = self.firstNode
        while current.item !=None:
          current = current.item
        current.item = newNode
      else:
        self.firstNode = newNode
    ```

4. Create a method which can display all the nodes of your linked list . 
And check if list is empty then return it and if it present then travel 
the list and display them 
  ```
  def display(self):
    if self.firstNode == None:
      peint("List is Empty")
      return
   current = self.firstNode
   while current.next !=None:
    print(current.item)
    current = current.next
    
  ```
  
 5. Create a method which can delete the element by its value , 
 and check if the list is empty then return it and if its not empty then check for the first element that , 
 is it the target ? if ys then return . And if first node is not the target then travel the list and find .
 
  ```
  def delete(self,item):
    if self.firstNode == None:
      print("list is empty")
      return
    if self.firstNode == item:
      temp= self.firstNode
      self.firstNode = temp.next
      temp = None 
      return
    current = self.firstNode
      while current.next !=None:
        if current.next.item== item:
          temp = current.next
          current.next=temp.next
          temp=None
          return
        current = current.next
     print("Elementis not found")
      
  
  
