### Practical Use:

So, now let us extend our idea, of how can we achieve our possiblity 3, through classes and objects.

- What are classes:
Classes is similar to what we assumed to be a container. It is our container - which contains all the fields that we want. The power of this container just does not finish here. There is a lot of powers - which we will discover as move forward in exploring classes.
- What are objects:
If classes are containers of attributes, so objects are those entities whose attributes are being stored in those classes. So, basically, classes are acting like blueprints of objects. I can make use of a single class and call multiple objects with different names. 

Let us take the similar example and try to form that system.

In python we make use of "class" keyword for defining a class.

```py
class TechLead:
    # remeber to name the class with capital letters -- convention

    def __init__(self, name, employeeId, workingDomain, employeeReport):
        self.name = name
        self.employeeId = employeeId
        self.workingDomain = workingDomain
        self.employeeReport = employeeReport

akarsh = TechLead("Akarsh", 1, "Technology", ["utkarsh.pdf","sethu.pdf"])
sid = TechLead("Sid", 2, "Technology", ["deepika.pdf","arun.pdf"])
```

Now there are a lot of things to note.
First, we made a class which is storing information related to the role tech-lead. After defining the class, we are creating a method as ***def __init__ (self)*** method. 

- #### init method:
  This method basically means -- what are the parameters that you want to pass to your container whenever you initiliaze this class. So, whenever you will be calling this class, this method will run for that ***instance*** . If you don't create this method, then you are basically trying to say that - inside your class, you don't need any field which depends upon that particular ***instance***.

  - **What is an instance:**
      An instance is an object that belongs to a class. For eg: 
      In the above python code -> akarsh and sid are two different objects/instances of the class TechLead().
      Why do we call them as an instance - because the values that we are passing --> for each object is different and depends upon that particular instance/object. Like, name parameter for "akarsh" - object/instance is "akarsh" -- whereas for the similar name-parameter - "sid" have the value as "Sid". 
      So, when "***akarsh = TechLead(Akarsh, 1, Technology, ["utkarsh.pdf","sethu.pdf"])***" this line will be called, then we are basically saying that --> create an instace/object which have these "Akarsh, 1, Technology, ["utkarsh.pdf","sethu.pdf"]" values.
      Similarly, create another instance/object which have these "Sid, 2, Technology, ["deepika.pdf","arun.pdf"]" values.

  - **What is self:**
      Many people assumes that self is a keyword in python. Which is wrong. **self** is not a keyword.
      One thing to note is that, sometimes we don't need values which are instance-values. Sometimes we need values which remain the same for everytime. For eg: 

      ```py
      class TechLead:
        def __init__(self, name, employeeId, workingDomain, employeeReport):
            self.name = name
            self.employeeId = employeeId
            self.workingDomain = workingDomain
            self.employeeReport = employeeReport

        def salary(self):
            sal = "$ 21000 "
            return sal
      ```

      For the above case, I don't want to change this salary value, because salary for any tech lead in this company remains the same. So, my salary is not an instance variable.
      So, how should I differentiate between instance and non-instance variable is through ***self***.
      We can use any other name apart from self, but just keep in mind, that whatever name you are passing as the first parameter of __init__ method -- that will act as self.
      By convention pythoneers follow - self -- to inform python that those variables are instance variables.
      The reason of passing self in salary function is that -- by default -> whenever you call a function of class - it takes the first argument as self. If you have noticed, whenever I am creating an instance for a class, I am not passing any placeholder for self - this because, python by default understands and takes 1st parameter as self only.

The beauty of the above way is that - I am not re-defining anything again and again for two different employees. I am just calling the class and passing some values for that instance.

Now the question is, if I want to play around with any value - be it an instance variable or a non-instance variable - how can I access them within a class. Let's explore that - 

#### Situation:
The situation is very simple. Only the person with id=1, can have the access to do something. So, how can I make use of that id-> which I'll pass as a parameter to the class, in some other method - "grantAccess".

```py
def something:
    pass
```

You can clearly see, that instance values changes over different instances, while non-instance value like sal, does not change for different instances.


#### NOTE: 
Once you finish reading this, and you are clear with the concepts - then move to Assignment folder and complete the first assignment.
