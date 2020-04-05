# JavaScript ES6+ Feature Classes

 The ES6 simplified how we can create native classes using the keyword `class` followed by the *class name*. Classes can be included in the code either **by declaring them** or **by using class expressions**.

 ## Syntax: declaring a class
 ```javacript
class Class_Name {
    //definition
}
 ```

 ## Syntax: class expressions
```javacript
var var_name = new Class_name {
    //definition
}
```

A `class` body and method definition support prototype-based inheritance, constructors, super calls, instance, and static methods.

* **Constructor:** it is responsible for allocating memory for the objects of this `class`.
    * This is usually the first method to be called
    * It can create actions that will trigger object creation
    * It can initiate variables
    * It can use the `super()` keyword to call the constructor of the superclass ("parent class")
* **Methods:** it represents actions that an object can take.
 
Example: Simulate the logistics of a simple to-do list using a class to hold the list array and a subclass for a specific user.

STEPS:
    1. Create the class **TodoList**
    2. Add the constructor method and initiate **todos** variable as an empty array
    3. Add a method to add tasks and push a new task to the list
    4. Create a button in the **index.html** holding the id='newtodo'
    5. Instantiate the class by assigning a new list to a variable
    6. Add an **onclick** parameter to the button created
    7. Add the subclass **List** for user Diego

```javascript
class List {
    constructor() {
        this.data = [];
    }

    add(data) {
        this.data.push(data);
        console.log(this.data);
    }
}

class TodoList extends List {
    constructor() {
        super();
        this.user = 'Diego';
    }

    showUser() {
        console.log(this.user);
    }
}

const MyList = new TodoList();

document.getElementById('newtodo').onclick = function () {
    MyList.add('New Task')
}

MyList.showUser();
```

See the [ES6+ Feature Class
documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
on MDN for more details.