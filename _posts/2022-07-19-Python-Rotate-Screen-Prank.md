---
title: Python Rotate Screen Virus Prank
published: true
---

# [](#header-1)What is this?

This is a python "virus" that will be always rotating the screen 90º. Therefore, our victim will be so confused that he/she will not be able to do anything to stop the virus from executing.

Along with the virus I will post a fix file to get everything back to normal when the prank is over.

# [](#header-1)Requirements

*	python-time
*	rotate-screen
*	pywin32

# [](#header-1)Python code

```python
#This code will cause the display to rotate indefinitely
import time, rotatescreen as rs
pd = rs.get_primary_display()
angle_list = [90, 180, 270, 0]
while True:
    for x in angle_list:
        pd.rotate_to(x)
        time.sleep(0.5)
```

# [](#header-1)Fix code

```python
#This code returns the screen to normal.
import time, rotatescreen as rs
pd = rs.get_primary_display()
pd.rotate_to(0)
```
