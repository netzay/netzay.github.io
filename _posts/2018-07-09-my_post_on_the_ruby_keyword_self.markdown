---
layout: post
title:      "My post on the Ruby keyword "self""
date:       2018-07-09 11:41:17 -0400
permalink:  my_post_on_self
---

The idea of self, describing the nuances as it pertains to Ruby instead of self as it pertains to me, ended up being a more daunting task than I originally imagined in my newbie programmer brain.  I know I still have lots to learn and as they say practice makes perfect, so here it goes...

First, calling self on a method in Ruby, refers the call implicity, to the current object being received.  

In Ruby, the value of using the keyword self, can vary based on the specific context in which it is used.  Importantly and maybe obviously, when self is used, at any given time it will only ever refer to the current specific object it is being called on.  In other words self can never be referring to two objects at any given time, only one.

Referencing self within the body of the class, refers to the current instance of the class, while creating a class method is done by defining the method on self.  This differs from referencing self within an instance method as it refers to the current object or instance of the call being made, not relating to the class itself.

To demonstrate:
<a href="https://imgur.com/AmikB6a"><img src="https://i.imgur.com/AmikB6a.png" title="source: imgur.com" /></a>

<a href="https://imgur.com/s8Fbfis"><img src="https://i.imgur.com/s8Fbfis.png" title="source: imgur.com" /></a>


Self called within the class: *puts the class itself  "Flower" *
Self called within the instance method puts the current object: 
*"#<Flower:0x007ff8f9016f18>"*
Calling an instance of the class on a class method will still return the parent class: *"Flower" *


Calling a class method within an instance method is one example of when the need to explicitly specify the receiver call will be self.  

<a href="https://imgur.com/Jt9VM0Y"><img src="https://i.imgur.com/Jt9VM0Y.png" title="source: imgur.com" /></a>

Additionally, when using an assignment operator within a writer method, explicitly calling self on the assignment variable is required, without, Ruby refers to it as local variable which makes sense, otherwise local variables would not be possible.

