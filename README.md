```ruby
#!/usr/bin/ruby

class SoftwareEngineer
  def initialize(params)
    @name              = params[:name]
    @role              = params[:role]
    @current_company   = params[:current_company]
    @languages_spoken  = params[:languages_spoken]
    @location          = params[:location]
    @contact           = params[:contact]
  end

  def say_hello
    message = [
      "Hello, World! Thanks for dropping by...",
      "My name is #{@name}, I am a #{@role} located in #{@location}.",
      "Currently working at #{@current_company}.",
      "Can speak #{@languages_spoken[0...-1].join(",")}, and #{@languages_spoken[-1]}.",
      "You can contact me at: #{@contact}.",
    ].join("\n")
  end
end

me = SoftwareEngineer.new({
  name:             "Ivan Reyes",
  role:             "Software Engineer",
  current_company:  "GMO Internet Group",
  languages_spoken: ["en_US", "es_CO", "ja_JP"],
  location:         "Tokyo, Japan",
  contact:          "https://www.linkedin.com/in/ivan-reyes-9504/"
})

puts me.say_hello
```
```
Hello, World! Thanks for dropping by...
My name is Ivan Reyes, I am a Software Engineer located in Tokyo, Japan.
Currently working at GMO Internet Group.            
Can speak en_US,es_CO, and ja_JP.
You can contact me at: https://www.linkedin.com/in/ivan-reyes-9504/.
=> nil
```

