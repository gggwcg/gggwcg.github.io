```python

import os

#获取当前目录,包含最后的斜杠
def get_current_dir():
	current_path = os.path.abspath(__file__)
	parent_path = os.path.dirname(current_path) + os.path.sep
	return parent_path

```
