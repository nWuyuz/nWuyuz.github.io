---
layout:     post
title:      Ditch That Else
subtitle:   Arrow coding should be abandoned
date:       2023-11-11
author:     Nathan Wu
header-img: img/ditch that else.png
catalog:   true
tags:
    
    -CS
---

# Arrow Coding

>**Naturally, when we learn to code, we are very likely to get into a *if-else structure*, and solve the *margin issues* in the else lines.**
>
>**It is quite safe to do this because we know we have protected the code from *inappropriate inputs.***
>
>**However, this also make our code to be *really hard to read.***

```py
if(SomeConditionMet):
    #do sth

    #...

    return sth
    #...

    #and 100 lines more

    #and more

else(YouDontExpectThis):
    #Now take your margin situation

   return sth
```

The issue is that the edge case handling can be left at the end, so we add code above it, and ***the ifs will dig deeper.***

```py
if(sth):
  #do this

  if(sth):
    #do that

      if(sth):
          #do this

          if(sth):
            #do that

          else:
            #solve that

      else:
        #solve this

  else:
  #solve that

else:
  #Finally, solve this

#Do this
```
**Code nesting can be the easiest way to bring *unnecessary complexity* to your code. The human brain can only deal with a few different things at a time, so when facing a code that you need to dig this deep, it is easy to forget something.**

**Our business processes are complex enough, why bringing it back to coding?**

**There is a simple way to solve the arrow coding.**

# Ditch that Else. Invert the logic. Tackle the edge case first.

```py
if(somestrangeconditions):
    #take care of the edge condition

#then happily deal with the things that you expect

return something
```
    
This can also be used to deal with several edge conditions:

```py
if(sth happen):
    #deal with it

if(sth happen):
    #take care of it before the mains

if(ThisIsTheFinaStrangeCondition):
    #done with margin conditions, now main.
    
#Then happily code your main principle
```

**Lets [ditch that else](https://blog.codinghorror.com/flattening-arrow-code/)**
      
