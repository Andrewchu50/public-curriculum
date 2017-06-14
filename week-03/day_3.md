Day 3
====================
Videos
------
* [Video 1](https://vimeo.com/221603629)
* [Video 2]()

Code Style
---------------
* Coding style is very important to make things clean and to adhere to a set of universal standards. This makes code universally easier to read, reviewing code more efficient, and ensures that your code can be implemented/understood by a new developer.
* [Rubocop](https://github.com/bbatsov/rubocop)
* [Ruby Style Guide](https://github.com/styleguide/ruby)
* [AirBnB's Style Guide for Ruby](http://airbnb.io/projects/ruby/)

Inheritance
----------------
* [Video](https://vimeo.com/204196259)
* Inheritance is a relationship between two classes. Think of your relationship with your parents. All your features are inherited from them - your race, eye color, hair color, height, weight to some extent. But you are also very different from them. You have new features. You can do different things from them. After this course is over, I guarantee you that whenever they have issues with tech, they will come to you for help.
* Similarly in coding, let's say we have two classes - a parent and child class. A child class has the ability to inherit all the features of a parent class and any number of methods from the parent class can be overriden in the child class.
* A good way to think about this is `is-a`. Think of a parent class called Dog for example. There are many types of dogs, right? What are some examples of dogs?
	* A golden retriever `is-a` dog. A golden retriever in code would inherit from its parent class, Dog.
* What do we get when we inherit things? We get all the methods available to the parent class.
* We can override the parent class methods by defining our own in the child class
* To keep code DRY, we may want to use the behavior of the parent class but do something extra before or after. In that case, we use the `super` method.

Practice
-------------
* Read up on Polymorphism and Encapsulation
	* [Resource 1](https://devblast.com/b/ruby-inheritance-encapsulation-polymorphism)
	* [Resource 2](https://robots.thoughtbot.com/back-to-basics-polymorphism-and-ruby)
* [More Reading #1](http://practicingruby.com/articles/solid-design-principles)
* [More Reading #2](https://chesterli0130.wordpress.com/2012/10/04/four-major-principles-of-object-oriented-programming-oop/)
