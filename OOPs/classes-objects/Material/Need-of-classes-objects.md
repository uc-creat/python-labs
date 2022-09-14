## Why do we need classes: 

This is a very important question to ask yourself, before starting anything - Why do we need to have any sort of understanding of concepts like classes and objects. To answer this question, let us consider a situation. 

### Situation: 
I want to create a management system, which can help me to manage my employees. There are various attributes that I need to consider and accordingly manage them. Some of the important and common attributes for all type of employees are listed below: 

- Name
- Employee Id
- Working Domain

Then apart from this information, I also need some extra information - which is very specefic to the role in which that employee is working. For example: 

- Tech Lead: Employee working under this domain will have to submit a report of all the software developers working under him/her.
- SDE level 1: Level 1 SDE have to submit the daily task report + the list of his/her skill set.

Now considering the above situation, I am finding it very difficult to manage, because in my company I have many domains, and many levels of every role. 
Let us try to explore what all are the possiblities as a developer that we can think of -- for creating such type of system.

- #### Possiblity 1: 


          ```py

          def SdeLevelTwo(name, id, workingDomain, toDoReport, skillSet, project):
               pass       
          ```
       
    But the problem with such type of system is that -- 
       
    1. If I want to add more attributes - then my function will be full of parameters -- which is not a good coding practice.
    2. We know that for every employee there are some common attributes, but with this type of system, I need to pass those common attributes everytime for every role.
    3. Now consider, if there is some other role like SDE level 2 - which depends upon SDE level 1. Like, along with the skill set list and daily report they also have to submit the project they are in. So with this approach we will be creating another function like -- 

       ```py

       def SdeLevelTwo(name, id, workingDomain, toDoReport, skillSet, project):
           pass       
       ```
 
 
    Clearly, one thing we can get from the above case is that - if there are more dependencies our function will become a lot complicated.
    All the above three points - seems to make us think that - with this type of system, I might be able to group certain roles - but still my problem        of manageing various operations + these roles are not fully satisfied.

- #### Possibility 2:
    Second possiblity can be by creating a single function for eveything.

    ```py

    def companyName(name, id, workingDomain, *args):
        pass
    ```
    
    This way, we are just saying that, first three parameters are name, id, workingDomain, and other parameters depends upon the role. We can give n-number of parameters as per requirement.
    Again, this sort of approach gives a major issue of readability. 
    Now with this type of approach, I am not sure what parameters are required for SDE level 1 employee and SDE level 2 employee.

- #### Possibility 3:
    The third possiblity can be -- if somehow I can create a sort of container, which can store all the required fields for a role, and if somehow I can reuse that container for other roles which are dependent upon each other, then my manageing part might become a little easy. And for each role, if I can create a seperate container, then my readability will also become easy. 
    For eg:

    ```py

    containerSdeOne:
        fields: name, id, workingDomain, toDoReport, skillSet

    ```
    
    Different python file

    ```py

    containerSdeTwo contains containerSdeOne:
        fields: project

    ```

    In the above case I am trying to make a system, where containeSdeTwo contains all the attributes that containerSdeOne have.
    If you notice, this type of structure is actually helping us to overcome all the drawbacks that above two possibilities were having.


This type of structure can be achieved through classes and objects.

