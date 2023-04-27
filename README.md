local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()

local Window = Library.CreateLib("COPY Cframe | pee xhub", "GrapeTheme")

local Tab = Window:NewTab("Copy cframe")

local Section = Tab:NewSection("copy click ↓✓")

Section:NewButton("Copy cframe", "Click to copy thx", function()

    setclipboard(tostring(game.Players.LocalPlayer.Character.HumanoidRootPart.Position))

end)
