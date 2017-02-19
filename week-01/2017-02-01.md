Day 3
=======================
Ruby Fundamentals
----------------------
* Why are we learning two languages?
	* You will most likely not work in the first language you learn
	* To avoid being scared of learning new things - if you get stuck in one language and are scared of other languages, then you won't make it in development.
	* Main Point: Same exact concept, different syntax
* [Slides 27-39](/week-01/intro_to_rails_final.pdf)
* Variables - Difference between Ruby and Javascript
	* JS
		* You generally declare `var` in front of the variable
		* Variables are written in `camelCase`
	* Ruby
		* Simply assign your variable to something
		* Variables are written in `snake_case`
* Defining methods
	* `functions === methods` (JS)
	* `functions == methods` (Ruby)
	* JS
		```
		function addTwo(number) {
			console.log(number + 2);
		};
		```
		* Need to have a `function` and curly brackets to define where the code block begins and ends
		* Should generally have `;` semicolons at the end of a train of thought
	* Ruby
		```
		def add_two(number)
			puts number + 2
		end
		```
		* `def` and `end` wil act as your curly brackets
		* No semicolons necessary

Practice in Ruby
--------------------------------
* [99 Bottles](https://github.com/CodePlatoon/99_bottles_challenge)
* [Deaf Grandma](https://github.com/CodePlatoon/deaf_grandma_challenge)

1:00 JS Fundamentals - Collections
----------------------------------
* Collections are data structures that store information for us
* Two common ones are arrays and hashes
* [Arrays](https://prezi.com/khg0wb0dqio-/ga/)
* Arrays...
	* Maintain the order of a list by index
	* Allow duplicates (show an example)
	* Have efficient random access since there is an index
* Accessing array elements - start counting at 0 and move up. To access the last index of an array, it'll be the length minus 1
	* In JS, we create an array by declaring a variable a setting it equal to an array. This array can be empty or filled in
	* Methods are called upon the arrays to alter the array or to get information
	* Array methods can be mutating or non-mutating. Mutating means that you change the original data structure, non-mutating means you don't mutate
	* List of common methods [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
* Hashes and Hash Tables
	* For the purposes of our class, hashes and hash tables are synonymous
	* JS does not have hash tables - it only has objects but acts the same way.
	* Good introduction into OO
	* Objects hold sets of key-value pairs in the same way that dictionaries hold word-meaning pairs. Values are assigned to different keys.
	```
	var petNames = {dog: ‘Max’}


	// Add key-value pair using dot notation:
	petNames.cat = ‘Mewie’


	// Add key-value pair using bracket notation:
	petNames[‘bird’] = ‘Bluey’
	```
* Hashes...
	* Do not have implied order
	* Are very efficient to access its values since you access by key
	* Allows duplicate values but keys have to be unique

* Set
	* Kind of a mix between arrays and hashes
	* It's a collection of unordered values with no duplicates
		* By comparison, arrays have order and can have duplicates
	* For most of your junior career, you'll be using only Hashes and Arrays.

Practice
--------------------------
* [Practice with a Pair](https://github.com/CodePlatoon/git-pair)
* [Roman Numerals](https://github.com/CodePlatoon/roman_numerals) in Ruby
* [Factorial](https://github.com/CodePlatoon/factorial) in Ruby
* [Linear Search](https://github.com/CodePlatoon/linear_search) in Ruby
