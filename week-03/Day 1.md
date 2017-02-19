Day 1
=====================
Types of Ruby Variables
-----------------------
* [Ruby Variables Video 1](https://vimeo.com/203857910)
* [Ruby Variables Video 2](https://vimeo.com/203857659)

| Type             | Begins With        | Scope                                    |
|:----------------:|:------------------:|------------------------------------------|
|Local variable    | **a-z** *or* **_** | Available only within the immediate scope.
|Instance variable | **@**              | Available to a specific instance of a class
|Class variable    | **@@**             | Available anywhere in a specific class (including all instances) (avoid me)
|Global variable   | **$**              | Available everywhere (don't use me).
|Constant          | **ALL_CAPS**       | Available in the scope of their definition

### Local Variable
- Local variables start with a lowercase letter or an underscore.
- Local variables are only available within the block of its initialization.
- Local variables will raise an error if they are read before they're created
- Local variables are used often

```ruby
my_name = "<3 Jon!"
```

### Instance Variables
- Instance variables begin with `@`
- Instance variables are available to the object of it's initialization
- Instance variables are also used very commonly

```ruby
class Ghost
  attr_reader :name

  def initialize(name_var)
    @name = name_var
  end
end
```

### Class Variables
- Class variables begin with `@@`
- Class variables are available to the entire class (in any method)
- Class variables will raise an error if they are read before they're created
- Class variables can cause problem down the road (**avoid using them**)
- Class variables are sometimes used for application configuration

```ruby
class Ghost
  @@ghosts_in_the_world = 0
  attr_reader :name

  def initialize(name_var)
    @@ghosts_in_the_world +=1
    @name = name_var
  end

  def how_many_ghosts
    @@ghosts_in_the_world
  end
end
```

### Global Variables
- Global variables begin with `$`
- Global variables are available to the entire application
- Global variables are dangerous **Don't use them.**

```ruby
$dead = true

class Ghost

  def is_dead?
    $dead # this is bad
  end

end
```

Instantiating objects with hashes
--------------------------------------
* A `Hash` is a great way to pass in arguments to the `initialize` method of a `Class`. Have a look at this Class:

```ruby
class Address
  def initialize(first_name, last_name, street_one, street_two, city, state, country, postal_code)
    @first_name  = first_name
    @last_name   = last_name
    @street_one  = street_one
    @street_two  = street_two
    @city        = city
    @state       = state
    @country     = country
    @postal_code = postal_code
  end
end

Address.new("Jeremy","Flores","123 Fake St.","Apt Yes","Seattle","WA","USA","98115")
```

__Question: What happens if you don't have a `street_two` attribute?__

Let's try this again. This time, let's initialize using a `Hash`:

```ruby
class Address
  def initialize(address_hash)
    @first_name  = address_hash[:first_name]
    @last_name   = address_hash[:last_name]
    @street_one  = address_hash[:street_one]
    @street_two  = address_hash[:street_two]
    @city        = address_hash[:city]
    @state       = address_hash[:state]
    @country     = address_hash[:country]
    @postal_code = address_hash[:postal_code]
  end
end

Address.new(first_name: "Jeremy", state: "WA")
```

Using a hash to provide parameters to an `initialize` method lets us omit parameters that may not exist for some instances. It also adds clarity to `class` instantiation by explicitely stating keys and values.

```ruby
# not using a hash to initialize
Address.new("Jeremy","","","","WA","","")

# now with a fancy hash!
Address.new(first_name: "Jeremy", state: "WA")
```

Practice
-------------
* [Apple Trees](https://github.com/CodePlatoon/apple-trees)
* [Part 1](https://github.com/CodePlatoon/parsing-data-1)
* [Part 2](https://github.com/CodePlatoon/parsing-data-2)
* [Read this great article on CSV and Ruby](https://www.sitepoint.com/guide-ruby-csv-library-part/) - Please note that they are using an older version of Ruby but it should overall be a good resource.
