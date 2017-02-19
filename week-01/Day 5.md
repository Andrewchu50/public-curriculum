Day 5
====================
Ruby Fundamentals
----------------------
* Control flow, if/else statements, and loops all work fundamentally the exact same way as they do in Javascript but look a little different
* JS:
```javascript
var lexiWants = 'pizza';
if(lexiWants === 'pizza') {
	console.log('Let us go get pizza');
}
else if(lexiWants === 'salad') {
	console.log('Are you sure?');
}
else {
	console.log('So what would you like?');
}
```
* In Ruby it looks like this:
```ruby
lexi_wants = 'pizza'
if lexi_wants == 'pizza'
	puts 'Let us go get pizza'
elsif lexi_wants == 'salad'
	puts 'Are you sure?'
else
	puts 'So what would you like?'
end
```
* [Slides 40-43](/week-01/intro_to_rails_final.pdf)

Method arguments / Defaults
---------------------------------
* Arguments == Parameters
* You can either pass in arguments to a method or assign defaults
```
function sumOfNumbers(num1, num2 = 0) {
  console.log(num1 + num2);
}
sumOfNumbers(3) // 3


function sayHello(name = ‘to you’) {
	console.log(‘Hello ‘ + name);
}

sayHello() // 'Hello to you'

```

* Method Chaining
	* Most often found in OOP, this is where you invoke multiple methods at once
	* Each method returns an output, which the next chained method is called on
	```
	['a', 'b', 'c'].shuffle.pop.upcase
	```


Individual or Pair Practice
--------------------------------
* [Credit Check](https://github.com/CodePlatoon/credit-check) in JS/Ruby


Classes in Ruby
--------------------
* [Class Video](https://vimeo.com/203349418)
* Ruby is an object-oriented language and everything is an object
	* Everything means everything - booleans, strings, Hashes, arrays, integers, everything
* Classes are used to combine how data is represented and methods to manipulate data.
* Example:
	* We already know things like `Array.new` and `Hash.new`
	* The `Array` and `Hash` classes have built-in methods. An example is `push`
		```
		a = Array.new
		a.push(1)
		a # [1]

		# The source code may look like this:
		class Array
			def push
				# code for push goes here
			end
		end
		```
* Basically, Ruby classes are a way to reuse and organize code.
* A class is basically a noun. Every noun has attributes and things it can do.
* Let's create a class together to get an idea of how it works.
	```
	class Cat
		def initialize(color)
			@color = color
			# The initialize method (called a constructor) is to create a new cat. The parameters passed in are traits of the cat, things that you know you'll use later in your code - something that every cat will have. You don't need to initialize with any trait if you don't want to. Let's say for now that every single cat has a color.
		end
	end
	```
	* You may be wondering why there is an `@` sign in the previous example. That means it is an `instance variable`. Instance variables attributes to a class or in layman's terms, an adjective to a noun. Every cat has a color and every cat knows its color (let's pretend that they do). The `@` sign means that that variable is available everywhere with a class.

	```
	class Cat
		def initialize(color, name)
			@color = color
			@name = name
		end

		def color
			@color
		end

		def name
			@name
		end
	end

	my_cat = Cat.new('orange', 'Catman')
	my_cat.color #'orange'
	my_cat.name #'Catman'
	```

	* What did I do just now? I created a new cat, which set an `instance variable` of `@color` to the color I passed in. I then created a new method, `color`, which reads/returns that variable
	* Let's slim that code down by getting some `getters`. This sets and `gets` the variable for us. In Ruby, the code is `attr_reader`
	```
	class Cat
		attr_reader :color, :name

		def initialize(color, name)
			@color = color
			@name = name
		end
	end

	my_cat = Cat.new('orange', 'bob')
	my_cat.color #'orange'
	my_cat.name #bob
	```
	* What if the cat grows up and changes color or someone else adopts it? You want the ability to change the name and color right? Here's what that code could look like:
	```
	class Cat
		attr_reader :color, :name

		def initialize(color, name)
			@color = color
			@name = name
		end

		def color=(new_color)
			@color
		end

		def name=(new_name)
			@name
		end
	end

	my_cat = Cat.new('orange', 'Catman')
	my_cat.color #'orange'
	my_cat.color = 'white'
	my_cat.color #'white'
	```

	* Again, this is verbose. There's a concept in programming called `setters` which gets and `sets` a variable to something else. In Ruby, we use `attr_writer` Here is the code above, but refactored:
	```
	class Cat
		attr_reader :color, :name
		attr_writer :color, :name

		def initialize(color, name)
			@color = color
			@name = name
		end
	end

	my_cat = Cat.new('orange', 'Catman')
	my_cat.color #'orange'
	my_cat.color = 'white'
	my_cat.color #'white'
	```

	* If a class variable is both a getter and setter, we want to refactor that further into `attr_accessor` (allows getting and setting of a class variable):
	```
	class Cat
		attr_accessor :color, :name

		def initialize(color, name)
			@color = color
			@name = name
		end
	end

	my_cat = Cat.new('orange', 'Catman')
	my_cat.color #'orange'
	my_cat.color = 'white'
	my_cat.color #'white'
	```
	* What else can a cat do? Name some methods!
	```
	class Cat
		attr_accessor :color, :name

		def initialize(color, name)
			@color = color
			@name = name
		end

		def meow
			'MEOW!'
		end

		def meow_name_color #this is obviously not something that cats do
			"Meow! I am #{name} and I am a #{color} cat"
		end
	end

	my_cat = Cat.new('orange', 'Catman')
	my_cat.meow # MEOW!
	my_cat.meow_name_color
	```
	* Remember that the class variables (in our case, color and name, are accessible everywhere within the class). Once we go outside the class, we lose that class variable. Try it!
* [More](https://www.tutorialspoint.com/ruby/ruby_object_oriented.htm)


2:00 Projects (Ruby)
-------------------
* [Boggle](https://github.com/CodePlatoon/boggle)
* [Boggle Part 2](https://github.com/CodePlatoon/boggle2)
