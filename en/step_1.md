- Substituting single characters using **regex** is fairly simple using the `re` module in Python.

	```python
	import re
	text = 'cat'
	text = re.sub(r'c', 'b', text)
	```

- This will turn `cat` to `bat`. Sometimes you might want to substitute more that one type of character though.

- For instance, you might want to change all mentions of the word `grey` to `black` but you are aware that Americans spell the word `gray`. You need to match both words therefore. To do this you can use a search for `[ae]` which will match both the letters `a` and `e`.

	```python
	import re
	text = 'The walls were grey. The walls were gray'
	text = re.sub(r'gr[ae]y', 'white', text)
	```

- This will turn `text` into the following:
  ```python
  The walls were white. The walls were white
  ```
