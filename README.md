#[Plutfo][1]

`plutfo` is a Pure [Lua][2] UTF-8 Operations library which is compatible with the Lua 5.3 [`utf8`][3] module and [`lutf8`][4]

##Dependencies

NONE! Other than the standard [String][5], [Math][6] and [Table][7] libraries

No C nor C++ code is used at all, just Lua

##Usage

Just grab it

```shell
git clone git@github.com/Cations/plutfo.git
```

And require it into your project and use it as you would use the [`utf8`][3] module

```lua
local utf8 = require "plutfo"
```

Check the [UTF-8 section][3] in the [Lua Manual][8] for info on the available functions. Or the [Wiki][9] for more in depth examples (**WIP #3**)

##Benchmarks

Yet to come! (#2) But it should be slower in Lua 5.1 to Lua 5.3 compared to the native [`utf8`][3] module or [`lutf8`][4]

Could be faster in [LuaJIT][10] because it requires less calls to native code, which the JIT compiler can't optimize, yet it uses `string.gmatch` a lot which can't be optimized either so who knows

##Spec

Currently there is no spec (#2), but I'm working on it, plutfo should work as intended most of the time.

Errors exist mainly because plutfo doesn't error on wrong arguments or when an invalid byte sequence is found. This needs to be fixed, check issue #1

##Credits

Kyle Smith and [Minh Ngo][12] which created [this awesome utf8 library][13] which I used as a reference

##License

The [`plutfo`][1] library is licensed under [**MIT License**][14]

Copyright (c) 2016 [Cations][15] ([Pablo A. Mayobre][16])

[1]:https://www.github.com/Cations/plutfo
[2]:https://www.lua.org/
[3]:http://www.lua.org/manual/5.3/manual.html#6.5
[4]:http://luarocks.org/modules/positive07/lutf8
[5]:http://www.lua.org/manual/5.3/manual.html#6.4
[6]:http://www.lua.org/manual/5.3/manual.html#6.7
[7]:http://www.lua.org/manual/5.3/manual.html#6.6
[8]:http://www.lua.org/manual/5.3/manual.html
[9]:https://www.github.com/Cations/plutfo/wiki
[10]:http://www.luajit.org/luajit.html

[12]:https://www.github.com/markandgo
[13]:https://gist.github.com/markandgo/5776124

[14]:https://www.github.com/Cations/plutfo/blob/master/LICENSE
[15]:https://www.github.com/Cations
[16]:https://www.github.com/Positive07