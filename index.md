# Titanic Survivors 
The Titanic dataset has sparked numerous questions, inviting me to unravel its layers of information. Beyond survival rates and demographics, I'm intrigued by the untold stories and hidden patterns within the data. It's a captivating journey, unveiling the human dynamics aboard the historic vessel.  

---

# What is the percentage of those that survived?

The first ste
```python 
todolist=["get money", "save money", "rejoice"]
``` 
This became the current list and users will be able to see this list  

Next step 
```python 
while True:
    addtodos = input("Would you like to add a todo or remove a todo") 
    if addtodos == ("add"): 

        add= input("what is the new todo") 

        todolist.append(add) 

    elif addtodos == ('remove'): 
        remove= input("what in the todo list, would you like to remove") 
        if remove in todolist:  
            todolist.remove(remove)

        else: 
            print("This isn't in the list")  
    else: 
        print("The input is incorrect")    
``` 
I first made a loop that will continue to repeat until the condition is met.

In addition I also made inputs to make users able to add todos to the list. Then I created the 'addtodo' variable which will allow you to add or remove a todo.

 I also used "append" which will allow users to add a todo at the very end of the list. I also added remove, so that if they type remove, they are able to delete something from the list. Then I added "todolist.remove", this function will officially remove what they want to remove from the list. Added an else statement, so that if what they put isn't in this list, it would print "this isn't in the list" or "the input is incorrect".  

```python 
 print("-----------------------------------------------") 

    print("your current todos are:"+str(todolist)) 
```
I added the big line just to create seperation and the next print is just to show your current todo list with all the todos you added or removed. 

# Obstacles  

Finding the correct loop was slightly challenging because I tend to always mix up for loops and while loops 

In addition, another obstacle I faced was time.

Just figuring out the exact code to use to build this was challenging to do.
