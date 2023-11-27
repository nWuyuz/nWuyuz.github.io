---
layout:     post
title:      __slots__magic
subtitle:   a way to save RAM
date:       2023-11-09
author:     Nathan Wu
header-img: img/__slots__.png
catalog:   true
tags:
    -Notes
    -CS
---

# __slots__ MAJIK

**every classes have attributes**

For small classes it can be a bottle neck because **it wastes lots of RAM**

Here is a way to decrease it with **slots**

```py

class myclass(obj):

  def __init__(self.name.identify):

    self.name=name

    self.identify=identify

    self.setup()

```

**Without _slots, it is wasting more RAM**

```py

class myclass(obj):

  __slots=['name','identify']

  def __init__(self,name,identify):

    self.name=name

    self.identifier=identifier

    self.setup()


```

**The one with __slots__ can use much less RAM than the previous one**

