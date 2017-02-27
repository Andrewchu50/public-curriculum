Day 2
=====================
Ruby Gems
--------------
* Package manager for distributing Ruby libraries
* Library == Gem
* [List of all gems](https://rubygems.org/gems)
* Gems are basically thousands of lines of code that someone wrote to make your life easier.
	* Each gem does something different and serves specific purposes

Javascript Libraries
-------------------------
* [List of JS libraries](https://www.javascripting.com/)
* Javascript libraries are a bit more involved in terms of getting them to work, but are the same as Ruby gems.
	* Javascript libraries are thousands of Javascript code that someone wrote to make your life easier and your website better
	* You may have heard of some of these JS libraries - React was written by Facebook and the big 3 frameworks are Angular, Ember, and Backbone
	* Makes your website more of a joy to use and makes consumption of whatever you want to portray nice to look at
* Let's take a look at some of them
	* [D3](https://d3js.org/)
	* [Animate](https://daneden.github.io/animate.css/)
	* [Three JS](https://threejs.org/examples/)

Debugging with Pry in Ruby
-------------------------------
* This morning, we talked about Ruby Gems. One of those Gems that we can use for debugging is called [pry](https://rubygems.org/gems/pry/versions/0.10.3)
* Pry is especially useful because it allows us to drop into the execution of our code at a specific point
* Let's try it!
`gem install pry # in the terminal`
```
require 'pry' # at the top of any file
binding.pry # put this anywhere in the file - this will stop the code when it hits this line
```
* Are you ever wondering what a certain value is when you are iterating over a loop? What a return value is? You can find it in `pry`!
* A popular alternative to `pry` is `byebug`. It's your call on which debugging tool you want to use.

Debugging with Debugger in Javascript
------------------------------------------
* Debugger for Javascript is similar to `pry` in Ruby in that it allows you to drop into your code at any point.
* Usage is very simple: you simply put `debugger;` at the point you want to drop into
* Why is debugging with `pry` and debugger important?
	* Teaches you to read the error messages and Google things first.

Practice Problems
----------------------
* [Caesar Cipher](https://github.com/CodePlatoon/caesar-cipher) in JS/Ruby
* [Bubble Sort](https://github.com/CodePlatoon/bubble-sort) in Ruby/JS
