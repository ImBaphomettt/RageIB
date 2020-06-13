# RageIB

Rage Instructional Button is a standalone Instructional Button API for FiveM.

## Lua Example
```lua
Citizen.CreateThread(function()
    local object = UIInstructionalButton.New()
    object:Refresh() -- call this even after the creation of the object
    object:Visible(true) -- set the object visibility

    RegisterCommand("background", function()
        object:UpdateBackground(255, 100, 0, 80) -- upgrade the background based on r, g, b, a parameters you will pass
        object:Refresh() -- refresh the game part if you changed some data
    end)

    RegisterCommand("example", function()
        for i = 1, 300, 1 do
            object:Add(tostring(i), i) -- add a button to the object based on name and control id
        end

        object:Refresh()
    end)

    while true do
        object:Draw() -- draw the ui you need this or it will not show anything
        Citizen.Wait(0)
    end
end)
```

<a href="https://ibb.co/sbT0ZZX"><img src="https://i.ibb.co/QpW244x/unknown.png" alt="unknown" border="0"></a>
