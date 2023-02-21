# SALFINUILIB 
# Not made by me, made by https://github.com/slf0Dev

# Documents

Slider and Slider2 is different as Slider works after you finish sliding but Slider2 is a calling script, which it would always update when sliding

```-- Library Core Loadstring
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/JustAP1ayer/SALFINUILIB/main/SALFINUILIB"))()

-- Creating Gui
local MainWindow = Library.Main("GuiName","KeyBind")

-- Creating Categories
local Category = MainWindow.Category("Your Text","ImageId","ImageScaleType","Image Transparency")


--[[
ImageScaleTypes : "Crop" , "Fit" , "Slice" , "Stretch"
]]

-- Creating Folders
local Folder = Category.Folder("TemplateFolder")

-- Creating Components

-- Creating Labels
local Label = Folder.Label("Your Text")

-- Creating Buttons
local Button = Folder.Button("Your Text",function()
print("Pressed")
-- Code Here
end)

-- Creating Toggles
local Toggle = Folder.Toggle("Your Text",function(bool)
print(bool)
end,DefaultBoolValue)

-- Creating Sliders
local Slider = Folder.Slider("Your Text",min,max,function(value)
print(value)
end,DefaultValue,isFloat) --isFloat is boolean

-- Creating Slider2s
local Slider2 = Folder.Slider2("Your Text",min,max,function(value)
print(value)
end,DefaultValue,isFloat) --isFloat is boolean

-- Creating Dropdowns
local Dropdown = Folder.Dropdown("Placeholder for dropdown", false)
Dropdown.Choice("text", function()
-- Put a Choice Here
-- code
end, false)
```



Example


```-- Library Core Loadstring
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/JustAP1ayer/SALFINUILIB/main/SALFINUILIB"))()

-- Creating Gui
local MainWindow = Library.Main("Test","LeftAlt")

-- Creating Categories
local Category = MainWindow.Category("Test","1","Crop","1")

-- Creating Folders
local Folder = Category.Folder("Test")

-- Creating Components

-- Creating Labels
local Label = Folder.Label("Test")

-- Creating Buttons
local Button = Folder.Button("AntiAfk",function()
wait(0.5)
local bb=game:service'VirtualUser'
game:service'Players'.LocalPlayer.Idled:connect(function()
bb:CaptureController()
bb:ClickButton2(Vector2.new())
end)
print("Antiafk ON")
end)

-- Creating Toggles
local Toggle = Folder.Toggle("3d rendering",function(bool)
game:GetService("RunService"):Set3dRenderingEnabled(bool)
end,true)

-- Creating Sliders
local Slider = Folder.Slider("walkspeed",1,200,function(value)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
end,16,isFloat) --isFloat is boolean

-- Creating Slider2s
local Slider2 = Folder.Slider2("walkspeed",1,200,function(value)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
end,16,isFloat) --isFloat is boolean

-- Creating Dropdowns

local Dropdown = Folder.Dropdown("What Choice did you choose", false)
Dropdown.Choice("Choice1", function()
  print("Choice1 was selected.")
end, false)
  Dropdown.Choice("Choice2", function()
  print("Choice2 was selected.")
end, false)

```

