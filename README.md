

	local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
	local Window = Library.CreateLib("Tds hub", "BloodTheme")
	local Lobby = Window:NewTab("Game")
	local AutoChain = Lobby:NewSection("AutoChain")
	local turn = false
	AutoChain:NewToggle("AutoChain", "Make sure u have at least 3 lv 2 plus commanders", function(state)
		if state then
			turn = true
			print("lolok")
			while state do
				for index,value in pairs(game.Workspace.Towers:GetChildren()) do
					if value.Owner.Value == game.Players.LocalPlayer and value.Replicator:GetAttribute("Type") == "Commander" then
						local args = {
							[1] = "Troops",
							[2] = "Abilities",
							[3] = "Activate",
							[4] = {
								["Name"] = "Call Of Arms",
								["Troop"] = value
							}
						}

						game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args))
						wait(10.1)
					end
				end
				wait()
			end 
		else
			turn = false
			print("ok")
		end
	end)


	local Stack = Lobby:NewSection("Stack")
	Stack:NewTextBox("TowerNameHere", "Make sure u stand in the position u want to place", function(txt)
		local args = {
			[1] = "Troops",
			[2] = "Place",
			[3] = txt,
			[4] = {
				["Rotation"] = CFrame.new(0,5,0,0,5,0,0,5,0,0,5,0),
				["Position"] = game.Players.LocalPlayer.character.HumanoidRootPart.Position - Vector3.new(0,5,0)
			}
		}

		game:GetService("ReplicatedStorage").RemoteFunction:InvokeServer(unpack(args))
	end)
	local Lobbyl = Window:NewTab("Lobby")
	local LeaderBoard = Lobbyl:NewSection("LeaderBoard")
	LeaderBoard:NewButton("Update leader board", "This will update the leader board", function()

		local A_1 = "Leaderboard"
		local A_2 = "Request"
		local Event = game:GetService("ReplicatedStorage").RemoteFunction
		Event:InvokeServer(A_1, A_2)

	end)
	local Selling = Lobby:NewSection("Selling")
	Selling:NewButton("Sell all towers", "ok", function()
		for index,value in pairs(game.Workspace.Towers:GetChildren()) do
			-- Script generated by R2Sv2
			-- R2Sv2 developed by Luckyxero

			local A_1 = "Troops"
			local A_2 = "Sell"
			local A_3 = 
				{
					["Troop"] = value 
				}
			local Event = game:GetService("ReplicatedStorage").RemoteFunction
			Event:InvokeServer(A_1, A_2, A_3)

		end
		wait()
	end)


	Selling:NewTextBox("SellAllTowersName", "ok", function(txt)
		for index,value in pairs(game.Workspace.Towers:GetChildren()) do
			if value.Replicator:GetAttribute("Type") == txt then



				local A_1 = "Troops"
				local A_2 = "Sell"
				local A_3 = 
					{
						["Troop"] = value 
					}
				local Event = game:GetService("ReplicatedStorage").RemoteFunction
				Event:InvokeServer(A_1, A_2, A_3)
			end
			wait()
		end


	end)
	Stack:NewButton("Place weird ace pilot", "This is only work for some map", function()
		local A_1 = "Troops"
		local A_2 = "Place"
		local A_3 = "Ace Pilot"
		local A_4 = 
			{
				["Rotation"] = CFrame.new(0,5,0,0,0,0,0,0,0,0,-90,-90),
				["Position"] = game.Players.LocalPlayer.character.HumanoidRootPart.Position - Vector3.new(0,5,0)
			}
		local Event = game:GetService("ReplicatedStorage").RemoteFunction
		Event:InvokeServer(A_1, A_2, A_3, A_4)
	end)
	Stack:NewButton("Place weird pursuit", "Same as the ace pilot", function()
		local A_1 = "Troops"
		local A_2 = "Place"
		local A_3 = "Pursuit"
		local A_4 = 
			{
				["Rotation"] = CFrame.new(0,5,0,0,0,0,0,0,0,0,-90,-90), 
				["Position"] = game.Players.LocalPlayer.character.HumanoidRootPart.Position - Vector3.new(0,5,0)
			}
		local Event = game:GetService("ReplicatedStorage").RemoteFunction
		Event:InvokeServer(A_1, A_2, A_3, A_4)
	end)
    Stack:NewButton("Place weird ace pilot2", "For lay by i guess lol", function()
		local A_1 = "Troops"
		local A_2 = "Place"
		local A_3 = "Ace Pilot"
		local A_4 = 
			{
				["Rotation"] = CFrame.new(0,5,0,0,0,90,-90), 
				["Position"] = game.Players.LocalPlayer.character.HumanoidRootPart.Position - Vector3.new(0,5,0)
			}
		local Event = game:GetService("ReplicatedStorage").RemoteFunction
		Event:InvokeServer(A_1, A_2, A_3, A_4)
	end)
    Stack:NewButton("Place weird pursuit2", "For lay by i guess lol", function()
		local A_1 = "Troops"
		local A_2 = "Place"
		local A_3 = "Pursuit"
		local A_4 = 
			{
				["Rotation"] = CFrame.new(0,5,0,0,0,90,-90), 
				["Position"] = game.Players.LocalPlayer.character.HumanoidRootPart.Position - Vector3.new(0,5,0)
			}
		local Event = game:GetService("ReplicatedStorage").RemoteFunction
		Event:InvokeServer(A_1, A_2, A_3, A_4)
	end)

Stack:NewDropdown("StackTower", "Alt of stack tower name", {"Scout", "Sniper", "Demoman","Freezer","Hunter","Ace Pilot","Medic", "Farm", "Militant","Shotgunner","Military Base","Electroshocker", "Commander","DJ Booth", "Soldier","Pyromancer","Rocketeer","Minigunner","Ranger","Accelerator","Engineer","Crook Boss","Turret","Mortar","Pursuit","Cowboy","Gladiator","Commando","Slasher","Frost Blaster","Swarmer","Toxic Gunner", "Sledger" , "Executioner","Archer","Mecha Base"}, function(currentOption)
    local A_1 = "Troops"
		local A_2 = "Place"
		local A_3 = currentOption
		local A_4 = 
			{
				["Rotation"] = CFrame.new(0,5,0), 
				["Position"] = game.Players.LocalPlayer.character.HumanoidRootPart.Position - Vector3.new(0,5,0)
			}
		local Event = game:GetService("ReplicatedStorage").RemoteFunction
		Event:InvokeServer(A_1, A_2, A_3, A_4)
end)



