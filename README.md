Code will let you understand how to use
```lua
-- This script lets you add custom modules for vape v4.
-- This only apply's to universal.lua however, your free to change the code if you want it to modify something else.

if not isfile("newvape/games/universal.lua") then
          loadstring(game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/main/NewMainScript.lua", true))()
end
repeat wait(0.01) until isfile("newvape/games/universal.lua")


local universalContents = game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/refs/heads/main/games/universal.lua", true)

-- This part is where you can add more code, this will go under the original code.

local newUniversal = universalContents .. [[




notif('hey guys', 'If you are seeing this, it worked! :D', 5)




]]


if isfile("newvape/games/universal.lua") then
    if readfile("newvape/games/universal.lua") ~= newUniversal then
        delfile("newvape/games/universal.lua")
        writefile("newvape/games/universal.lua", newUniversal)
        repeat wait(0.01) until isfile("newvape/games/universal.lua") and readfile("newvape/games/universal.lua") == newUniversal
    end
end

loadstring(game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/main/NewMainScript.lua", true))()
```
