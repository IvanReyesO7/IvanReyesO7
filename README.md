```ruby
#!/usr/bin/ruby

class SoftwareEngineer
  def initialize
    @name = "Ivan Reyes"
    @role = "Software Engineer"
    @language_spoken = ["en_US", "es_CO", "ja_JP"]
  end

  def say_hello
    puts "Hello, World! Thanks for dropping by..."
  end
end

me = SoftwareEngineer.new
me.say_hello
```
