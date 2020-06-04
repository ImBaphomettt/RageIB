# RageIB

Rage Instructional Button. is a standalone Instructional Button for FiveM.


```lua
local object = UIInstructionalButton.__constructor()
Citizen.CreateThread(function()
    while true do
        Citizen.Wait(1.0)
        object:onTick()
    end
end)

RegisterCommand("background", function()
    object:UpdateBackground(255, 100, 0, 80)
end)

RegisterCommand("example", function()
    for i = 1, 300 do
        object:Add(tostring(i), i)
        Citizen.Wait(50)
    end
    object:Visible(true)
end)

AddEventHandler('onResourceStart', function(resourceName)
    if (GetCurrentResourceName() ~= resourceName) then
        return
    end
    object:onRefresh()
end)

```
<a href="https://ibb.co/sbT0ZZX"><img src="https://i.ibb.co/QpW244x/unknown.png" alt="unknown" border="0"></a>
