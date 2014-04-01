UISoup
======

#### This library supports UI-related testing using Python.

##### How to use examples:

* Calculator:
```python
from uisoup import uisoup


calculator = uisoup.get_window('Calculator')

calculator.drag_to(50, 50, x_offset=30, y_offset=5)
b1 = calculator.find(c_name='btn2')
b1.click()
ba = calculator.find(c_name='btnAdd')
ba.click()
b2 = calculator.find(c_name='btn3')
b2.click()
be = calculator.find(c_name='btnEquals')
be.click()
```

* Notepad:
```python
from uisoup import uisoup


# You can use wildcard in names such as "?" and "*".
notepad = uisoup.get_window('*Notepad')

notepad.set_focus()
kc = uisoup.keyboard.codes
uisoup.keyboard.send(kc.SHIFT.modify(kc.KEY_H), kc.KEY_E, kc.KEY_L,
                     kc.KEY_L, kc.KEY_O, kc.SPACE, kc.KEY_W, kc.KEY_O,
                     kc.KEY_R, kc.KEY_L, kc.KEY_D,
                     kc.SHIFT.modify(kc.KEY_1))

```

##### Also adds ```ui-inspector``` script that allows you to inspect UI elements. Just type it in terminal.
