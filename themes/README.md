# Modus

This theme is primarily designed for Ruby syntax highlighting according to https://github.com/zed-extensions/ruby/blob/main/languages/ruby/highlights.scm

## Comment

### style.syntax.comment
```ruby
# This is a comment
```

## Primitives

### style.syntax.boolean
```ruby
true
false
```

### style.syntax.number
```ruby
1
42
3.14
```

### style.syntax.string
```ruby
"hello world"
'single quotes'
```

### style.syntax.string.special.symbol
```ruby
:symbol
:"symbol with spaces"
%i[array of symbols]
{ key: "value" }  # key is a symbol
```

### style.syntax.string.regex
```ruby
/pattern/
/\d+/i
```

### style.syntax.string.escape
```ruby
"hello\nworld"
"tab\there"
```

## Constants

### style.syntax.constant
```ruby
CONSTANT_VALUE
PI
MAX_SIZE
```

### style.syntax.constant.builtin
```ruby
nil
__FILE__
__LINE__
__ENCODING__
**nil
```

## Types

### style.syntax.type
```ruby
class MyClass
end

module MyModule
end

MyClass  # constant references
```

### style.syntax.type.super
```ruby
class Child < Parent
end

class Child < Namespace::Parent
end

class Child < Deep::Nested::Parent
end
```

## Variables

### style.syntax.variable
```ruby
identifier
global_variable
```

### style.syntax.variable.parameter
```ruby
def method(param1, param2 = default, keyword:, &block)
  # param1, param2, keyword are parameters
end

[1, 2, 3].each { |item| puts item }  # item is a block parameter
```

### style.syntax.variable.special
```ruby
self
super
@instance_variable
@@class_variable
```

## Functions

### style.syntax.function.builtin
```ruby
include SomeModule
extend SomeModule
prepend SomeModule
refine SomeClass
using SomeModule
```

### style.syntax.function.method.builtin
```ruby
defined?(variable)
```

### style.syntax.function.method

- alias
  ```ruby
  alias new_name old_name
  alias size length
  alias + add
  ```

- setter
  ```ruby
  def name=(value)
    @name = value
  end

  def age=(years)
    @age = years
  end

  attr_writer :email  # creates email= setter
  ```

- method (identifier names)
  ```ruby
  def calculate_total
    # method body
  end

  def user_name
    @name
  end
  ```

- method (constant names)
  ```ruby
  def MyMethod
    # method body
  end
  ```

- singleton_method
  ```ruby
  # Class methods
  def self.create_user
    # class method
  end

  def MyClass.factory_method
    # another class method syntax
  end

  # Singleton methods on objects
  obj = Object.new
  def obj.special_method
    # method only available on this specific object
  end
  ```

- method calls
  ```ruby
  puts "hello"
  user.name
  Calculator.add(1, 2)
  ```

## Keywords

### style.syntax.keyword
### style.syntax.keyword

- Control flow
  ```ruby
  if condition
    puts "true"
  elsif other_condition
    puts "elsif"
  else
    puts "false"
  end

  unless negative_condition
    puts "unless block"
  end

  case value
  when "a"
    puts "a"
  when "b"
    puts "b"
  else
    puts "default"
  end
  ```

- Loops
  ```ruby
  while counter < 10
    counter += 1
  end

  until finished
    do_work
  end

  for item in collection
    puts item
  end
  ```

- Method and class definitions
  ```ruby
  def method_name
    return "value"
  end

  class MyClass
    def initialize
    end
  end

  module MyModule
  end
  ```

- Exception handling
  ```ruby
  begin
    risky_operation
  rescue StandardError => e
    handle_error
  ensure
    cleanup
  end
  ```

- Loop control
  ```ruby
  loop do
    next if skip_condition
    break if exit_condition
    retry if retry_condition
  end
  ```

- Logical operators
  ```ruby
  a and b
  x or y
  ```

- Blocks and yielding
  ```ruby
  def block_method
    yield if block_given?
  end
  ```

- Method aliasing
  ```ruby
  alias new_method old_method
  ```

- Additional keywords
  ```ruby
  def method_with_params
    x = 1
    then puts x  # 'then' keyword
  end

  if user.admin?
    do_admin_stuff
    return unless authorized?
    while tasks.any?
      process_task
      break if emergency?
    end
  end
  ```

### style.syntax.keyword.exception
```ruby
raise StandardError, "message"
fail "error message"
catch :symbol
throw :symbol
```

### style.syntax.keyword.import
```ruby
require 'library'
require_relative 'local_file'
load 'file.rb'
```

## Operators and Punctuation

### style.syntax.operator
```ruby
! ~ + - ** * / % << >> & | ^ > < <= >= == != =~ !~ <=> || && .. ... = **= *= /= %= += -= <<= >>= &&= &= ||= |= ^= => ->
```

### style.syntax.punctuation.delimiter
```ruby
, ; . ::
```

### style.syntax.punctuation.bracket
```ruby
( ) [ ] { } %w( %i(
```

### style.syntax.punctuation.special
```ruby
"Hello #{name}!"  # #{ } are punctuation.special in interpolation
```

## Embedded Content

### style.syntax.embedded
```ruby
"Hello #{name}!"  # The interpolated content inside #{ }
"Result: #{calculate(x, y)}"
```
