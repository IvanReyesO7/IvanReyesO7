```ruby
#!/usr/bin/ruby

class SoftwareEngineer
  def initialize(name:, role:, current_company:, languages_spoken:, location:, contact:)
    @name             = name
    @role             = role
    @current_company  = current_company
    @languages_spoken = languages_spoken
    @location         = location
    @contact          = contact
  end

  def say_hello
    languages = if @languages_spoken.size > 1
      "Can speak #{@languages_spoken[0...-1].join(", ")}, and #{@languages_spoken[-1]}."
    else
      "Can speak #{@languages_spoken[0]}."
    end

    <<~MSG
      Hello, World! Thanks for dropping by...
      My name is #{@name}, I am a #{@role} located in #{@location}.
      Currently working at #{@current_company}.
      #{languages}
      You can contact me at: #{@contact}.
    MSG
  end
end

me = SoftwareEngineer.new(
  name:             "Ivan Reyes",
  role:             "Software Engineer",
  current_company:  "GMO Internet Group",
  languages_spoken: ["en_US", "es_CO", "ja_JP"], # BCP 47 codes: English (US), Spanish (Colombia), Japanese (Japan)
  location:         "Tokyo, Japan",
  contact:          "https://www.linkedin.com/in/ivan-reyes-9504/"
)

puts me.say_hello
```

```
Hello, World! Thanks for dropping by...
My name is Ivan Reyes, I am a Software Engineer located in Tokyo, Japan.
Currently working at GMO Internet Group.            
Can speak en_US, es_CO, and ja_JP.
You can contact me at: https://www.linkedin.com/in/ivan-reyes-9504/.
=> nil
```

