---
published: 2020-12-01
id: 636
author: orsinium
---

# emojis

Python has rich support for Unicode, including referencing glyphs (including emojis, of course) by name.

Get glyph name:

```python
'🤣'.encode('ascii', 'namereplace')
# b'\\N{ROLLING ON THE FLOOR LAUGHING}'
```

Convert name to a glyph:

```python
'\N{ROLLING ON THE FLOOR LAUGHING}'
# '🤣'

# case doesn't matter:
'\N{Rolling on the Floor Laughing}'
# '🤣'
```

A good thing is that f-strings also aren't confused by named unicode glyphs:

```python
fire = 'hello'
f'{fire} \N{fire}'
# 'hello 🔥'
```
