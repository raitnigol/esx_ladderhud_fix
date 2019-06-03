**Replace your [esx]/esx_status/client/main.lua** with this file if you don't know what piece of code to add to your code.

How to fix esx_ladderhud not working:
Add this piece of code to the 56th line of the code:
```lua
TriggerEvent('esx_ladderhud:updateBasics', GetStatusData(true))
```

How the code looks at first place (line 56 and 57):
```lua
TriggerEvent('esx_status:onTick', GetStatusData(true))
Citizen.Wait(Config.TickTime)
```

How it should look like if you want to fix the ladderhud (lines 55-57):
```lua
TriggerEvent('esx_status:onTick', GetStatusData(true))
TriggerEvent('esx_ladderhud:updateBasics', GetStatusData(true)) -- add this line of code.
Citizen.Wait(Config.TickTime)
```
