---
layout: post
title:  "Self in Ruby"
date:   2016-07-22 12:32:41 -0400
---

In Ruby, the concept of self seems tricky at first. But in principle it is quite simple—though applying the principle to different contexts can be difficult. Basically, a method must be called on an object (or a class object). So, you can't just do the following: 
`object_id`

The object_id method must be called on something. If nothing is specified, by default the method will be called on `self`. But what is self?

1. If you are inside a class definition, self is that class.
2. If you are inside a module definition, self is that module. 
3. If you are inside a method definition, self will be the object that calls that method. 

Rule 3 is a bit trickier, since it depends on the kind of method and on the object that eventually calls it. If it is a class method, self will be the class object that calls that method. 

```
class Archer
  def self.fire
    puts "Firing now"
    puts self
  end
end
```

`Archer.fire` will return:
```
Firing now
self: Archer
 => nil
```
  
Here is an example of self in an instance method (credits to "Robin Hood: Men in Tights" for the example, and for its general greatness):

```
class Archer
  def fire
    puts "He split Robin's arrow in twain!"
    puts self
  end
end
```

```
sheriff_of_rottingham = Archer.new
sheriff_of_rottingham.fire
#He split Robin's arrow in twain!
#<Archer:0x007fcc43874b70>
```

Now when let's create two archers and make the code conditional. Then we'll clearly see who self is when we call #fire.

```
class Archer
  attr_reader :name
  def initialize(name)
    @name = name
  end
  def fire
    if self.name == "Robin"
      puts "He split the Sheriff's arrow in twain!"
      puts self
    elsif self.name == "Sheriff of Rottingham"
      puts "He split Robin's arrow in twain!"
      puts self
    else
      puts "You're not part of this competition!"
    end
  end
end
```

Now we'll create three instances of the Archer class, and the output will show us how self differs depending on which instance calls it. 

```
robin = Archer.new("Robin")
sheriff_of_rottingham = Archer.new("Sheriff of Rottingham")
litte_john = Archer.new("Little John—though in real life, he's actually very big")
```
```
robin.fire
He split the sheriff's arrow in twain!
#<Archer:0x007fbe79a11fa0>
```
```
sheriff_of_rottingham.fire
He split Robin's arrow in twain!
#<Archer:0x007fcc43874b70>
```
```
little_john.fire
You're not part of this competition!
 => nil
 ```
  
So, when you're writing an instance method, you don't know exactly who self will be until an object calls it. But if you're writing the method within a class, you know it will be an instance of that class. 



 



