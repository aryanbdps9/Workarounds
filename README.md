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
### Solution
[This stackoverflow answer](https://stackoverflow.com/a/56124666) says we need to remove the python history file (`~/.python_history` on Linux and `%userprofile%/.python_history` on Windows). Just deleting lines containing non-ascii characters worked for me.


## Enable Tab completion in cmd on Windows
I followed [this link](https://www.maketecheasier.com/enable-auto-complete-feature-command-prompt-windows/). Here are the steps:
1. Open Registry Editor.
2. Navigate to the following key:
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Command Processor`
3. Set the value of `CompletionChar` key (double click to open the edit dialogue box) to `9`. Make sure that Base is set to `Hexadecimal`. That's it!

Extra: ascii value of `Tab` key is `0x9`, hence we set the value of `CompletionChar` to `9`. If you want to use some other character for autocompletion, feel free to put its ascii value instead. [Here is a link to ascii table.](http://www.asciitable.com/).

