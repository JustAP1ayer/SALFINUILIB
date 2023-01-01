# SALFINUILIB 
# Not made by me, made by https://github.com/slf0Dev

# Documents

```-- Library Core Loadstring
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/JustAP1ayer/SALFINUILIB/main/SALFINUILIB"))()

-- Creating Gui
local MainWindow = Library.Main("GuiName","KeyBind")

-- Creating Categories
local Category = MainWindow.Category("Your Text","ImageId","ImageScaleType",Image Transparency)


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
