# Workarounds
List of logistical problems with my computer and how I managed to solve them

## Anaconda Error
### Problem description
```python
(base) C:\WINDOWS\System32>python
Python 3.8.3 (default, Jul  2 2020, 17:30:36) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
Failed calling sys.__interactivehook__
Traceback (most recent call last):
  File "D:\ProgramData\Anaconda3\lib\site.py", line 440, in register_readline
    readline.read_history_file(history)
  File "D:\ProgramData\Anaconda3\lib\site-packages\pyreadline\rlmain.py", line 165, in read_history_file
    self.mode._history.read_history_file(filename)
  File "D:\ProgramData\Anaconda3\lib\site-packages\pyreadline\lineeditor\history.py", line 82, in read_history_file
    for line in open(filename, 'r'):
  File "D:\ProgramData\Anaconda3\lib\encodings\cp1252.py", line 23, in decode
    return codecs.charmap_decode(input,self.errors,decoding_table)[0]
UnicodeDecodeError: 'charmap' codec can't decode byte 0x9d in position 2152: character maps to <undefined>
```

[Solution](https://stackoverflow.com/a/56124666)
