# cp-sublime-files

# Precompile stdc++.h header file
1. Open CMD (admin) and then enter command: `cd "C:\Program Files\MinGW\lib\gcc\x86_64-w64-mingw32\8.1.0\include\c++\x86_64-w64-mingw32\bits"`
2. Now enter command: `g++ -std=c++14 stdc++.h`

Depending upin the c++ version, it can be set like: `-std=c++17`.

# Bonus
1. We can install the `Terminus` plugin available in Sublime packages, which can be configured like:
Change the default shell. Go to 'Preferences' > 'Package Settings' > 'Terminus' > 'Command Pallete'. And add below stanza.
```
  [
   {
        "caption": "Terminal (panel)",
        "command": "terminus_open",
        "args"   : {
           "cmd": "bash",
           "cwd": "${file_path:${folder}}",
           "title": "Command Prompt",
           "panel_name": "Terminus"
        }
   },
]
```

Note: `cmd` can be changes as per the OS.

- Setting key binding. Go to Go to 'Preferences' > 'Package Settings' > 'Terminus' > 'Key Bindings'. And add below stanza.
```
[
   {
       "keys": ["ctrl+`"],
       "command": "terminus_open",
       "args" : {
           "cmd": "bash",
           "cwd": "${file_path:${folder}}",
           "panel_name": "Terminus"
       }
   }
]
```


### Linux
To compile the header <bits/stdc++.h>, we need to compile this header using below steps:
1. Go to dir: `/usr/include/x86_64-linux-gnu/c++/13/bits`; Here `13` is the version
2. Now, compile the file using command: `g++ -std=c++17 stdc++.h`

# Resources:
1. https://www.geeksforgeeks.org/setting-up-sublime-text-for-cpp-competitive-programming-environment/
2. https://blog.codingblocks.com/2019/setting-up-a-c-competitive-programming-environment/

