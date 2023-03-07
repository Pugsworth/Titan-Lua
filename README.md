# Titan
## What is it

Titan is my own split of lua based on Lua 5.4.4 with many changes that I feel enhance the language.


## Why

Lua is great as is, but it does a lot of weird things that can get fairely annoying. There have also been lots of advancements in the sector of programming lanuage development.
Some claim syntactic sugar is bad and should be elimitnated as much as possible.
I'd argue that syntactic sugar is very beneficial for implementing new syntax and structure to a language without changing the underlying language. Most of these could be compiled into raw lua.

## Features
- [ ] Continue keyword
- [x] Compound assignments (+=, *=, etc) - Provided by ../patches/plusequals-5.4.patch
- [ ] range function and type (similar to python
- [ ] Range operator (1..3) -> range(1, 3)
- [ ] Null (nil) safety operator (?)
- [ ] Required operator (!)
- [ ] Promises.
- [ ] Compiler warning of shadowed variables
- [ ] Destructuring (a, b, c = {1, 2, 3})
- [ ] Binary number literals
- [ ] __len metamethod
	Allows tables to override what is returned by the '#' operator.
- [ ] Short if statements
	- return 3 if true
		Returns 3 always
	- break if data == ""
		Break a loop if data is empty
- [ ] Last argument function outside (TODO: Find the correct name)
	This one is borrowed from Kotlin. If the last argument to a function is a function, you will be able to call it like so:
	```lua
		function doThing(a, b, func)
			func(a, b)
		end
		
		doThing(1, 2) do |a, b| print(a, b) end
	```

	instead of:
	```lua
		doThing(1, 2, function(a, b) print(a, b) end)
	```
	Haven't settled on the exact syntax yet...
