# pbpytestwpytest

#### Test strategy
note
- Subcutaneous test: A test that doesn’t run against the final end-user interface, but against an interface just below the surface. 
Since most of the tests in this book test against the API layer—not the CLI—they qualify as subcutaneous tests.


```
from collections import namedtuple
Task = namedtuple('Task', ['summary','owner','done','id'])
Task.__new__.__defaults__ = (None, None, False, None)
def test_defaults():
"""Using no parameters should invoke defaults."""
  t1 = Task()
  t2 = Task(None, None, False, None)
  assert t1 == t2
```







