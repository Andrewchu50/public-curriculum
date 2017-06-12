Day 4
======================
Class Videos
------------
* [Video 1](https://vimeo.com/220822437)
* [Video 2](https://vimeo.com/220822487)


Test-driven development
-----------------------------------------------
* [TDD Video](https://vimeo.com/203348818)
* TDD == Test-Driven Development
* TDD is the concept where you write tests with the desired end result first and then write the code you want to make those tests pass
* Why is this useful?
	* It makes for better code because you are first driven to think through what you want your code to do before you start writing code
	* It allows you to have a blueprint
	* It helps you think through potential pitfalls and bugs before it happens
* Many of the top tech companies in Chicago follow TDD processes
	* Braintree
	* DevMynd
	* Pivotal Labs
* The companies that use this are either very wealthy or consultancies who can bill this to their clients.
* It is definitely a slower process at the beginning when we are learning how to TDD, but makes for more sustainable code down the line. When things are properly tested from the start, whenever anything breaks down the line, you know immediately why it's broken.
* Red, Green, Refactor
	* This is the most popular way to approach test-driven development
	* First, write the test and run the test suite. It will fail your test and be `red` (broken)
	* Next, we write the code to make the test pass. This code can be as ugly as you need it to be to get the desired test to pass. This will pass your test and be `green`
	* Finally, we revisit the code we wrote and `refactor` it to make it cleaner and faster. Because you wrote good tests in the first step, you know that the code that you refactor will not change the behavior of the program
* It is most common in Ruby to use [RSPEC](http://rspec.info/) for TDD
	* It's definitely overkill for the basic problems we are writing now, but when we reach Rails, your fluency in writing tests in RSPEC will definitely help
* [Quick Left TDD Article](https://quickleft.com/blog/use-test-driven-development-tdd/)

BDD and RSPEC
--------
* [TDD vs. BDD Part 1](https://www.toptal.com/freelance/your-boss-won-t-appreciate-tdd-try-bdd)
* [TDD vs. BDD Part 2](http://joshldavis.com/2013/05/27/difference-between-tdd-and-bdd/)
* BDD is an evolution of TDD. It's still TDD, but with better guidelines where we write the behavior and specifications so that it's easier to read and to know what the code is supposed to do.

Practice with TDD and RSPEC
-------------
* [Sum Pairs](https://github.com/CodePlatoon/sum-pairs)
* [Most Frequent Integer](https://github.com/CodePlatoon/most-frequent-int)