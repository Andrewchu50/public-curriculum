Day 2
=======================
CSV as a Database
----------------------
* [CSV Video](https://vimeo.com/204077023)
### What is a Database?
A _database_ is a system of storing and organizing information on a computer. In this case a _CSV_ will act as our database. In most cases a database can be thought of as a table or group of tables:

| ID | Team     | Wins  | Losses   |
|:---|:-------- |:------|:---------|
| 1  | Patriots | 10    | 2        |
| 2  | Bears	  | 2     | 10       |


We're going to quickly create a CSV to read. Let's create a CSV from the data of the top 5 NFL teams, courtesy of ESPN. Who can explain what is going on with this weird code below? Check the Ruby Docs!

```ruby
require 'csv'
teams = [
  [1, "Patriots", 10, 2],
  [2, "Bears", 2, 10]
]
CSV.open("team_data.csv", "w") do |file|
  teams.each do |team|
    file << team
  end
end
```

__Question: What does csv data look like?__

### The `CSV` Class
Ruby includes a CSV class tailored for working with csv data:

```ruby
require 'csv'
# Reads the contents of the file into an array of arrays.
CSV.read("team_data.csv")
# => [["1", "Patriots", 10, 2], ["2", "Bears", 2, 10]]

# Returns a CSV Object, to be read or manipulated.
csv = CSV.open("team_data.csv")
# <#CSV io_type:File io_path:"file.csv" encoding:UTF-8 ...>
```

The `open` method requires at least one argument and up to three arguments as well as an optional block.

```ruby
CSV.open(filename, mode='r', options) {|file| block}
```

The required argument is the CSV filename and path. The second argument (`mode`) sets what permissions Ruby has to the file when it is opened. This defaults to `r` (read only). Possible values are:

|Mode |  Meaning
|:---:|-----------------------------------------------------------|
|"r"  |  Read-only, starts at beginning of file  (default mode)   |
|"r+" |  Read-write, starts at beginning of file.                 |
|"w"  |  Write-only, truncates existing file to zero length       |
|"w+" |  Read-write, truncates existing file to zero length.      |
|"a"  |  Append write-only, starts at end of file if file exists. |
|"a+" |  Append read-write, starts at end of file if file exists. |
|"b"  |  Binary file mode                                         |
|"t"  |  Text file mode                                           |

Most modes will create a new file if one doesn't already exist with the given name.

If you pass a block to `open`, Ruby will open the file, execute the code within the block (the file contents is given to the block as a local variable), and then close the file.

```ruby
require 'csv'
CSV.open("team_data.csv", 'a') do |csv|
  csv << [5, "Jupiter", 318, 5.2]
end
```

We can iterate over each line of the file using the `each` method:

```ruby
require 'csv'
CSV.open("team_data.csv", 'r').each do |line|
  puts line
end
```

The `.read` method requires one argument, the filename, and allows for additional options. `.read` first opens the CSV file, then reads the contents of it into a new `Array`. Each row of CSV data is translated into an array as well.

```
# team_data.csv
1,Patriots,10,2
2,Bears,2,10
```

```ruby
require 'csv'
require 'awesome_print'
array_of_team_data = CSV.read("team_data.csv")
ap array_of_team_data
```

Practice
-------------
* [Word Guess CSV](https://github.com/CodePlatoon/word-guess)
* [Schools](https://github.com/CodePlatoon/school)
* Watch the following videos:
  * [Video 1](https://www.youtube.com/watch?v=_NSBm_Q431Y)
  * [Video 2](https://www.youtube.com/watch?v=wpG-uXmlNj4)
  * [Video 3](https://www.youtube.com/watch?v=eXiCza050ug)
  * [Video 4](https://www.youtube.com/watch?v=4Z9KEBexzcM)
