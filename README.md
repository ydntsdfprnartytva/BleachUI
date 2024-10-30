## Create Window
```lua
local debris = game:GetService("Debris")
local contentProvider = game:GetService("ContentProvider")
local scriptContext = game:GetService("ScriptContext")
local players = game:GetService("Players")
local tweenService = game:GetService("TweenService")
local statsService = game:GetService("Stats")
local runService = game:GetService("RunService")
local userInputService = game:GetService("UserInputService")
local replicatedStorage = game:GetService("ReplicatedStorage")
local httpService = game:GetService("HttpService")
local starterGui = game:GetService("StarterGui")

if not isfolder("bleachhack") then
	makefolder("bleachhack")
end

local ping = 0
local fps = 0

local Lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/devdoroz/bleachhack-ui-lib/main/zmacsploitsynchrousfix.lua"))()
local UI = Lib:Create()
```
## Configs Settings
```lua
local configSavingUI = game:GetObjects("rbxassetid://18187656247")[1]:Clone()
configSavingUI.Parent = (gethui and gethui()) or game:GetService("CoreGui")
configSavingUI.Enabled = false
```
## Create Tab
```lua
local tab1 = UI:CreateCategory("Catching", "")
```
## Create Module
```lua
local mag1 = tab1:CreateModule("Magnets")
```
## Create Dropdown
```lua
local magType = mag1:CreateSwitch({
	Title = "Type",
	Range = {"Blatant", "Legit", "League", "Custom"}
})
```
## Create Slider
```
local magrange = mag1:CreateSlider({
    Title = "Radius",
    Range = {0, 25},
    Callback = function(v)
        print(v)
    end,
})
```
## Create Toggle
```lua
local magToggle = mag1:CreateToggle({Title = "Textures", Callback = function(v)
    print(v)
end,})
```
