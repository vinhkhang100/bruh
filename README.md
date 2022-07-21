local haha = game.Workspace.Gems:GetDescendants()
local safePlace 





local function kill(player)
	local args = {
		[1] = player.UserId
	}
	
	game:GetService("ReplicatedStorage").Events.Weapons.KnifeSwing:FireServer(unpack(args))
end
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("murder party hax", "DarkTheme")
local Game = Window:NewTab("Game")
local MurderP = Game:NewSection("Murder Party")
local AutoF = false
local AutoFTele = false
local ExpFarm = false
local Creditse = Window:NewTab("Credits")
local Credits = Creditse:NewSection("Haha yes")
Credits:NewLabel("bianhquan12345: Tester and helper")
Credits:NewLabel("vinhkhang100: Others")
Credits:NewButton("Copy discord link", "fuck (:", function ()
	setclipboard("https://discord.gg/yEBheZxfN7")
end)
local value = Instance.new("NumberValue",game.Workspace)
value.Name = "CheckT"

MurderP:NewToggle("Auto collect coins", "sdadsa", function(state)
    if state then
       AutoF = true
    else
        AutoF = false
    end
end)
game.Workspace.Time.Changed:Connect(function()
	if game.Workspace.Time.Value == 119 then
		
safePlace = Instance.new("Part",game.Workspace)
safePlace.Anchored = true
safePlace.Size = Vector3.new(6,1,6)
safePlace.CFrame = CFrame.new(game.Players.LocalPlayer.character.HumanoidRootPart.Position) + Vector3.new(0,150,0)

if AutoF == true then
	game.Players.LocalPlayer.character.HumanoidRootPart.CFrame = CFrame.new(safePlace.Position)+Vector3.new(0,4,0)
repeat
			for i,v in pairs(game.Workspace.Gems:GetDescendants()) do
				if v.Name == "TouchInterest" then
				firetouchinterest(game.Players.LocalPlayer.Character.Head, v.Parent,0)
				wait()
				end
				end
until game.Players.LocalPlayer.MatchCurrency.Value == 15



	end
end
end)
local InfJUmp = false
MurderP:NewToggle("Inf jump", "haha yes?", function(state)
    if state then
        InfJUmp = true
    else
       InfJUmp = false
    end
end)
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfJUmp == true then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
MurderP:NewButton("Teleport to map", "you only need this if you want to go out the safe place", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(12, 1210, 43)
end)
MurderP:NewButton("Teleport to safe place", "haha yes", function ()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(safePlace.Position) + Vector3.new(0,3,0)
end)
MurderP:NewButton("Collect coins", "this will auto collect coins for u", function()
	for i,v in pairs(game.Workspace.Gems:GetDescendants()) do
		if v.Name == "TouchInterest" then
		firetouchinterest(game.Players.LocalPlayer.Character.Head, v.Parent,0)
		wait(0.05)
		firetouchinterest(game.Players.LocalPlayer.Character.Head, v.Parent,1)
		end
		end

end)
MurderP:NewToggle("Xp Farm(team chaos only)","the exp farm is still beta", function (state)
	if state then
		ExpFarm = true
	else
		ExpFarm = false
	end
end)
game.Workspace.Time.Changed:Connect(function ()
	if game.Workspace.Time.Value == 119 then
		if ExpFarm == true then
			game.Players.LocalPlayer.character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack["0"])

		end
	end
end)
local noclip = false
 game:GetService("RunService").Stepped:Connect(function()
if noclip then
    game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
end
    end)

MurderP:NewButton("Esp", "haha yes", function()

--- Tut

local esp_settings = { ---- table for esp settings 
    textsize = 8,
    colour = 255,255,255
}

local gui = Instance.new("BillboardGui")
local esp = Instance.new("TextLabel",gui) ---- new instances to make the billboard gui and the textlabel



gui.Name = "Cracked esp"; ---- properties of the esp
gui.ResetOnSpawn = false
gui.AlwaysOnTop = true;
gui.LightInfluence = 0;
gui.Size = UDim2.new(1.75, 0, 1.75, 0);
esp.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
esp.Text = ""
esp.Size = UDim2.new(0.0001, 0.00001, 0.0001, 0.00001);
esp.BorderSizePixel = 4;
esp.BorderColor3 = Color3.new(esp_settings.colour)
esp.BorderSizePixel = 0
esp.Font = "GothamSemibold"
esp.TextSize = esp_settings.textsize
esp.TextColor3 = Color3.fromRGB(esp_settings.colour)

game:GetService("RunService").RenderStepped:Connect(function() 
    for i,v in pairs (game:GetService("Players"):GetPlayers()) do
        if v ~= game:GetService("Players").LocalPlayer and v.Character.Head:FindFirstChild("Cracked esp")==nil  then
            esp.Text = "{"..v.Name.."}"
            gui:Clone().Parent = v.Character.Head
    end
end
end)
game.Players.PlayerAdded:Connect(function()

--- Tut

local esp_settings = { ---- table for esp settings 
    textsize = 8,
    colour = 255,255,255
}

local gui = Instance.new("BillboardGui")
local esp = Instance.new("TextLabel",gui) ---- new instances to make the billboard gui and the textlabel



gui.Name = "Cracked esp"; ---- properties of the esp
gui.ResetOnSpawn = false
gui.AlwaysOnTop = true;
gui.LightInfluence = 0;
gui.Size = UDim2.new(1.75, 0, 1.75, 0);
esp.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
esp.Text = ""
esp.Size = UDim2.new(0.0001, 0.00001, 0.0001, 0.00001);
esp.BorderSizePixel = 4;
esp.BorderColor3 = Color3.new(esp_settings.colour)
esp.BorderSizePixel = 0
esp.Font = "GothamSemibold"
esp.TextSize = esp_settings.textsize
esp.TextColor3 = Color3.fromRGB(esp_settings.colour)

game:GetService("RunService").RenderStepped:Connect(function() 
    for i,v in pairs (game:GetService("Players"):GetPlayers()) do
        if v ~= game:GetService("Players").LocalPlayer and v.Character.Head:FindFirstChild("Cracked esp")==nil  then
            esp.Text = "{"..v.Name.."}"
            gui:Clone().Parent = v.Character.Head
    end
end
end)
end)
end)
local currentSpeed = game.Players.LocalPlayer.character.Humanoid.WalkSpeed
local currentJump = game.Players.LocalPlayer.character.Humanoid.JumpPower
MurderP:NewSlider("Walkspeed", "fsasadads", 95, 16, function(s) 
    currentSpeed = s
end)
MurderP:NewSlider("JumpPower", "fsasadads", 299, 50, function(s) 
    currentJump = s
end)
while wait() do
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = currentSpeed
	game.Players.LocalPlayer.Character.Humanoid.JumpPower = currentJump
end

