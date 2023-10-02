```ruby
#!/usr/bin/ruby

class SoftwareEngineer
  def initialize(params)
    @name              = params[:name]
    @role              = params[:role]
    @current_company   = params[:current_company]
    @languages_spoken  = params[:languages_spoken]
    @location          = params[:location]
  end

  def say_hello
    puts "Hello, World! Thanks for dropping by..."
  end
end

me = SoftwareEngineer.new({
  name:             "Ivan Reyes",
  role:             "Software Engineer",
  current_company:  "GMO Internet Group",
  languages_spoken: ["en_US", "es_CO", "ja_JP"],
  location:         "Tokyo, Japan"
})

me.say_hello
```
