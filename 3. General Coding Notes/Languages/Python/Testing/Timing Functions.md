Use [`time.time()`](http://docs.python.org/library/time.html#time.time) to measure the elapsed wall-clock time between two points:
[Link](https://stackoverflow.com/questions/7370801/how-do-i-measure-elapsed-time-in-python)

```python
import time

start = time.time()
print("hello")
end = time.time()
print(end - start)
```