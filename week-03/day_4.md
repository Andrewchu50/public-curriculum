Day 4
======================
CS Concepts: Benchmarking
------------------------------
* [Benchmarking and Big O](https://vimeo.com/204237961)
* What is Benchmarking?
  * Essentially, benchmarking is the act of timing your code - how long it takes to execute?
* Why do we do this?
  * We are basically looking to see if your code is slow. If it's slow, how can we improve the speed?
  * If your code is slow, then you are basically asking people to go to another site or move away from your page.
  * Right now, your code is only impacting a handful of people but once you get into the thousands of users, and especially if one piece of code relies on another, then you need to have code that's fast.
* Ruby Benchmarking
  * In Ruby, they have a module in their standard library (think Array/Hash/String methods from the docs) that will take care of things for you
  * [Benchmarking](https://ruby-doc.org/stdlib-2.4.0/libdoc/benchmark/rdoc/Benchmark.html) documentation
  * [Blog post on Benchmarking](http://rubylearning.com/blog/2013/06/19/how-do-i-benchmark-ruby-code/)
  * [Another blog](http://mitrev.net/ruby/2015/08/28/benchmarking-ruby/)
* How does this apply to us?
  * We want to write algorithms and code that is as fast as possible, code that uses as little memory as possible. If we write a lot of bad code that executes slowly, your site is going to be slow. You want to get into the habit of writing the fastest, most readable code that you can.

CS Concepts: Big O Notation
--------------------------------
* Big O Notation describes the performance and/or complexity of your algorithm. It's directly related to Benchmarking in that how long your code takes to run and how complex it is in relation to Big O are directly correlated. If it's very complex, then it's going to be slow. If it's not very complex, it will be faster.
* Big O tells you how complex an algorithm is based on what you provide to it.
* The more complex something is, the more you want to refactor. Of course, there are times where you cannot refactor anymore, but as much as possible, you want it to be less complex when it comes to Big O.
* Let's take a look at some examples of Big O
```
O(1) - The amount of time it takes to run your code is CONSTANT. Whether you pass in one argument or a million arguments, it's all the same.

def first_element_is_red?(array)
  array[0] =='red' ? true : false
end


O(n) - The amount of time it takes to run your code WILL GROW LINEARLY based on what you put in. This means that if you pass in 1 parameter, it'll be quick. If you pass in a million parameters, it will take 1 million times longer.

def contains?(array, value)
  array.each do |item|
    return true if item == value
  end
  false
end

O(n^2) - The amount of time it takes to run your code will DOUBLE based on your input. Take a look at the code below. If we have an array with 4 items, it'll return have to run through the code 16 times (or 4**2) to get me the result. For each item in our list, we have to do that many additional operations.

def all_combinations(array)
  results = []
  array.each do |number_1|
    array.each do |number_2|
      results << [number_1, number_2]
    end
  end
end

Obviously, having an algorithm that's less complex will help with runtime.
```
* [Extra Resources: Sorting & Efficiency PowerPoint via Ada](https://docs.google.com/presentation/d/1elJdFGo1ZcEI8rcmWgbSUFS33b-DoB2z_cA1yRaM1ec/edit#slide=id.ga34e6770f_0_81)


Practice
--------
* [Bank Accounts](https://github.com/codeplatoon/bank-accounts)
* [Big O Problems 1](https://github.com/CodePlatoon/big-o)
* [Big O Problems 2](https://github.com/CodePlatoon/big-o-2)
* Read over ADTs / Stacks / Queues [here](https://github.com/Ada-Developers-Academy/textbook-curriculum/blob/master/04-cs-fundamentals/classroom/02-ADTs-Stacks-Queues.md)
