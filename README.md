# Mato UI library!

Loadstring
```lua
local MatoUI = loadstring(game:HttpGet("https://raw.githubusercontent.com/Itzzavi335/Mato-Ui-Library/refs/heads/main/Source.luau"))()
```

Create Window Here:
```lua
local Window = MatoUI:CreateWindow({
    Title = "Mato Hub",
    Subtitle = "Best script ever",
    Size = UDim2.new(0, 600, 0, 450)
})
```

Badges:
```lua
Window:AddBadge("BETA", Color3.fromRGB(255, 165, 0))
Window:AddBadge("VIP", Color3.fromRGB(255, 215, 0), Color3.fromRGB(0,0,0))
-- Syntax: Window:AddBadge("Text", BackgroundColor, TextColor optional)
```

Information ( basically Label but Improved ):
```lua
MainTab:AddInformation({
    Title = "Info",
    Message = "Message here!"
})
```

Warning ( To warn users ):
```lua
MainTab:AddWarning({
    Title = "WARNING",
    Message = "Using speed hacks can get you banned on some games! ( example )"
})
```

AddTab:
```lua
local MainTab   = Window:AddTab("Main")
```
AddButton:
```lua
MainTab:AddButton({
    Name = "Button name here",
    Callback = function()
        -- code here
    end
})
```

AddDialogueButton:
```lua
MainTab:AddDialogueMessage({
    Name = "Show Credits",
    Title = "Credits",
    Message = "Made with love by you <3",
    Callback = function() end -- fires when OK is pressed
})
```

AddToggle:
```lua
MainTab:AddToggle({
    Name = "Name here",
    Default = false, -- make true to activate
    Callback = function(state)
        -- code here
    end
})
```

```
AddSlider: No Mobile support, sorry!
```lua
MainTab:AddSlider({
    Name = "WalkSpeed",
    Min = 16,
    Max = 300,
    Default = 16,
    Callback = function(value)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
    end
})
```

AddDialogueDropdown:
```lua
MainTab:AddDialogueDropdown({
    Name = "Choose Weapon",
    Title = "Weapon Selector",
    Message = "Pick your weapon below:",
    Options = {"Sword", "Gun", "Knife", "Flamethrower", "Rocket Launcher"},
    Callback = function(selected)
        print("You selected:", selected)
    end
})
```

AddDropdown:
```lua
MainTab:AddDropdown({
    Name = "Select Features",
    Options = {"Fly", "Noclip", "Infinite Yield", "ESP", "Aimbot"},
    Multi = true,
    Default = {"Fly", "ESP"},  -- you can pre-select multiple
    Callback = function(selected)
        print("Currently enabled features:", table.concat(selected, " | "))
    end
})
```
