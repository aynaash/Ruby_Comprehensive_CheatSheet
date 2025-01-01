# Ruby

# Variables

In Ruby, variables and constants are essential concepts for holding data in your programs. Lets value. Constants in Ruby are conventionally written in uppercase letters.
   - **Naming Convention:** All uppercase letters (i.e., `CONSTANT_NAME`).
       
       ```ruby
       MAX_SIZE = 100
       GRAVITY = 9.8
       
       ```
       
6. **Boolean Variables:**
   - **Definition:** Boolean variables represent two states: `true` or `false`.
   
   ```ruby
   is_active = true
   
   ```
   

### Constants in Ruby

- **Definition:** Constants hold values that should remain unchanged once assigned. They are typically used to store data such as configurations or mathematical constants (e.g., Pi, Gravity).
- **Naming Convention:** Always written in all uppercase letters.

```ruby
PI = 3.14
MAX_USERS = 100

```

- **Mutability:** While constants are intended to be immutable, Ruby allows you to change them (but it will issue a warning).

```ruby
PI = 3.14
PI = 3.1415  # This will show a warning but will still execute.

```

---

### Ruby Variable and Constant Exercise

Here are 10 questions to test your understanding of Ruby variables and constants.

### 1. **Basic Local Variables:**

What type of variable is `age` in the following code, and how can it be used inside and outside the `Person` class?

```ruby
def create_person
 age = 30
end

```

### 2. **Instance Variable Explanation:**

Consider this Ruby code:

```ruby
class Car
 def initialize(model)
   @model = model
 end
end

```

Explain the role of `@model`. How does it relate to the object?

### 3. **Changing Constants:**

What happens when you change the value of a constant, and why would this be a bad practice?

```ruby
MAX_SPEED = 120
MAX_SPEED = 150  # What will Ruby do here?

```

### 4. **Class Variables Behavior:**

How does the value of `@@count` behave between different instances of the `Book` class below?

```ruby
class Book
 @@count = 0

 def initialize(title)
   @@count += 1
   @title = title
 end
end

```

### 5. **Global Variable Accessibility:**

Define a global variable and show how it can be accessed within different methods.

### 6. **Assigning Boolean to a Variable:**

Create a variable `is_available` and assign a Boolean value to it.

### 7. **Constant Naming Conventions:**

Write a Ruby constant for storing the mathematical constant `Eulert access `my_variable` outside the `my_method` in this case:

```ruby
def my_method
 my_variable = 10
end
puts my_variable

```

### 10. **Instance vs. Class Variables:**

Compare the behavior of instance and class variables with a code example, explaining how they behave across instances of a class.

---

### Ruby Variable and Constant Facts

1. **Variable Assignment and Initialization:**
In Ruby, variables do not need to be declared before they are used, making Ruby extremely flexible in terms of defining variables.
2. **Thread-Safety:**
Ruby's constant mutability provides an interesting edge-case when it comes to multi-threaded environments where constants can unexpectedly change, though they are typically designed as read-only.
3. **Undefined Variables:**
If you attempt to use a variable before it's initialized, Ruby will raise a `NameError`. Conversely, undefined constants also throw an exception, but Ruby provides warnings for their reassignment.

---

# Data Types

In Ruby, data types define what kind of value a variable can hold. Understanding these data types is crucial to working with Ruby because they dictate the kind of operations you can perform on a variable, as well as how values are represented in memory. Heres integers are automatically scaled based on the platform, meaning they can be arbitrarily large without overflow.
- **Example**:
   
   ```ruby
   my_integer = 42
   puts my_integer   # Outputs: 42
   
   ```
   
- **Operations**:
   - Mathematical operations can be performed on integers, such as `+`, ``, ``, `/`, `%`:
       
       ```ruby
       result = 7 + 3  # 10
       result = 10 * 3 # 30
       
       ```
       

### 3. **Float**

- **Definition**: `Float` represents numbers that require decimals, or numbers that are not whole (i.e., floating-point numbers).
- **Example**:
   
   ```ruby
   my_float = 3.14
   puts my_float  # Outputs: 3.14
   
   ```
   
- **Operations**:
   - You can also perform mathematical operations on floats, but be mindful of precision errors when comparing floats:
       
       ```ruby
       result = 3.5 + 2.3 # 5.8
       
       ```
       

### 4. **Boolean**

- **Definition**: `Boolean` represents a truth value: either `true` or `false`.
- **Example**:
   
   ```ruby
   is_active = true
   has_permission = false
   
   ```
   
- **Operations**:
   - Boolean logic can be performed using `&&` (AND), `||` (OR), `!` (NOT):
       
       ```ruby
       puts true && false  # Outputs: false
       puts true || false  # Outputs: true
       
       ```
       

### 5. **Nil**

- **Definition**: `Nil` represents the absence of a value. In Ruby, `nil` is an object, and its type is `NilClass`.
- **Example**:
   
   ```ruby
   my_value = nil
   puts my_value  # Outputs: nothing (nil does not print)
   
   ```
   
- **Use cases**:
   - It is used to indicate that something is not present or has not been initialized.

### 6. **Array**

- **Definition**: An `Array` is an ordered collection of objects, which can be of any data type.
- **Example**:
   
   ```ruby
   my_array = [1, 2, 3, "hello"]
   puts my_array[0]  # Outputs: 1
   puts my_array[3]  # Outputs: hello
   
   ```
   
- **Operations**:
   - Accessing, modifying, and iterating over elements:
       
       ```ruby
       my_array.push(4)   # Adds 4 to the array
       my_array.each { |x| puts x }   # Iterates and prints each element
       
       ```
       

### 7. **Hash**

- **Definition**: A `Hash` (also known as a dictionary or map) is a collection of key-value pairs.
- **Example**:
   
   ```ruby
   my_hash = { "name" => "Sudeys", "age" => 25 }
   puts my_hash["name"]  # Outputs: Sudeys
   
   ```
   
- **Operations**:
   - You can add, access, or modify keys and values:
       
       ```ruby
       my_hash["email"] = "sudeys@example.com"  # Adds a new key-value pair
       my_hash.each { |key, value| puts "#{key}: #{value}" }  # Iterates over hash
       
       ```
       

### 8. **Symbol**

- **Definition**: A `Symbol` is like an immutable string but is more efficient. It's often used as keys for hashes and as identifiers in Ruby programs.
- **Example**:
   
   ```ruby
   my_symbol = :status
   puts my_symbol  # Outputs: status
   
   ```
   
- **Efficiency**:
   - Unlike strings, symbols are immutable and share the same object ID, making them faster when used repeatedly.

### 9. **Range**

- **Definition**: A `Range` represents an interval of values, defined by a start point and an endpoint. It can be inclusive or exclusive.
- **Example**:
   
   ```ruby
   range = (1..5)  # Inclusive of 5
   puts range.include?(5)  # Outputs: true
   
   ```
   
- **Use cases**:
   - You can use ranges in loops, to express continuous intervals.
   
   ```ruby
   (1..5).each { |n| puts n }  # Outputs: 1 2 3 4 5
   
   ```
   

### Ruby Data Type Comparison

| Type | Example | Operations Supported | Immutable |
| --- | --- | --- | --- |
| String | `"hello"` | Concatenation, Substring, etc. | Yes |
| Integer | `42` | Math operations | Yes |
| Float | `3.14` | Math operations | Yes |
| Boolean | `true` / `false` | Logic operators (AND, OR, NOT) | Yes |
| Nil | `nil` | == check, Conditional checks | Yes |
| Array | `[1,2,3]` | Add, Remove, Iterate | No |
| Hash | `{a:1, b:2}` | Add, Access, Iterate | No |
| Symbol | `:hello` | Compare, Use in Hash keys | Yes |
| Range | `1..5` | Iterate, Check inclusion | Yes |

---

---

# Operators and Expressions

In Ruby, **operators** are special symbols or words used to perform operations on values and variables, while **expressions** are combinations of variables, constants, and operators that yield a result. Heres Blocks, Procs, and Lambdas are foundational to writing reusable and concise code. Lets defined. | Returns control to the calling method. |

### **Example of Argument Behavior**

```ruby
proc = Proc.new { |x, y| puts x, y }
proc.call(1)  # Output: 1, nil (ignores missing arg)

lambda = ->(x, y) { puts x, y }
# lambda.call(1)  # Error: wrong number of arguments (given 1, expected 2)

```

### **Example of Return Behavior**

```ruby
def test_proc
 proc = Proc.new { return "Proc exited!" }
 proc.call
 "Method finished"
end
puts test_proc  # Output: "Proc exited!"

def test_lambda
 lambda = -> { return "Lambda exited!" }
 lambda.call
 "Method finished"
end
puts test_lambda  # Output: "Method finished"

```

---

### **5. Passing Blocks, Procs, or Lambdas to Methods**

### Passing a Block

```ruby
def run_block
 yield
end

run_block { puts "I'm a block!" }  # Output: I'm a block!

```

### Passing a Proc

```ruby
def run_proc(my_proc)
 my_proc.call
end

p = Proc.new { puts "I'm a Proc!" }
run_proc(p)  # Output: I'm a Proc!

```

### Passing a Lambda

```ruby
def run_lambda(my_lambda)
 my_lambda.call
end

l = -> { puts "I'm a Lambda!" }
run_lambda(l)  # Output: I'm a Lambda!

```

---

# Modules and Mixins

## **Modules in Ruby**

Modules are a way of grouping methods, classes, and constants together. Unlike classes, they cannot be instantiated or inherited. Modules serve two primary purposes:

1. **Namespaces:** Prevent name clashes by grouping related code together.
2. **Mixins:** Add shared behavior to classes using `include` or `extend`.

---

### **1. Defining a Module**

```ruby
module Greetings
 def say_hello
   "Hello!"
 end

 def say_goodbye
   "Goodbye!"
 end
end

```

The module above groups two methods: `say_hello` and `say_goodbye`.

---

### **2. Mixins with Modules**

Mixins allow modules to be included in classes to share behavior without inheritance.

### **Including a Module**

- `include`: Adds module methods as *instance methods* in a class.

```ruby
module Greetings
 def say_hello
   "Hello!"
 end
end

class Person
 include Greetings
end

person = Person.new
puts person.say_hello  # Output: Hello!

```

### **Extending a Module**

- `extend`: Adds module methods as *class methods* in a class.

```ruby
module Farewell
 def say_goodbye
   "Goodbye!"
 end
end

class Robot
 extend Farewell
end

puts Robot.say_goodbye  # Output: Goodbye!

```

---

### **3. Namespaces**

Modules can act as containers for related code, such as classes and constants. This avoids name collisions in larger projects.

### **Example**

```ruby
module MathTools
 class Calculator
   def add(a, b)
     a + b
   end
 end
end

calc = MathTools::Calculator.new
puts calc.add(2, 3)  # Output: 5

```

Here, `MathTools` serves as a namespace for the `Calculator` class.

---

### **4. Combining Mixins and Namespaces**

You can define methods and constants in the same module for both purposes.

### **Example**

```ruby
module Utils
 CONSTANT_PI = 3.14

 def self.square(number)
   number * number
 end

 def format_text(text)
   text.upcase
 end
end

puts Utils.square(4)         # Output: 16
puts Utils::CONSTANT_PI      # Output: 3.14

class Formatter
 include Utils
end

formatter = Formatter.new
puts formatter.format_text("hello")  # Output: HELLO

```

---

### **5. `Module` vs `Class` Comparison**

| **Aspect** | **Module** | **Class** |
| --- | --- | --- |
| Can be instantiated? | No | Yes |
| Can define methods? | Yes | Yes |
| Supports inheritance? | No | Yes |
| Used for? | Mixins, Namespaces | Objects and Blueprints for behavior |

---

Modules, with their mixins functionality, replace the need for multiple inheritance in Ruby. This simplicity makes Rubys default exception handling mechanisms!

## **Metaprogramming in Ruby**

Metaprogramming is a Ruby feature that lets you dynamically define methods, alter classes, or execute code. This provides powerful ways to write concise, adaptable, and reusable code.

---

### **1. `method_missing`**

The `method_missing` method is called when you invoke a method that doesns metaprogramming enables the ActiveRecord library in Rails to dynamically generate model methods based on database schemas. For example, `User.find_by_email(email)` is not pre-defined but dynamically created!

# Reflection

## **Reflection in Ruby**

Reflection is the ability to inspect and modify objects, classes, and their attributes at runtime. It allows a program to learn about its structure and behavior dynamically. Reflection in Ruby makes the language highly adaptable and powerful.

---

### **1. ObjectSpace**

`ObjectSpace` is a module that provides utilities to interact with all living objects in a Ruby program. It enables inspection, iteration, and manipulation of objects.

### **Key Methods**

- `ObjectSpace.each_object` Returns the memory size of an object.
- `ObjectSpace.count_objects` s `send` method is the foundation for many internal libraries. For example, Rails heavily uses `send` for dynamic attribute accessors in ActiveRecord models like `user.send(:email)`!

# Singletons

## **Singleton Classes in Ruby**

A singleton class is a class that exists only for a single object. Its garbage collector is invoked automatically but can be controlled manually in some cases.

### **Key GC Methods**

- `GC.start`: Forces garbage collection explicitly (not recommended for regular use).
- `GC.disable`: Temporarily disables garbage collection.
- `GC.enable`: Enables garbage collection if previously disabled.
- `GC.stat`: Provides statistics about the garbage collector.

### **Example: Forcing GC**

```ruby
puts "Before GC: #{GC.stat[:heap_free_slots]}"
GC.start
puts "After GC: #{GC.stat[:heap_free_slots]}"

```

---

### **4. Managing Memory with Variables**

Unused variables holding large data can cause excessive memory usage. To prevent this:

- **Set Large Variables to `nil`**: Explicitly release references to objects no longer needed.
   
   ```ruby
   large_data = "x" * 10_000_000
   large_data = nil
   GC.start
   
   ```
   
- **Use Lazy Enumerations**: Process data streams without creating large intermediate objects.

---

### **5. Symbols vs Strings in Memory**

- **Symbols**: Immutable, unique, and stored in memory only once. Useful for identifiers (`:key`).
- **Strings**: Mutable and stored separately every time they are created.

### **Memory Optimization Tip**

Prefer symbols for keys or repeated immutable values to save memory.

---

### **6. Best Practices for Memory Management in Ruby**

1. **Minimize Object Creation**
   - Avoid creating unnecessary objects inside loops.
   - Use caching mechanisms where appropriate.
2. **Use Lazy Evaluation**
   - Use `Enumerator::Lazy` for large collections to compute values on demand.
       
       ```ruby
       large_array = (1..Float::INFINITY).lazy.map { |x| x * 2 }.first(10)
       p large_array
       
       ```
       
3. **Reuse Data**
   - Reuse existing strings instead of creating new ones unnecessarily.
4. **Monitor Memory Usage**
   - Use tools like `memory_profiler` to track memory allocation and leaks.
       
       ```bash
       gem install memory_profiler
       
       ```
       

---

### **7. Monitoring and Debugging Tools**

1. **`ObjectSpace`**
   - Analyze live objects and memory usage:
       
       ```ruby
       require 'objspace'
       puts ObjectSpace.memsize_of("string")
       
       ```
       
2. **`memory_profiler`**
   - Reports memory usage for code blocks:
       
       ```ruby
       require 'memory_profiler'
       
       report = MemoryProfiler.report do
         100.times { "test".upcase }
       end
       
       report.pretty_print
       
       ```
       
3. **`GC::Profiler`**
   - Profile garbage collection activity:
       
       ```ruby
       GC::Profiler.enable
       puts "GC running..."
       GC.start
       puts GC::Profiler.result
       
       ```
       

---

### **8. Manual GC for Performance Optimization**

- In **short-lived applications**, you dont Markup Language) is a human-readable data serialization format. Ruby provides the `YAML` module for parsing and generating YAML.

### **2.1 Parsing YAML Strings**

Use `YAML.load` or `YAML.safe_load` to convert YAML strings to Ruby hashes or arrays.

```ruby
require "yaml"

yaml_string = <<~YAML
 name: Charlie
 age: 35
 skills:
   - Ruby
   - JavaScript
YAML

data = YAML.load(yaml_string)
puts data["name"]    # Charlie
puts data["skills"]  # ["Ruby", "JavaScript"]

```

**Note**: Use `YAML.safe_load` when dealing with untrusted inputs to avoid executing malicious code.

### **2.2 Reading YAML from Files**

```ruby
data = YAML.load_file("config.yml")
puts data["setting"]  # Access YAML file content

```

### **2.3 Generating YAML Strings**

Use `YAML.dump` to generate YAML from Ruby objects.

```ruby
ruby_hash = { name: "Dylan", age: 40, active: true }
yaml_output = YAML.dump(ruby_hash)

puts yaml_output
# Output:
# ---
# name: Dylan
# age: 40
# active: true

```

---

### **3. JSON vs. YAML**

| Feature | JSON | YAML |
| --- | --- | --- |
| Readability | Compact but less readable | Human-readable with indentation |
| Data Types | Strings, numbers, arrays, objects | Supports more types like dates |
| Comments | Not allowed | Allowed |
| File Size | Smaller | Larger due to whitespace |

---

### **4. Practice Examples**

1. **Parsing and Generating JSON**
   - Create a program that reads a JSON file containing user data, modifies a value, and writes it back.
2. **Reading and Writing YAML**
   - Parse a YAML file containing app settings, change a configuration, and save it back.
3. **Converting Between Formats**
   - Write a script to convert a JSON file into a YAML file.

---

### **Example: Parsing and Generating Both Formats**

```ruby
require "json"
require "yaml"

# Convert JSON to YAML
json_data = '{"name": "Eve", "age": 28}'
ruby_hash = JSON.parse(json_data)

yaml_output = YAML.dump(ruby_hash)
puts yaml_output

# Convert YAML back to JSON
yaml_data = <<~YAML
 name: Adam
 age: 31
YAML

ruby_hash = YAML.load(yaml_data)
json_output = JSON.generate(ruby_hash)
puts json_output

```

---

### **5. Handling Large Files**

For large JSON/YAML files, you can use streaming parsers like `oj` (for JSON) or third-party gems for optimized parsing.

---

### **Neovim Tips**

1. **YAML Highlighting**: Ensure your Neovim setup supports YAML and JSON syntax highlighting. Use plugins like `vim-polyglot`.
2. **Linting Support**: Install `eslint` for JSON and `yamllint` for YAML to ensure correct syntax.

---

### **Fun Ruby Fact**

Ruby's flexibility allows you to extend the core `JSON` or `YAML` modules. For instance, you could customize `to_json` behavior for your classes:

```ruby
class User
 attr_accessor :name, :age

 def initialize(name, age)
   @name = name
   @age = age
 end

 def to_json(*_args)
   { name: @name, age: @age }.to_json
 end
end

puts User.new("Alice", 25).to_json

```

## **Ruby Date, Time, and Math Libraries**

Ruby provides extensive libraries to handle dates, times, and mathematical calculations. These libraries are versatile and efficient for performing operations like formatting, calculations, and time manipulation.

---

### **1. Date and Time in Ruby**

### **1.1 Date Class**

The `Date` class represents a calendar date (year, month, day). It's part of the Ruby standard library, so you need to require it.

```ruby
require 'date'

date = Date.new(2023, 12, 30)  # Year, Month, Day
puts date                     # 2023-12-30
puts date.year                # 2023
puts date.month               # 12
puts date.day                 # 30

```

### **1.2 Current Date**

You can get today's date using `Date.today`.

```ruby
today = Date.today
puts today   # e.g., 2024-12-30

```

### **1.3 Formatting Dates**

Format dates with `strftime`.

```ruby
formatted_date = Date.today.strftime("%d-%m-%Y")
puts formatted_date   # 30-12-2024

```

Common format specifiers:

- `%Y`: Year (e.g., 2024)
- `%m`: Month (01-12)
- `%d`: Day of the month (01-31)

---

### **1.4 Time Class**

The `Time` class represents the date and time with precision down to the second.

```ruby
current_time = Time.now
puts current_time     # e.g., 2024-12-30 10:15:30 +0000

```

### **Working with Time**

```ruby
time = Time.new(2024, 12, 30, 14, 35, 20) # Year, Month, Day, Hour, Min, Sec
puts time.hour    # 14
puts time.min     # 35
puts time.sec     # 20

```

### **Adding/Subtracting Time**

```ruby
later_time = Time.now + (60 * 60) # Add 1 hour
puts later_time

```

### **1.5 DateTime Class**

The `DateTime` class combines both the `Date` and `Time` functionality and supports operations like addition or subtraction of days.

```ruby
require 'date'

datetime = DateTime.new(2024, 12, 30, 15, 0, 0) # Year, Month, Day, Hour, Min, Sec
puts datetime  # 2024-12-30T15:00:00+00:00

# Add 10 days
puts datetime + 10   # 2024-01-09T15:00:00+00:00

```

---

### **2. Math Library**

The Ruby `Math` module provides mathematical functions for calculations.

### **2.1 Common Methods**

- `Math.sqrt(number)`: Square root.
- `Math.log(number, base)`: Logarithm.
- `Math.sin(angle)`, `Math.cos(angle)`, `Math.tan(angle)`: Trigonometric functions.
- `Math::PI`: The constant Pi.
- `Math::E`: Eulers widely used to write readable, structured tests and assertions for your Ruby code.

### **2.2 Basic RSpec Syntax**

- **`describe`**: Describes a class, method, or feature.
- **`it`**: Describes the behavior or expectations of the test case.
- **`expect`**: Defines what the expected outcome should be.

```ruby
# my_class.rb
class MyClass
 def add(a, b)
   a + b
 end
end

# my_class_spec.rb
require 'rspec'
require './my_class'

RSpec.describe MyClass do
 it 'adds two numbers' do
   expect(MyClass.new.add(2, 3)).to eq(5)
 end
end

```

You can run RSpec tests using `rspec my_class_spec.rb`.

### **2.3 Common RSpec Matchers**

- `eq`: Checks for equality (`expect(5).to eq(5)`).
- `be`: Checks for identity (`expect(obj).to be_nil`).
- `raise_error`: Checks if a block raises an error.

### **2.4 RSpec Examples**

```ruby
RSpec.describe 'Array' do
 it 'contains the number 4' do
   expect([1, 2, 3, 4]).to include(4)
 end

 it 'raises error when dividing by zero' do
   expect { 1 / 0 }.to raise_error(ZeroDivisionError)
 end
end

```

---

### **2.5 Minitest Framework**

Minitest is another lightweight framework for testing in Ruby, integrated into Ruby by default, and focuses on simplicity. Minitest has similar concepts to RSpec, but its syntax differs.

### **2.6 Basic Minitest Syntax**

- **`def test_`**: Defines a test method.
- **`assert`**: Used for assertions (conditions that should be true).
- **`assert_equal`**: Checks if two values are equal.

```ruby
require 'minitest/autorun'

class MyClassTest < Minitest::Test
 def test_addition
   assert_equal 5, 2 + 3
 end

 def test_nil_value
   assert_nil nil
 end
end

```

### **2.7 Running Tests**

To run the tests, just execute the script and Minitest will run all defined test methods starting with `test_`.

---

## **3. TDD/BDD Principles**

### **3.1 Test-Driven Development (TDD)**

TDD focuses on writing tests before writing the actual code. The typical flow in TDD involves the **Red-Green-Refactor** cycle:

1. **Red**: Write a test that fails (because the code isn't implemented yet).
2. **Green**: Write just enough code to make the test pass.
3. **Refactor**: Clean up the code without changing functionality.

### **3.2 Behavior-Driven Development (BDD)**

BDD emphasizes defining the behavior of an application from the user's perspective. It's often used with RSpec and relies on **natural language-style tests** for specifying expected behaviors.

- **Describe** the features.
- **It** outlines the specifications.

For example, in BDD:

```ruby
RSpec.describe 'Adding Numbers' do
 it 'should sum two numbers correctly' do
   expect(MyClass.new.add(1, 2)).to eq(3)
 end
end

```

---

### **3.3 Mocking and Stubbing**

### **3.4 Mocking**

Mocking is when you replace an object or method call with a predefined, "mocked" behavior.

For example, in RSpec:

```ruby
RSpec.describe 'User' do
 it 'sends email on creation' do
   user = double('user')
   allow(user).to receive(:send_email)

   # Now, calling the method won't do anything:
   user.send_email
   expect(user).to have_received(:send_email)
 end
end

```

### **3.5 Stubbing**

Stubbing is when you replace a method on an object with a fixed response.

```ruby
class Account
 def balance
   # Real balance-fetching code
 end
end

# Stub
allow(account).to receive(:balance).and_return(100)

```

---

## 

Ruby's dynamic nature allows for incredible flexibility, including overriding and redefining methods during runtime (metaprogramming). For instance, method definitions can even change based on the presence of arguments:

```ruby
def foo(arg = nil)
 arg.nil? ? "No arguments" : "Received #{arg}"
end

```

## **Functional Programming Features in Ruby**

Ruby is primarily an object-oriented programming language, but it also supports several functional programming features. These features enable you to use Ruby in a functional way, such as higher-order functions, immutability concepts, lazy enumerators, and working with enumerable methods. Lets flexibility with blocks makes it easy to implement higher-order functions.

---

## **2. Enumerables**

The **Enumerable** module in Ruby provides a collection of methods that help work with collections (arrays, hashes, etc.) in a functional style. Many methods in the Enumerable module are higher-order functions. Some common methods include `map`, `select`, `reduce`, `each`, `find`, and `reject`.

### **2.1 Example: Using Enumerable Methods**

```ruby
arr = [1, 2, 3, 4, 5]

# map
squared = arr.map { |n| n**2 }
puts squared  # Output: [1, 4, 9, 16, 25]

# select
evens = arr.select { |n| n.even? }
puts evens  # Output: [2, 4]

# reduce
sum = arr.reduce(0) { |sum, n| sum + n }
puts sum  # Output: 15

```

### **2.2 Example: Finding Elements**

```ruby
# find returns the first element matching the block condition
arr = [3, 7, 8, 10]
found = arr.find { |n| n > 6 }
puts found  # Output: 7

```

### **2.3 Example: Rejecting Elements**

```ruby
arr = [10, 20, 30, 40]

# reject returns elements for which the block condition is false
rejected = arr.reject { |n| n < 30 }
puts rejected  # Output: [30, 40]

```

The `Enumerable` module encourages functional programming by focusing on collection transformations with methods that take blocks.

---

## **3. Immutability Concepts**

In functional programming, immutability refers to the concept that data should not be modified after itt immediately process all elements. Instead, it postpones evaluation until you explicitly ask for the data.

### **Example: Lazy Evaluation**

```ruby
arr = (1..10).lazy

# map doesn't evaluate immediately, but transforms lazily
lazy_map = arr.map { |n| n * 2 }

# Using take to force evaluation
result = lazy_map.take(5).to_a
puts result  # Output: [2, 4, 6, 8, 10]

```

In this case, the map operation does not occur until we call `take(5)`. By chaining methods on a lazy enumerable, only the required elements are processed, which can greatly improve performance when dealing with large data sets.

### **4.2 Chaining Lazy Operations**

```ruby
arr = (1..1000).lazy

# Chaining map, select, and take operations
result = arr.map { |n| n * 2 }.select { |n| n.even? }.take(5).to_a
puts result  # Output: [4, 8, 12, 16, 20]

```

In this example:

- The `map` and `select` operations will be lazily evaluated, meaning the calculations are deferred until `take(5)` is called.
- Only the first 5 even numbers (after multiplication by 2) are evaluated.

---

Rubyll need to create a `Gemfile` in your project directory. The `Gemfile` lists all the required gems for your application and any specific versions you need.

### **Creating a Gemfile**

A `Gemfile` is a plain-text file where you specify your dependencies. A basic `Gemfile` looks like this:

```ruby
source 'https://rubygems.org'

gem 'rails', '~> 7.0.0'
gem 'pg', '>= 1.2.3'
gem 'puma', '~> 5.0'

```

Here:

- The `source` tells Bundler where to fetch the gems from, usually `https://rubygems.org`.
- Each `gem` line specifies a gem name and the version you need.

### **Install Dependencies**

Once you have your `Gemfile`, you install the dependencies defined in it using:

```
bundle install

```

This command installs the gems specified in the Gemfile, and Bundler also creates a `Gemfile.lock` file, which locks the versions of the gems yous dependencies.

### **1.3 Bundler Commands Summary:**

- **bundle install** - Installs the gems defined in `Gemfile`.
- **bundle update** - Updates the gems to the latest compatible versions according to `Gemfile`.
- **bundle exec** - Executes a command in the context of the gems listed in `Gemfile.lock`.
- **bundle outdated** - Lists all outdated gems.

---

### **2. Creating and Managing Your Own Gems**

Creating your own Ruby gem allows you to package your Ruby code and make it reusable across multiple projects or share it with the Ruby community. Here's how you can create and manage your gem.

### **2.1 Steps to Create a Simple Ruby Gem**

### **1. Setup Gem Structure**

Use the `bundler gem` command to create the necessary directories and files:

```
gem install bundler
bundle gem my_gem

```

This generates a skeleton structure like:

```
my_gem/
  lib/
  my_gem.rb
  Gemfile

```

- **bin/**: Contains executable files (optional for gems).
- **lib/**: Contains the core functionality of your gem.
- **my_gem.gemspec**: The specification file for the gem, describing metadata, dependencies, etc.
- **Gemfile**: Lists dependencies if the gem needs other gems.

### **2.2 Define Functionality in `lib/my_gem.rb`**

Edit the `lib/my_gem.rb` to define the functionality of your gem.

For example, a simple gem that prints "Hello, World":

```ruby
module MyGem
 def self.hello
   puts "Hello, World!"
 end
end

```

### **3. Editing the Gemspec (`my_gem.gemspec`)**

The `.gemspec` file contains metadata about your gem, like its name, version, description, and dependencies. Open `my_gem.gemspec` and edit the required fields. Here's an example:

```ruby
Gem::Specification.new do |spec|
 spec.name          = "my_gem"
 spec.version       = "0.1.0"
 spec.author        = "Your Name"
 spec.email         = "your_email@example.com"
 spec.summary       = "A simple gem that says Hello World"
 spec.files         = Dir["lib/**/*"]
 spec.require_paths = ["lib"]
end

```

### **4. Build and Install Your Gem Locally**

Once your gem is ready, you can build it into a `.gem` file:

```
gem build my_gem.gemspec

```

You can then install it locally for testing:

```
gem install ./my_gem-0.1.0.gem

```

### **5. Publish Your Gem**

Once yous version number according to Semantic Versioning (MAJOR.MINOR.PATCH). After changing the version, rebuild the gem and push it again to RubyGems:

```
gem build my_gem.gemspec
gem push my_gem-0.2.0.gem

```

### **3. Gem Best Practices**

1. **Write Tests:** Use testing libraries like **RSpec** or **Minitest** to write tests for your gem functionality to ensure stability.
2. **Document the Gem:** Include usage instructions in your `README.md`. Clear documentation is crucial for user adoption.
3. **Semantic Versioning:** Use [Semantic Versioning](https://semver.org/) for version management to help users determine the impact of updates.

---

## **Performance Optimization in Ruby**

Optimizing the performance of Ruby applications is important, especially as they grow in complexity. Performance issues can arise from inefficient algorithms, poor memory usage, or unnecessary computation. Optimizing Ruby applications often involves profiling, memory management, and leveraging concurrency.

### **1. Benchmarking and Profiling**

### **1.1 Benchmark Module**

Rubys GC will eventually handle this on its own.
- **Freezing Immutable Objects**: Use `.freeze` on strings and other objects that do not need modification. This saves memory by sharing objects between references.

```ruby
str = "Hello"
str.freeze  # Prevent modification, reducing memory overhead

```

- **Lazy Loading and Iteration**: Ruby's **`Enumerator`** and **lazy iteration** can be very useful for memory-sensitive applications. Instead of loading entire collections into memory, lazy enumerators only load data when its GC activity and performance with the following:

```ruby
GC.stat

```

- **Manual GC Trigger**: You can manually invoke Ruby's garbage collector:

```ruby
GC.start

```

Calling `GC.start` can help free up memory in critical sections of your application but should generally be avoided unless necessary, as Ruby's GC is fairly good at managing memory without user intervention.

### **2.3 Avoid Memory Leaks**

Memory leaks can arise if objects are not properly discarded or kept unnecessarily in memory. These can be prevented with:

- **Weak References**: Use `WeakRef` for references to large objects that you don't want to keep alive after the garbage collection cycle.

```ruby
require 'weakref'

object = SomeLargeObject.new
weak_ref = WeakRef.new(object)

```

- **Identifying Memory Leaks**: Tools like `memory_profiler` can help identify memory leaks by analyzing your program's memory usage.

```
gem install memory_profiler

```

### **3. Parallel and Concurrent Programming**

Ruby, by default, uses Global Interpreter Lock (GIL), which makes true parallel execution of threads impossible for Ruby processes, but concurrency (doing tasks seemingly simultaneously) can still be achieved. If performance improvement requires true parallelism, threading, fibers, or even native extensions are possible solutions.

### **3.1 Threading**

Ruby supports threading to execute multiple blocks of code concurrently, useful for I/O-bound tasks like web requests or file reading.

```ruby
thread = Thread.new do
 sleep(2)
 puts "Hello from thread!"
end

thread.join  # Wait for thread to finish before continuing
puts "Main thread finished!"

```

- **Thread Pooling**: Consider using thread pools (e.g., `concurrent-ruby` gem) when creating multiple threads in Ruby.

### **3.2 Fibers**

Fibers are lightweight concurrency primitives that allow the programmer to manually yield control. Fibers are not as resource-intensive as threads because they are cooperative and only run one at a time.

```ruby
fiber = Fiber.new do
 puts "First"
 Fiber.yield
 puts "Second"
end

fiber.resume  # Output: "First"
fiber.resume  # Output: "Second"

```

- **When to Use Fibers**: Use fibers for concurrency but not parallelism (since they are not truly parallel).

### **3.3 Async and EventMachine**

For even better concurrency, you can use the `async` gem, which allows writing asynchronous, non-blocking code for I/O-bound tasks.

- **Install `async` gem**:

```
gem install async

```

- **Basic Usage**:

```ruby
require 'async'

Async do
 puts "Running asynchronously"
 sleep(1)
 puts "Done"
end

```

- **EventMachine** is another popular gem for handling asynchronous I/O. It enables non-blocking operations for networking or other high-latency I/O, providing better performance for servers and real-time systems.

### **3.4 Parallel Execution (Using `parallel` gem)**

For CPU-bound tasks, threads alone may not provide the desired performance due to the GIL. In such cases, you can use the **`parallel` gem** to run tasks in separate processes (leveraging true multi-core parallelism).

- **Basic Usage of `parallel`**:

```ruby
gem install parallel

Parallel.each([1, 2, 3]) do |num|
 # Expensive work
 sleep(1)
 puts "Processed #{num}"
end

```

- **Explanation**: This gem spawns separate processes for each job, bypassing the GIL for CPU-bound tasks.

---

In Ruby, performance optimization is multifaceted, combining benchmarking, profiling, memory management, and concurrent programming techniques. To summarize:

1. **Benchmark and Profile**: Use tools like `Benchmark` for timing and **ruby-prof** for profiling your code to find performance bottlenecks.
2. **Memory Optimization**: Reduce memory usage by reusing objects, using `nil`, and leveraging **Lazy Enumerators**. Also, monitor and optimize garbage collection.
3. **Concurrency**: Use threads, fibers, or asynchronous gems to handle concurrent tasks. For CPU-bound tasks, **parallel execution** in separate processes can increase performance.

With the right tools and optimizations, Rubys root. This file allows you to enable or disable specific cops (rules), and configure settings (like maximum line lengths).
   
- **Usage**:
Run RuboCop to check your code style:
   
   ```
   rubocop
   
   ```
   
   To auto-correct some offenses:
   
   ```
   rubocop -a
   
   ```
   
   **Example Output**:
   
   ```
   10 files inspected, 5 offenses detected
   
   ```
   
   RuboCop supports a variety of configuration options and is customizable to different styles. You can also use it within an editor for real-time feedback.
   

### **1.2 Reek**

**Reek** is a tool that detects code smells in your Ruby code. Code smells refer to things that may not necessarily be bugs but suggest that your code might need some refactoring. Reek analyzes your code for bad practices, design flaws, or areas that could cause problems later.

- **Installation**:
   
   ```
   gem install reek
   
   ```
   
- **Usage**:
Run Reek on your project folder to check for smells:
   
   ```
   reek
   
   ```
   
   **Common Smells Detected by Reek**:
   
   - **Long Method**: A method that does too much, violating the Single Responsibility Principle.
   - **Feature Envy**: A method that uses many of the instance variables or methods of another object.
   - **Large Class**: A class that is trying to do too many things.
- **Example Output**:
   
   ```
   app/models/user.rb -- Error: The class 'User' has a complexity score of 11.
   
   ```
   
   By fixing code smells, you improve the maintainability and readability of your code.
   

---

### **2. Debugging Tools**

### **2.1 Pry**

**Pry** is an interactive Ruby shell and debugging tool that can be used for inspecting objects, changing states during execution, and exploring code interactively.

- **Installation**:
   
   ```
   gem install pry
   
   ```
   
   Or add it to the Gemfile for Rails or your project:
   
   ```ruby
   gem 'pry'
   
   ```
   
- **Usage**:
Insert a `binding.pry` line where you want to start debugging in your code:
   
   ```ruby
   def some_method
     binding.pry
     puts "This is after the pry"
   end
   
   ```
   
   When the program reaches this line, it will pause, and you'll be dropped into an interactive shell. This allows you to inspect variables, check the call stack, and even alter your code on the fly.
   
- **Common Commands in Pry**:
   - **`exit`**: Exit the pry session.
   - **`ls`**: List the methods and instance variables of an object.
   - **`cd`**: Navigate through the call stack.
   - **`show-method`**: Show the source code of a method.

### **2.2 Byebug**

**Byebug** is another popular debugger for Ruby applications, especially in Ruby on Rails. It provides step-by-step debugging where you can pause execution, step through code line-by-line, and inspect variables.

- **Installation**:
Add it to your `Gemfile`:
   
   ```ruby
   gem 'byebug'
   
   ```
   
   Or install it globally:
   
   ```
   gem install byebug
   
   ```
   
- **Usage**:
Insert the `byebug` statement where you want execution to halt and enter debug mode:
   
   ```ruby
   def my_method
     a = 10
     byebug  # Execution pauses here
     b = 20
   end
   
   ```
   
- **Common Commands in Byebug**:
   - **`next`**: Move to the next line of code.
   - **`step`**: Step into the function being called.
   - **`continue`**: Continue execution until the next breakpoint.
   - **`quit`**: Exit the debugger.
   - **`print <variable>`**: Print the value of a variable.

---

### **3. Documentation Tools**

### **3.1 RDoc**

**RDoc** is a Ruby tool for generating documentation from the comments in your code. It reads your Ruby files and generates HTML, XML, or a simple text format with documentation based on special markup.

- **Installation**:
   
   ```
   gem install rdoc
   
   ```
   
- **Usage**:
You can generate RDoc documentation for your project by running:
   
   ```
   rdoc
   
   ```
   
   RDoc will automatically parse the source code files and generate documentation files.
   
- **Markup Syntax**:
RDoc supports special comment syntax for creating documentation. For example:
   
   ```ruby
   # This is the add method
   # It adds two numbers
   #
   # == Example
   #   add(2, 3)  #=> 5
   def add(a, b)
     a + b
   end
   
   ```
   

### **3.2 YARD**

**YARD** is another documentation tool for Ruby, offering enhanced support and flexibility compared to RDoc, with better handling for complex codebases and a richer set of features for documenting and structuring documentation.

- **Installation**:
   
   ```
   gem install yard
   
   ```
   
- **Usage**:
Generate documentation for your project:
   
   ```
   yard
   
   ```
   
- **YARD Markup Syntax**:
YARD also uses comments, but supports extra features and customization. Here's an example:
   
   ```ruby
   # Adds two numbers.
   #
   # @param [Integer] a The first number.
   # @param [Integer] b The second number.
   # @return [Integer] The sum of the two numbers.
   #
   # @example Adding two numbers:
   #   add(1, 2)
   def add(a, b)
     a + b
   end
   
   ```
   
- YARDs widely used in Ruby communities.

- **Installation**:
   
   ```
   \curl -sSL https://get.rvm.io | bash -s stable
   
   ```
   
- **Basic Usage**:
   - Install a Ruby version:
       
       ```
       rvm install 2.7.0
       
       ```
       
   - Use a specific Ruby version:
       
       ```
       rvm use 2.7.0
       
       ```
       
   - Create and switch to a new gemset:
       
       ```
       rvm gemset create mygemset
       rvm gemset use mygemset
       
       ```
       

---

### **Summary**

In Ruby development, using the right tools is crucial for improving code quality, debugging effectively, and maintaining clear documentation.

- **Linters** like **RuboCop** and **Reek** help maintain code quality and identify common code smells.
- **Debugging tools** such as **Pry** and **Byebug** allow for efficient inspection and fixing of code at runtime.
- **Documentation tools** like **RDoc** and **YARD** can automatically generate clear and structured documentation from your code.
- **Version management tools** like **rbenv** and **RVM** help manage Ruby versions and gemsets, making it easy to switch environments based on project requirements.

By using these tools and practices, you can ensure your Ruby code remains high quality, well-documented, and easy to maintain.

# Symbols and keywords

Ruby has a rich set of **symbols** and **keywords**, each serving a specific purpose. Below is a structured explanation of all symbols and keywords used in Ruby, including examples to clarify their roles.

---

## **Symbols**

Ruby symbols are lightweight, immutable identifiers often used in place of strings for keys, method names, and values.

### Common Symbols

| Symbol | Explanation | Example |
| --- | --- | --- |
| `:` | Denotes a symbol. Often used for hash keys or identifiers. | `:name` or `{ :key => "value" }` |
| `#` | Begins a single-line comment or refers to instance methods. | `# This is a comment` or `object#method` |
| `@` | Marks an instance variable. | `@name = "Ruby"` |
| `@@` | Marks a class variable. | `@@instances_count = 0` |
| `$` | Marks a global variable. | `$global_var = 42` |
| `?` | Suffix for predicate methods that return a boolean. | `[].empty? # true` |
| `!` | Suffix for methods with destructive actions; can indicate "not." | `"ruby!".upcase! # "RUBY!"`, `!true # false` |
| `=>` | Hash rocket; used for key-value pairs (alternative to `:`). | `{ :key => "value" }` |
| `..` | Creates an inclusive range. | `(1..5) # Includes 5` |
| `...` | Creates an exclusive range. | `(1...5) # Excludes 5` |
| `::` | Used for namespacing modules and classes or accessing constants. | `Math::PI # 3.14159` |

---

## **Keywords**

Ruby has 44 reserved keywords that cannot be used as variable or method names. These keywords enable Ruby's language features like loops, conditionals, and method definitions.

### Keywords by Category

### 1. **Control Flow**

| Keyword | Description | Example |
| --- | --- | --- |
| `if` | Conditional branching. | `if condition; puts "yes"; end` |
| `elsif` | Adds more branches to `if` conditions. | `elsif other_condition` |
| `else` | The default branch of an `if`. | `else; puts "no"` |
| `unless` | Executes code only if a condition is false. | `unless condition; puts "no"` |
| `case` | Switch-like structure for multiple conditions. | `case value; when 1; puts "one"` |
| `when` | Represents cases in `case`. | `when 2; puts "two"` |
| `while` | Repeats while a condition is true. | `while i < 5; i += 1` |
| `until` | Repeats until a condition is true. | `until i >= 5; i += 1` |
| `for` | Iteration over a range or enumerable. | `for i in 1..3; puts i; end` |
| `break` | Exits a loop prematurely. | `break if condition` |
| `next` | Skips to the next iteration. | `next if i.even?` |
| `redo` | Restarts the loop iteration. | `redo if condition` |
| `retry` | Reattempts the block after rescue. | `begin...rescue...retry` |

---

### 2. **Method and Block Definitions**

| Keyword | Description | Example |
| --- | --- | --- |
| `def` | Begins a method definition. | `def greet; puts "hello"; end` |
| `end` | Closes a block, method, or class. | `end` |
| `yield` | Pauses the method and yields to a block. | `yield if block_given?` |
| `alias` | Creates a new name for a method. | `alias new_name old_name` |
| `undef` | Removes a method definition. | `undef some_method` |

---

### 3. **Classes and Modules**

| Keyword | Description | Example |
| --- | --- | --- |
| `class` | Begins a class definition. | `class Person; end` |
| `module` | Begins a module definition. | `module Utilities; end` |
| `super` | Calls the parent method. | `super(arg)` |
| `self` | Refers to the current object. | `self.name` |
| `nil` | Represents nothingness. | `value.nil?` |

---

### 4. **Variables and Scoping**

| Keyword | Description | Example |
| --- | --- | --- |
| `local_variables` | List all defined local variables in scope. | `p local_variables` |
| `defined?` | Checks if an identifier is defined. | `defined?(var)` |

---

### 5. **Miscellaneous**

| Keyword | Description | Example |
| --- | --- | --- |
| `true` | Represents a truthy value. | `if true` |
| `false` | Represents a falsey value. | `unless false` |

---

### Pro Tips

1. **Symbol vs String**
Use symbols (`:key`) in cases where immutability and efficiency matter (e.g., hash keys).
2. **Constant Names**
Constants should be named in ALL_CAPS by convention.

---

### C
