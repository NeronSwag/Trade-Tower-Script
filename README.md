
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local AutoFarm = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local AutoUpgrade = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local FakeKorblox = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local Credits = Instance.new("TextLabel")
local UICorner_5 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.ResetOnSpawn = false

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(62, 62, 62)
Frame.BackgroundTransparency = 0.200
Frame.Position = UDim2.new(0.0531622358, 0, 0.280834913, 0)
Frame.Size = UDim2.new(0, 276, 0, 209)

UICorner.Parent = Frame

AutoFarm.Name = "AutoFarm"
AutoFarm.Parent = Frame
AutoFarm.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
AutoFarm.Position = UDim2.new(0.137681156, 0, 0.095693782, 0)
AutoFarm.Size = UDim2.new(0, 200, 0, 30)
AutoFarm.Font = Enum.Font.SciFi
AutoFarm.Text = "Autofarm"
AutoFarm.TextColor3 = Color3.fromRGB(255, 255, 255)
AutoFarm.TextScaled = true
AutoFarm.TextSize = 14.000
AutoFarm.TextWrapped = true

UICorner_2.Parent = AutoFarm

AutoUpgrade.Name = "AutoUpgrade"
AutoUpgrade.Parent = Frame
AutoUpgrade.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
AutoUpgrade.Position = UDim2.new(0.137681156, 0, 0.287081361, 0)
AutoUpgrade.Size = UDim2.new(0, 200, 0, 30)
AutoUpgrade.Font = Enum.Font.SciFi
AutoUpgrade.Text = "AutoUpgrade"
AutoUpgrade.TextColor3 = Color3.fromRGB(255, 255, 255)
AutoUpgrade.TextScaled = true
AutoUpgrade.TextSize = 14.000
AutoUpgrade.TextWrapped = true

UICorner_3.Parent = AutoUpgrade

FakeKorblox.Name = "FakeKorblox"
FakeKorblox.Parent = Frame
FakeKorblox.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
FakeKorblox.Position = UDim2.new(0.137681156, 0, 0.478468925, 0)
FakeKorblox.Size = UDim2.new(0, 200, 0, 30)
FakeKorblox.Font = Enum.Font.SciFi
FakeKorblox.Text = "Fake Korblox"
FakeKorblox.TextColor3 = Color3.fromRGB(255, 255, 255)
FakeKorblox.TextScaled = true
FakeKorblox.TextSize = 14.000
FakeKorblox.TextWrapped = true

UICorner_4.Parent = FakeKorblox

Credits.Name = "Credits"
Credits.Parent = Frame
Credits.BackgroundColor3 = Color3.fromRGB(62, 62, 62)
Credits.BackgroundTransparency = 0.300
Credits.Position = UDim2.new(0, 0, 0.760765553, 0)
Credits.Size = UDim2.new(0, 276, 0, 50)
Credits.Font = Enum.Font.Cartoon
Credits.Text = "Simple script made by Neron#1111 | join discord.gg/dhc :3"
Credits.TextColor3 = Color3.fromRGB(255, 255, 255)
Credits.TextScaled = true
Credits.TextSize = 14.000
Credits.TextWrapped = true

UICorner_5.Parent = Credits

-- Scripts:

local function TTZAL_fake_script() -- AutoFarm.LocalScript 
	local script = Instance.new('LocalScript', AutoFarm)

	AutoFarm.MouseButton1Down:connect(function()
		getgenv().autofarm = true
	
		while getgenv().autofarm do wait()
			game:GetService("ReplicatedStorage").Events.Click:FireServer("Click")
		end)
end
coroutine.wrap(TTZAL_fake_script)()
local function JXEQDC_fake_script() -- AutoUpgrade.LocalScript 
	local script = Instance.new('LocalScript', AutoUpgrade)

	AutoUpgrade.MouseButton1Down:connect(function()
		getgenv().autoupgrade = true
	
		while getgenv().autoupgrade do wait()
		game:GetService("ReplicatedStorage").Events.StoreActions:InvokeServer("Upgrade")
	end)
	
end
coroutine.wrap(JXEQDC_fake_script)()
local function CNZIML_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	script.Parent.Selectable = true
	script.Parent.Active = true
	script.Parent.Draggable = true
end
coroutine.wrap(CNZIML_fake_script)()
