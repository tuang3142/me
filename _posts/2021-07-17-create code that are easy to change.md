---
layout: post
title: "Create code that are easy to change"
categories: design, ror
---

# create code that are easy to change

### why

because change is inevitable. single purpose classes: easy to be reused later

### how

- ask questions: what the class is, what it does.
- describe class in 1 sentence. no `and/or`
- single res for method


### code adapt to change

- now - later trade off
- once place, not all over the places
- wrap instance variable in method, bc they are only defined **ONCE**

```ruby
class Gear
  attr_reader :cog, :chainring
  
  def initialize(chainring, cog)
    @chainring = chainring
    @cog = cog
  end
 
  def ratio
    chainring / cog.to_f # good
  end
end
```


### struct

Struct as “a convenient way to bundle a number of attributes together, using accessor methods, without having to write an explicit class.”

basically light weighted class, but shud not compare to hash i think?  
but when to use hash over struct then? -> ask tien (more than tien)
but struct is interesting. should use it more

```ruby
data = { coin:, price:, change: }
```

### quest?

- but what about when we need caching?
