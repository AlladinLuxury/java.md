if game.PlaceId == 2753915549 then

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local shift = Instance.new("TextButton")

local f9 = Instance.new("TextButton")

local delete = Instance.new("TextButton")

local shift4 = Instance.new("TextButton")

local main = Instance.new("ScreenGui")

local pon = Instance.new("ScreenGui")

local vis = Instance.new("TextButton")

local rj = Instance.new("TextButton")

pon.Parent = game.CoreGui

pon.Name = "Pons"

pon.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

main.Name = "Main"

main.Parent = game.CoreGui

main.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

shift.Name = "shift"

shift.Parent = main

shift.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

shift.BorderSizePixel = 1

shift.BorderColor3 = Color3.fromRGB(255, 160, 30)

shift.Position = UDim2.new(0.200683122, 0, 0, 0)

shift.Size = UDim2.new(0, 50, 0, 50)

shift.Font = Enum.Font.PermanentMarker

shift.Text = "Shift"

shift.TextColor3 = Color3.fromRGB(255, 160, 30)

shift.TextSize = 20.000

shift.TextWrapped = true

shift.MouseButton1Click:Connect(function()

	game:GetService("VirtualInputManager"):SendKeyEvent(true, "RightShift" ,false ,game)end)

f9.Name = "f9"

f9.Parent = main

f9.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

f9.BorderSizePixel = 1

f9.BorderColor3 = Color3.fromRGB(255, 160, 30)

f9.Position = UDim2.new(0.240683122, 0, 0, 0)

f9.Size = UDim2.new(0, 50, 0, 50)

f9.Font = Enum.Font.PermanentMarker

f9.Text = "f9"

f9.TextColor3 = Color3.fromRGB(255, 160, 30)

f9.TextSize = 35.000

f9.TextWrapped = true

f9.MouseButton1Click:Connect(function()

	game:GetService("VirtualInputManager"):SendKeyEvent(true, "F9" ,false ,game)

end)

delete.Name = "delete"

delete.Parent = main

delete.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

delete.BorderSizePixel = 1

delete.BorderColor3 = Color3.fromRGB(255, 160, 30)

delete.Position = UDim2.new(0.280683122, 0, 0, 0)

delete.Size = UDim2.new(0, 50, 0, 50)

delete.Font = Enum.Font.PermanentMarker

delete.Text = "DEL"

delete.TextColor3 = Color3.fromRGB(255, 160, 30)

delete.TextSize = 35.000

delete.TextWrapped = true

delete.MouseButton1Click:Connect(function()

	main:Destroy()

	pon:Destroy()

end)

vis.Name = "Hide"

vis.Parent = pon

vis.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

vis.BorderSizePixel = 1

vis.BorderColor3 = Color3.fromRGB(255, 160, 30)

vis.Position = UDim2.new(0.320683122, 0, 0, 0)

vis.Size = UDim2.new(0, 50, 0, 50)

vis.Font = Enum.Font.PermanentMarker

vis.Text = "HIDE"

vis.TextColor3 = Color3.fromRGB(255, 160, 30)

vis.TextSize = 20.000

vis.TextWrapped = true

vis.MouseButton1Click:Connect(function()

local maine = game.CoreGui.Main.shift

local del = game.CoreGui.Main.delete

local f9 = game.CoreGui.Main.f9

local rj = game.CoreGui.Main.rj

if maine.Visible == false then

maine.Visible = true

f9.Visible = true

del.Visible = true

rj.Visible = true

		else

			maine.Visible = false

            f9.Visible = false

            del.Visible = false

            rj.Visible = false

		end

end)

rj.Name = "rj"

rj.Parent = main

rj.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

rj.BorderSizePixel = 1

rj.BorderColor3 = Color3.fromRGB(255, 160, 30)

rj.Position = UDim2.new(0.240683122, 0, 0, 0)

rj.Size = UDim2.new(0, 50, 0, 50)

rj.Font = Enum.Font.PermanentMarker

rj.Text = "RJ"

rj.TextColor3 = Color3.fromRGB(255, 160, 30)

rj.TextSize = 35.000

rj.TextWrapped = true

rj.MouseButton1Click:Connect(function()

	if #game.Players:GetPlayers() == 1 then

		game.Players.LocalPlayer:Kick("\nRejoin...")

		wait()

		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)

	else

		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)

	end

end)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local OrionLib = loadstring(game:HttpGet(('https://pastebin.com/raw/NDL9HYmx')))()

local Window = OrionLib:MakeWindow({Name = "PoistHub • Sea1", HidePremium = false, SaveConfig = true, ConfigFolder = "PoistHub"})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Значения

_G.killaura = true

_G.autochest1 = true

_G.autochest2 = true

_G.autochest3 = true

_G.hitbox = true

_G.automelee = true

_G.autodefense = true

_G.autosword = true

_G.autogun = true

_G.autodevil = true

_G.autorace = true

_G.autobuso = true

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Функции

if game.PlaceId == 2753915549 then

World1 = true

elseif game.PlaceId == 4442272183 then

World2 = true

elseif game.PlaceId == 7449423635 then

World3 = true

end

function isnil(thing)

return (thing == nil)

end

local function round(n)

return math.floor(tonumber(n) + 0.5)

end

function UpdateEspPlayer()

if ESPPlayer then

for i,v in pairs(game:GetService("Players"):GetPlayers()) do

if not isnil(v.Character) then

if not v.Character.Head:FindFirstChild('NameEsp'..v.Name) then

local BillboardGui = Instance.new("BillboardGui")

local ESP = Instance.new("TextLabel")

local HealthESP = Instance.new("TextLabel")

BillboardGui.Parent = v.Character.Head

BillboardGui.Name = 'NameEsp'..v.Name

BillboardGui.ExtentsOffset = Vector3.new(0, 1, 0)

BillboardGui.Size = UDim2.new(1,200,1,30)

BillboardGui.Adornee = v.Character.Head

BillboardGui.AlwaysOnTop = true

ESP.Name = "ESP"

ESP.Parent = BillboardGui

ESP.TextTransparency = 0

ESP.BackgroundTransparency = 1

ESP.Size = UDim2.new(0, 200, 0, 30)

ESP.Position = UDim2.new(0,25,0,0)

ESP.Font = Enum.Font.Gotham

ESP.Text = (v.Name ..' '.."[ "..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M'.." ]")

if v.Team == game:GetService("Players").LocalPlayer.Team then

ESP.TextColor3 = Color3.new(255, 160, 30)

else

ESP.TextColor3 = Color3.new(255, 120,30)

end

ESP.TextSize = 14

ESP.TextStrokeTransparency = 0.500

ESP.TextWrapped = true

HealthESP.Name = "HealthESP"

HealthESP.Parent = ESP

HealthESP.TextTransparency = 0

HealthESP.BackgroundTransparency = 1

HealthESP.Position = ESP.Position + UDim2.new(0, -25, 0, 15)

HealthESP.Size = UDim2.new(0, 200, 0, 30)

HealthESP.Font = Enum.Font.Gotham

HealthESP.TextColor3 = Color3.fromRGB(255, 0, 0)

HealthESP.TextSize = 14

HealthESP.TextStrokeTransparency = 0.500

HealthESP.TextWrapped = true

HealthESP.Text = "Level"..v.Data.Level.Value.."Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)

else

v.Character.Head['NameEsp'..v.Name].ESP.Text = (v.Name ..' '..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')

v.Character.Head['NameEsp'..v.Name].ESP.HealthESP.Text = "Level"..v.Data.Level.Value.."Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)

v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 0

v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 0

end

end

end

else

for i,v in pairs(game:GetService("Players"):GetPlayers()) do

if v.Character.Head:FindFirstChild('NameEsp'..v.Name) then

v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 1

v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextStrokeTransparency = 1

v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 1

v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextStrokeTransparency = 1

end

end

end

end

function UpdateIslandESP()

for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do

pcall(function()

if IslandESP then

if v.Name ~= "Sea" then

if not v:FindFirstChild('NameEsp') then

local bill = Instance.new('BillboardGui',v)

bill.Name = 'NameEsp'

bill.ExtentsOffset = Vector3.new(0, 1, 0)

bill.Size = UDim2.new(1,200,1,30)

bill.Adornee = v

bill.AlwaysOnTop = true

local name = Instance.new('TextLabel',bill)

name.Font = "GothamBold"

name.FontSize = "Size14"

name.TextWrapped = true

name.Size = UDim2.new(1,0,1,0)

name.TextYAlignment = 'Top'

name.BackgroundTransparency = 1

name.TextStrokeTransparency = 0.5

name.TextColor3 = Color3.fromRGB(80, 245, 245)

else

v['NameEsp'].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')

end

end

else

if v:FindFirstChild('NameEsp') then

v:FindFirstChild('NameEsp'):Destroy()

end

end

end)

end

end

function UpdateChestEsp()

for i,v in pairs(game:GetService("Workspace"):GetChildren()) do

pcall(function()

if string.find(v.Name,"Chest") then

if ChestESP then

if string.find(v.Name,"Chest") then

if not v:FindFirstChild('NameEsp'..Number) then

local bill = Instance.new('BillboardGui',v)

bill.Name = 'NameEsp'..Number

bill.ExtentsOffset = Vector3.new(0, 1, 0)

bill.Size = UDim2.new(1,200,1,30)

bill.Adornee = v

bill.AlwaysOnTop = true

local name = Instance.new('TextLabel',bill)

name.Font = "GothamBold"

name.FontSize = "Size14"

name.TextWrapped = true

name.Size = UDim2.new(1,0,1,0)

name.TextYAlignment = 'Top'

name.BackgroundTransparency = 1

name.TextStrokeTransparency = 0.5

name.TextColor3 = Color3.fromRGB(255, 160, 30)

if v.Name == "Chest1" then

name.Text = ("Silver Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')

end

if v.Name == "Chest2" then

name.Text = ("Gold Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')

end

if v.Name == "Chest3" then

name.Text = ("Diamond Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')

end

else

v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')

end

end

else

if v:FindFirstChild('NameEsp'..Number) then

v:FindFirstChild('NameEsp'..Number):Destroy()

end

end

end

end)

end

end

function UpdateBfEsp()

for i,v in pairs(game:GetService("Workspace"):GetChildren()) do

pcall(function()

if DevilFruitESP then

if string.find(v.Name, "Fruit") then

if not v.Handle:FindFirstChild('NameEsp'..Number) then

local bill = Instance.new('BillboardGui',v.Handle)

bill.Name = 'NameEsp'..Number

bill.ExtentsOffset = Vector3.new(0, 1, 0)

bill.Size = UDim2.new(1,200,1,30)

bill.Adornee = v.Handle

bill.AlwaysOnTop = true

local name = Instance.new('TextLabel',bill)

name.Font = "GothamBold"

name.FontSize = "Size14"

name.TextWrapped = true

name.Size = UDim2.new(1,0,1,0)

name.TextYAlignment = 'Top'

name.BackgroundTransparency = 1

name.TextStrokeTransparency = 0.5

name.TextColor3 = Color3.fromRGB(255, 160, 30)

name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')

else

v.Handle['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')

end

end

else

if v.Handle:FindFirstChild('NameEsp'..Number) then

v.Handle:FindFirstChild('NameEsp'..Number):Destroy()

end

end

end)

end

end

function topos(Pos)

Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude

if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end

pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/210, Enum.EasingStyle.Linear),{CFrame = Pos}) end)

tween:Play()

if Distance <= 250 then

tween:Cancel()

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos

end

if _G.StopTween == true then

tween:Cancel()

_G.Clip = false

end

end

function toClipboard(String)

	local clipBoard = setclipboard or toclipboard or set_clipboard or (Clipboard and Clipboard.set)

	if clipBoard then

		clipBoard(String)

	end

end

local jobId = ''..game.JobId..''

toClipboard(jobId..' если вылетит, вставьте в Join Server этот айди')

	

function getPlayerByNick(nick:string)

    local firstTry;

    local secondTry;

    local thirdTry;

    local fourthTry;

    nick = string.lower(nick)

    local playerList = game.Players:GetPlayers()

    for _,plr in pairs(playerList) do

        if string.lower(plr.Name) == nick then

            firstTry = plr

            break

        end

    end

    for _,plr in pairs(playerList) do

        if string.lower(plr.DisplayName) == nick then

            secondTry = plr

            break

        end

    end

    for _,plr in pairs(playerList) do

        if string.sub(string.lower(plr.Name), 1, #nick) == nick then

            thirdTry = plr

            break

        end

    end

    for _,plr in pairs(playerList) do

        if string.sub(string.lower(plr.DisplayName), 1, #nick) == nick then

            fourthTry = plr

            break

        end

    end

    return firstTry or nick == 'me' and game.Players.LocalPlayer or secondTry or thirdTry or fourthTry

end

function autobuso()

while _G.autobuso == true do

if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then

       game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")

       elseif game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then

print("Buso Activates")

wait(0.5)

end

end

end

function autorace()

while _G.autorace == true do

game:GetService("ReplicatedStorage").Remotes.CommE:FireServer("ActivateAbility")

wait(0.01)

end

end

function automelee()

while _G.automelee == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", 1)

wait(0.01)

end

end

function autodefense()

while _G.autodefense == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", 1)

wait(0.01)

end

end

function autosword()

while _G.autosword == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", 1)

wait(0.01)

end

end

function autogun()

while _G.autogun == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", 1)

wait(0.01)

end

end

function autodevil()

while _G.autodevil == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", 1)

wait(0.01)

end

end

function autochest1()

while _G.autochest1 == true do

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest1.CFrame

wait(0.01)

end

end

function autochest2()

while _G.autochest2 == true do

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest2.CFrame

wait(0.01)

end

end

function autochest3()

while _G.autochest3 == true do

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest3.CFrame

wait(0.01)

end

end

function killaura()

while _G.killaura == true do

for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do

    if enemy:FindFirstChild('HumanoidRootPart') then

z = enemy.UpperTorso

x = enemy.Head

x:Destroy()

z:Destroy()

wait(.0000001)

end

end

end

end

function hitbox()

while _G.hitbox == true do

for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do

    if enemy:FindFirstChild('HumanoidRootPart') then

local z = enemy.HumanoidRootPart

local x = enemy.Humanoid

        z.Size = Vector3.new(50,50,50)

        z.Shape = "Block"

        z.Transparency = 0.2

        z.Color = Color3.fromRGB(255,160,30)

        z.Material = "ForceField"

        z.CanCollide = false

        z.Anchored = true

        x.Sit = true

       wait(.000000000000001)

    end

end

end

end

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "",

	Icon = "",

	PremiumOnly = false

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Tools",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})

local a = game.Lighting

local c = Instance.new("ColorCorrectionEffect", a)

local e = Instance.new("ColorCorrectionEffect", a)

OldAmbient = a.Ambient

OldBrightness = a.Brightness

OldColorShift_Top = a.ColorShift_Top

OldBrightnessc = c.Brightness

OldContrastc = c.Contrast

OldTintColorc = c.TintColor

OldTintColore = e.TintColor

Tab:AddToggle({

	Name = "RTX",

	Default = false,

	Callback = function(Suka)

_G.RTXMode = Suka

if not _G.RTXMode then return end

while _G.RTXMode do wait()

a.Ambient = Color3.fromRGB(33, 33, 33)

a.Brightness = 0.3

c.Brightness = 0.176

c.Contrast = 0.39

c.TintColor = Color3.fromRGB(217, 145, 57)

game.Lighting.FogEnd = 999

if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("PointLight") then

local a2 = Instance.new("PointLight")

a2.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart

a2.Range = 15

a2.Color = Color3.fromRGB(217, 145, 57)

end

if not _G.RTXMode then

a.Ambient = OldAmbient

a.Brightness = OldBrightness

a.ColorShift_Top = OldColorShift_Top

c.Contrast = OldContrastc

c.Brightness = OldBrightnessc

c.TintColor = OldTintColorc

e.TintColor = OldTintColore

game.Lighting.FogEnd = 2500

game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("PointLight"):Destroy()

end

end

end

})

Tab:AddButton({

	Name = "Tp Tool" ,

	Callback = function()

local TpTool = Instance.new("Tool")

	TpTool.Name = "Teleport Tool"

	TpTool.RequiresHandle = false

	TpTool.Parent = game.Players.LocalPlayer.Backpack

	TpTool.Activated:Connect(function()

		local Char = game.Players.LocalPlayer.Character or workspace:FindFirstChild(game.Players.LocalPlayer.Name)

		local HRP = Char and Char:FindFirstChild("HumanoidRootPart")

		if not Char or not HRP then

			return warn("Failed to find HumanoidRootPart")

		end

		HRP.CFrame = CFrame.new(game.Players.LocalPlayer:GetMouse().Hit.X, game.Players.LocalPlayer:GetMouse().Hit.Y + 3, game.Players.LocalPlayer:GetMouse().Hit.Z, select(4, HRP.CFrame:components()))

	end)

end

})

Tab:AddButton({

	Name = "Tween Tp Tool" ,

	Callback = function()

local a = game:GetService("Players").LocalPlayer

            local b = Instance.new('Tool',a.Backpack)

            local g = game:GetService("TweenService")

            b.RequiresHandle = false

            b.Name = "TweenTp"

            b.Activated:connect(function()

            g:Create(

            a.Character:FindFirstChildOfClass("Humanoid").RootPart,

            TweenInfo.new(tonumber(2),Enum.EasingStyle.Linear),

            {CFrame = CFrame.new(a:GetMouse().Hit.Position+Vector3.new(0,5,0))}

            ):Play()

            end)

         end

})

Tab:AddButton({

	Name = "Remote Spy" ,

	Callback = function()

loadstring(game:HttpGet("https://github.com/exxtremestuffs/SimpleSpySource/raw/master/SimpleSpy.lua"))()

  	end    

})

Tab:AddButton({

	Name = "Dex V3" ,

	Callback = function()

loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/BypassedDarkDexV3.lua", true))()

  	end

})

Tab:AddButton({

	Name = "Dex V4" ,

	Callback = function()

    loadstring(game:HttpGet("https://raw.githubusercontent.com/peyton2465/Dex/master/out.lua"))()

  	end

})

Tab:AddButton({

	Name = "Big Jump" ,

	Callback = function()

    game.Players.LocalPlayer.PlayerGui.TouchGui.TouchControlFrame.JumpButton.Size = UDim2.new(0,200,0,200)

  	end    

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "BuyItem",

	Icon = "http://www.roblox.com/asset/?id=12496227758",

	PremiumOnly = false

})

local Section = Tab:AddSection({

	Name = "Abilities"

})

Tab:AddButton({

	Name = "Geppo 10.000$",

	Callback = function()

              game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Geppo")

  	end    

})

Tab:AddButton({

	Name = "Buso 25.000$",

	Callback = function()

      		 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Buso")

  	end    

})

Tab:AddButton({

	Name = "Soru 100.000$",

	Callback = function()

      		 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Soru")

  	end

})

Tab:AddButton({

	Name = "Ken 750.000$(need kill shanks)",

	Callback = function()

      		game:GetService("ReplicatedStorage").Remotes.CommE:FireServer("Ken",true)

  	end    

})

local Section = Tab:AddSection({

	Name = "Fighting Styles"

})

Tab:AddButton({

	Name = "Dark Step 250.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg" )

  	end    

})

Tab:AddButton({

	Name = "Electro 500.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro" )

  	end    

})

Tab:AddButton({

	Name = "Water Kung-Fu 750.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate" )

  	end    

})

Tab:AddButton({

	Name = "Dragon Breath",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")

  	end    

})

Tab:AddButton({

	Name = "Superhuman 3.000.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman" )

  	end    

})

Tab:AddButton({

	Name = "Death Step 2.500.000$ 2.500F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep" )

  	end    

})

Tab:AddButton({

	Name = "Electric Claw 2.500.000$ 2.500F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw" )

  	end    

})

Tab:AddButton({

	Name = "Sharkman Karate 2.500.000$ 2.500F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate" )

  	end    

})

Tab:AddButton({

	Name = "Dragon Talon 2.500.000$ 2.500F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon" )

  	end    

})

Tab:AddButton({

	Name = "Godhuman 5.000.000$ 5.000F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman" )

  	end    

})

local Section = Tab:AddSection({

	Name = "Fragments"

})

Tab:AddButton({

	Name = "Check Color Haki Dealer",

	Callback = function()

	OrionLib:MakeNotification({

	Name = "Haki Colors Dealer",

    Content = "".. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "1") .."",

	Image = "rbxassetid://4483345998",

	Time = 5

})

	end

})

Tab:AddButton({

	Name = "Buy Color Buso Haki",

	Callback = function()

	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "2")

	end

})

Tab:AddButton({

	Name = "Ghoul 0F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Ectoplasm","Change",4)

  	end    

})

Tab:AddButton({

	Name = "Cyborg 2.500F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CyborgTrainer","Buy")

  	end    

})

Tab:AddButton({

	Name = "Reset Stats 2.500F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")

  	end    

})

Tab:AddButton({

	Name = "Race Reroll 3.000F",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Reroll","2")

  	end    

})

local Section = Tab:AddSection({

	Name = "Bones"

})

Tab:AddButton({

	Name = "Surprise 50bones",

	Callback = function()

      		for i = 1, 10 do

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones", "Buy", 1, 1)

            end

  	end    

})

local Section = Tab:AddSection({

	Name = "Swords soon.."

})

local Section = Tab:AddSection({

	Name = "Guns soon.."

})

local Section = Tab:AddSection({

	Name = "Accessories soon.."

})

Tab:AddButton({

	Name = "Tomoe Ring 500.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Tomoe Ring")

end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Farming",

	Icon = "rbxassetid://12505503302",

	PremiumOnly = false

})

Tab:AddToggle({

	Name = "HitBox",

	Default = false,

	Callback = function(lolek)

	_G.hitbox = lolek

hitbox()

		end

})

local Section = Tab:AddSection({

    Name = "START"

})

Tab:AddButton({

	Name = "5Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)

end

})

local Section = Tab:AddSection({

    Name = "JUNGLE"

})

Tab:AddButton({

	Name = "10Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",1)

end

})

Tab:AddButton({

	Name = "15Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",2)

end

})

Tab:AddButton({

	Name = "20Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",3)    

end

})

local Section = Tab:AddSection({

    Name = "PIRATE VILLAGE"

})

Tab:AddButton({

	Name = "30Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",1)

end

})

Tab:AddButton({

	Name = "50Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",2)

end

})

Tab:AddButton({

	Name = "55Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",3)

end

})

local Section = Tab:AddSection({

    Name = "DESERT"

})

Tab:AddButton({

	Name = "60Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",1)

end

})

Tab:AddButton({

	Name = "75Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",2)

end

})

local Section = Tab:AddSection({

    Name = "SNOW VILLAGE"

})

Tab:AddButton({

	Name = "90Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 1)

end

})

Tab:AddButton({

	Name = "100Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 2)

end

})

Tab:AddButton({

	Name = "105Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 3)

end

})

local Section = Tab:AddSection({

    Name = "MARINE FORTRESS"

})

Tab:AddButton({

	Name = "120Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)

end

})

Tab:AddButton({

	Name = "130Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)

end

})

local Section = Tab:AddSection({

    Name = "SKY1"

})

Tab:AddButton({

	Name = "150Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",1)

end

})

Tab:AddButton({

	Name = "170Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",2)

end

})

local Section = Tab:AddSection({

    Name = "PRISON"

})

Tab:AddButton({

	Name = "190Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",1)

end

})

Tab:AddButton({

	Name = "210Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",2)

end

})

Tab:AddButton({

	Name = "220Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",1)

end

})

Tab:AddButton({

	Name = "230Lvl [BOS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",2)

end

})

Tab:AddButton({

	Name = "240Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",3)

end

})

local Section = Tab:AddSection({

    Name = "COLOSSEUM"

})

Tab:AddButton({

	Name = "250Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",1)

end

})

Tab:AddButton({

	Name = "275Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",2)

end

})

local Section = Tab:AddSection({

    Name = "MAGMA VILLAGE"

})

Tab:AddButton({

	Name = "300Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",1)

end

})

Tab:AddButton({

	Name = "325Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",2)

end

})

Tab:AddButton({

	Name = "350Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",3)

end

})

local Section = Tab:AddSection({

    Name = "UNDERWATER"

})

Tab:AddButton({

	Name = "375Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",1)

end

})

Tab:AddButton({

	Name = "400Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",2)

end

})

Tab:AddButton({

	Name = "425Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",3)

end

})

local Section = Tab:AddSection({

    Name = "SKY2-3"

})

Tab:AddButton({

	Name = "450Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",1)

end

})

Tab:AddButton({

	Name = "475Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",2)

end

})

Tab:AddButton({

	Name = "500Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",3)

end

})

Tab:AddButton({

	Name = "525Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 1)

end

})

Tab:AddButton({

	Name = "550Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 2)

end

})

Tab:AddButton({

	Name = "575Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 3)

end

})

local Section = Tab:AddSection({

    Name = "FOUNTAIN CITY"

})

Tab:AddButton({

	Name = "625Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",1)

end

})

Tab:AddButton({

	Name = "650Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",2)

end

})

Tab:AddButton({

	Name = "675Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",3)

end

})

--мб дропдауны под секции

Tab:AddButton({

	Name = "Player Quest",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer( "PlayerHunter")

end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Esp",

	Icon = "rbxassetid://12496239839",

	PremiumOnly = false

})

esps = {}

Tab:AddToggle({

    Name = "Fruit ESP",

    Default = false,

    Callback = function(Value) 

        if Value == true then

            fruitNames = {'Fruit ','Kilo Fruit', 'Spin Fruit', 'Chop Fruit', 'Spring Fruit', 'Bomb Fruit', 'Smoke Fruit', 'Spike Fruit', 'Flame Fruit', 'Bird: Falcon Fruit', 'Ice Fruit', 'Sand Fruit', 'Dark Fruit', 'Revive Fruit', 'Diamond Fruit', 'Light Fruit', 'Love Fruit', 'Rubber Fruit', 'Barrier Fruit', 'Magma Fruit', 'Quake Fruit', 'Human: Buddha Fruit', 'String Fruit', 'Bird: Phoenix Fruit', 'Portal Fruit', 'Rumble Fruit', 'Paw Fruit', 'Blizzard Fruit', 'Gravity Fruit', 'Dough Fruit', 'Shadow Fruit', 'Venom Fruit', 'Control Fruit', 'Spirit Fruit', 'Dragon Fruit', 'Leopard Fruit'}

            for key, value in pairs(fruitNames) do

                fruitNames[value] = key

            end

            for _, obj in pairs(workspace:GetChildren()) do

                if fruitNames[obj.Name] then

                    local billBoard = Instance.new("BillboardGui", obj.Handle)

                    local espText = Instance.new("TextLabel", billBoard)

                    

                    billBoard.Adornee = obj.Handle

                    billBoard.AlwaysOnTop = true

                    billBoard.Size = UDim2.new(1,200,1,30)

                    billBoard.Name = "Board"

                    

                    espText.Size = UDim2.new(1,0,1,0)

                    espText.Text = obj.Name

                    espText.TextColor3 = Color3.fromRGB(255,160,30)

                    espText.TextStrokeTransparency = 0

                    espText.BackgroundTransparency = 1

                    espText.TextSize = 10

                    espText.Name = "Text"

                    esps[billBoard] = obj

OrionLib:MakeNotification({

	Name = obj.Name,

	Content = "This fruit was found",

	Image = "rbxassetid://12496254877",

	Time = 10

})

                end

            end

        elseif Value == false then

            for esp, obj in pairs(esps) do

                esp:Destroy()

            end

            esps = {}

        end

    end

})

Tab:AddButton({

	Name = "Tracers",

	Callback = function()

local camera = workspace.CurrentCamera

for _,v in pairs(game.Players:GetPlayers()) do

if v ~= game.Players.LocalPlayer and v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then

local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)

local Line = Drawing.new("Line")

Line.Visible = true

Line.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)

Line.To = Vector2.new(vector.X, vector.Y)

Line.Color = Color3.fromRGB(255,160,30)

Line.Thickness = 2

Line.Transparency = 1

function script()

game:GetService("RunService").RenderStepped:Connect(function(step)

if v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then

local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)

if onScreen == true then

Line.To = Vector2.new(vector.X, vector.Y)

Line.Visible = true

else

Line.Visible = false

end

end

end)

end

coroutine.wrap(script)()

end

v.CharacterAdded:Connect(function()

repeat wait()  until v.Character ~= nil

repeat wait()  until v.Character:FindFirstChild("HumanoidRootPart") ~= nil

local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)

local Line = Drawing.new("Line")

Line.Visible = true

Line.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)

Line.To = Vector2.new(vector.X, vector.Y)

Line.Color = Color3.fromRGB(255,160,30)

Line.Thickness = 2

Line.Transparency = 1

function script()

game:GetService("RunService").RenderStepped:Connect(function(step)

if v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then

local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)

if onScreen == true then

Line.To = Vector2.new(vector.X, vector.Y)

Line.Visible = true

else

Line.Visible = false

end

end

end)

end

coroutine.wrap(script)()

end)

end

end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Fruit",

	Icon = "http://www.roblox.com/asset/?id=12496254877",

	PremiumOnly = false

})

Tab:AddToggle({

	Name = "Tp Fruit",

	Default = false,

	Callback = function(Grab)

_G.BringFruit = Grab

pcall(function()

while _G.BringFruit do wait(.1)

for i,v in pairs(game:GetService("Workspace"):GetChildren()) do

if v:IsA("Tool") then

local OldCFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame

game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame * CFrame.new(0,0,0)

v.Handle.CFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame

wait(.1)

game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = OldCFrame

end

end

end

end)

end

})

Tab:AddButton({

	Name = "Random Fruit",

	Callback = function()

      		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin", "Buy")

  	end    

})

Tab:AddButton({

	Name = "Fruit Shop",

	Callback = function()

game.Players.LocalPlayer.PlayerGui.Main.FruitShop.Visible = true

  	end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Points",

	Icon = "rbxassetid://12530069729",

	PremiumOnly = false

})

Tab:AddToggle({

	NameA = "uto Melee",

	Default = false,

	Callback = function(Melee1)

	_G.automelee = Melee1

automelee()

		end

})

Tab:AddToggle({

	Name = "Auto Defense",

	Default = false, 

	Callback = function(Defense1)

	_G.autodefense = Defense1

autodefense()

		end

})

Tab:AddToggle({

	Name = "Auto Sword",

	Default = false,

	Callback = function(Sword1)

	_G.autosword = Sword1

autosword()

		end

})

Tab:AddToggle({

	Name = "Auto Gun",

	Default = false,

	Callback = function(Gun1)

	_G.autogun = Gun1

autogun()

		end

})

Tab:AddToggle({

	Name = "Auto Devil Fruit",

	Default = false,

	Callback = function(Devil1)

	_G.autodevil = Devil1

autodevil()

		end

})

Tab:AddTextbox({

	Name = "Melee",

	Default = nil,

	TextDisappear = true,

	Callback = function(Melee)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", Melee) 

	end	  

})

Tab:AddTextbox({

	Name = "Defense",

	Default = nil,

	TextDisappear = true,

	Callback = function(Defense)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", Defense)

	end

})

Tab:AddTextbox({

	Name = "Sword",

	Default = nil,

	TextDisappear = true,

	Callback = function(Sword)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", Sword)

	end

})

Tab:AddTextbox({

	Name = "Gun",

	Default = nil,

	TextDisappear = true,

	Callback = function(Gun)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", Gun)

	end

})

Tab:AddTextbox({

	Name = "Devil Fruit",

	Default = nil,

	TextDisappear = true,

	Callback = function(Devil)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", Devil)

	end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name =  "GUIs soon...",

	Icon = "rbxassetid://12505501154",

	PremiumOnly = false

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name =  "Any Auto",

	Icon = "rbxassetid://12505499132",

	PremiumOnly = false

})

Tab:AddButton({

	Name = "Auto Sea2 testing..",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress","Detective")

wait(.00001)

topos(CFrame.new(1349.4, 37.5, -1326.2))

wait(.1)

local z = game.Players.LocalPlayer.Backpack.Key

z.Parent = game.Players.LocalPlayer.Character

end

})

Tab:AddToggle({

	Name = "Auto Silver Chest",

	Default = false,

	Callback = function(Chest1)

	_G.autochest1 = Chest1

autochest1()

		end

})

Tab:AddToggle({

	Name = "Auto Gold Chest",

	Default = false,

	Callback = function(Chest2)

	_G.autochest2 = Chest2

autochest2()

		end

})

Tab:AddToggle({

	Name = "Auto Diamond Chest",

    Default = false,

	Callback = function(Chest3)

	_G.autochest3 = Chest3

autochest3()

		end

})

Tab:AddToggle({

	Name = "Auto Buso",

	Default = false,

	Callback = function(Toggle1)

	_G.autobuso = Toggle1

autobuso()

		end

})

Tab:AddToggle({

	Name = "Auto Race",

	Default = false,

	Callback = function(Toggle5)

	_G.autorace = Toggle5

autorace()

		end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Teleport",

	Icon = "rbxassetid://12496230420",

	PremiumOnly = false

})

local Section = Tab:AddSection({

	Name = "Servers"

})

Tab:AddButton({

	Name = "Server Id",

	Callback = function()

    jobId = ''..game.JobId..''

	toClipboard(jobId)

	OrionLib:MakeNotification({

	Name = "Server ID copied to clipboard!",

	Content = "Paste this in Server Join Id",

	Image = "rbxassetid://4483345998",

	Time = 5

})

end

})

Tab:AddTextbox({

	Name = "Join Id Server",

	Default = ""..game.JobId.."",

	TextDisappear = true,

	Callback = function(Ponon)

		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId,Ponon,game.Players.LocalPlayer)

	end

})

Tab:AddButton({

	Name = "Rejoin",

	Callback = function()

if #game.Players:GetPlayers() == 1 then

		game.Players.LocalPlayer:Kick("\nRejoin...")

		wait()

		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)

	else

		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)

	end

  	end

})

Tab:AddButton({

	Name = "Server Hop",

	Callback = function()

loadstring(game:HttpGet"https://raw.githubusercontent.com/LeoKholYt/roblox/main/lk_serverhop.lua")():Teleport(game.PlaceId)

  	end    

})

local Section = Tab:AddSection({

	Name = "Worlds"

})

Tab:AddButton({

	Name = "Sea1",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")

  	end

})

Tab:AddButton({

	Name = "Sea2",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")

  	end

})

Tab:AddButton({

	Name = "Sea3",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")

  	end    

})

local Section = Tab:AddSection({

	Name = "Settings"

})

Tab:AddButton({

	Name = "Stop Tween",

	Callback = function()

topos(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)

end

})

local Section = Tab:AddSection({

	Name = "Islands"

})

Tab:AddButton({

	Name = "Marine Start",

	Callback = function()

topos(CFrame.new(-2566.4296875, 6.8556680679321, 2045.2561035156))

end

})

Tab:AddButton({

	Name = "Pirate Start",

	Callback = function()

topos(CFrame.new(979.79895019531, 16.516613006592, 1429.0466308594))

end

})

Tab:AddButton({

	Name = "Jungle",

	Callback = function()

topos(CFrame.new(-1612.7957763672, 36.852081298828, 149.12843322754))

end

})

Tab:AddButton({

	Name = "Pirate Village",

	Callback = function()

topos(CFrame.new(-1181.3093261719, 4.7514905929565, 3803.5456542969))

end

})

Tab:AddButton({

	Name = "Desert",

	Callback = function()

topos(CFrame.new(944.15789794922, 20.919729232788, 4373.3002929688))

end

})

Tab:AddButton({

	Name = "Snow Village",

	Callback = function()

topos(CFrame.new(1347.8067626953, 104.66806030273, -1319.7370605469))

end

})

Tab:AddButton({

	Name = "Marine Fortress",

	Callback = function()

topos(CFrame.new(-4914.8212890625, 50.963626861572, 4281.0278320313))

end

})

Tab:AddButton({

	Name = "Sky1",

	Callback = function()

topos(CFrame.new(-4869.1025390625, 733.46051025391, -2667.0180664063))

end

})

Tab:AddButton({

	Name = "Sky2",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))

  	end    

})

Tab:AddButton({

	Name = "Sky3",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))

  	end    

})

Tab:AddButton({

	Name = "Prison",

	Callback = function()

topos( CFrame.new(4875.330078125, 5.6519818305969, 734.85021972656))

end

})

Tab:AddButton({

	Name = "Colloseum",

	Callback = function()

topos( CFrame.new(-1427.6203613281, 7.2881078720093, -2792.7722167969))

end

})

Tab:AddButton({

	Name = "Magma Village",

	Callback = function()

topos(CFrame.new(-5247.7163085938, 12.883934020996, 8504.96875))

end

})

Tab:AddButton({

	Name = "Under Water City",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))

end

})

Tab:AddButton({

	Name = "Fountain City",

	Callback = function()

topos(CFrame.new(5411.8, 188.9, 4281.4))

end

})

Tab:AddButton({

	Name = "Mob Island",

	Callback = function()

topos( CFrame.new(-1503.6224365234, 219.7956237793, 1369.3101806641))

end

})

Tab:AddButton({

	Name = "Shank Room",

	Callback = function()

topos(CFrame.new(-1442.16553, 29.8788261, -28.3547478))

end

})

Tab:AddButton({

	Name = "Middle Town",

	Callback = function()

topos(CFrame.new(-2850.20068, 7.39224768, 5354.99268))

end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Boats",

	Icon = "rbxassetid://12496247656",

	PremiumOnly = false

})

local Section = Tab:AddSection({

	Name = "Pirate"

})

Tab:AddButton({

	Name = "Pirate Sloop 600$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateSloop")

  	end

})

Tab:AddButton({

	Name = "Pirate Basic 1.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBasic")

   	end    

})

Tab:AddButton({

	Name = "Pirate Brigade 4.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBrigade")

  	end    

})

local Section = Tab:AddSection({

	Name = "Marine"

})

Tab:AddButton({

	Name = "Marine Sloop 150$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineSloop")

  	end

})

Tab:AddButton({

	Name = "Marine Basic 600$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBasic")

  	end

})

Tab:AddButton({

	Name = "MarineBrigade 2.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBrigade")

  	end

})

local Section = Tab:AddSection({

	Name = "Luxury"

})

Tab:AddButton({

	Name = "RocketBoost 0$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "RocketBoost")

  	end

})

Tab:AddButton({

	Name = "Enforcer 1.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Enforcer")

  	end

})

Tab:AddButton({

	Name = "Swan 5.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Swan")

  	end

})

Tab:AddButton({

	Name = "Flower 5.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Flower")

  	end    

})

Tab:AddButton({

	Name = "Sleigh 5.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Sleigh")

  	end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Fast Cmd soon...",

	Icon = "rbxassetid://12496242729",

	PremiumOnly = false

})    

Tab:AddTextbox({

	Name = "Textbox",

	Default = "soon...",

	TextDisappear = true,

	Callback = function(Cmd)

		if Cmd == pon then

print("pon")

elseif Cmd == pon1 then

print("pon1")

end

	end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Combat soon..",

	Icon = "rbxassetid://12496236549",

	PremiumOnly = false

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Raids soon..",

	Icon = "rbxassetid://4483345998",

	PremiumOnly = false

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Troll",

	Icon = "rbxassetid://12505494337",

	PremiumOnly = false

})

Tab:AddToggle({

	Name = "Freeze",

	Default = nil,

	Callback = function(Value1)

	if Value1 == true then   game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true

elseif Value1 == false then

game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false

	end 

end   

})

Tab:AddButton({

	Name = "Sit",

	Callback = function()

game.Players.LocalPlayer.Character.Humanoid.Sit = true

  	end

})

Tab:AddButton({

	Name = "Lay Down",

	Callback = function()

local Human = game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid')

	if not Human then

		return

	end

	Human.Sit = true

	task.wait(.1)

	Human.RootPart.CFrame = Human.RootPart.CFrame * CFrame.Angles(math.pi * .5, 0, 0)

	for _, v in ipairs(Human:GetPlayingAnimationTracks()) do

		v:Stop()

	end

  	end  

})

Tab:AddTextbox({

	Name = "Spin",

	Default = nil,

	TextDisappear = true,

	Callback = function(SPINN)

		function getRoot(char)

	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')

	return rootPart

end

local Spin = Instance.new("BodyAngularVelocity")

	Spin.Name = "Spinning"

	Spin.Parent = getRoot(game.Players.LocalPlayer.Character)

	Spin.MaxTorque = Vector3.new(0, math.huge, 0)

	Spin.AngularVelocity = Vector3.new(0, SPINN, 0)

	end

})

Tab:AddButton({

	Name = "Stop Spin",

	Callback = function()

function getRoot(char)

	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')

	return rootPart

end

for i,v in pairs(getRoot(game.Players.LocalPlayer.Character):GetChildren()) do

		if v.Name == "Spinning" then

			v:Destroy()

		end

	end

  	end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Codes soon...",

	Icon = "rbxassetid://12496297350",

	PremiumOnly = false

})  

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Player Settings",

	Icon = "rbxassetid://12496250171",

	PremiumOnly = false

})

Tab:AddTextbox({

	Name = "Chat",

	Default = "Chat",

	TextDisappear = true,

	Callback = function(Say)

		game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(Say,"All")

	end	 

})

Tab:AddDropdown({

	Name = "Buso State",

	Default = nil,

	Options = {"0", "1", "2", "3", "4", "5"},

	Callback = function(statebuso)

		if statebuso == "0" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",0)

elseif statebuso == "1" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",1)

elseif statebuso == "2" then 

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",2)

elseif statebuso == "3" then 

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",3)

elseif statebuso == "4" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",4)

elseif statebuso == "5" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",5)

	end

	end

})

Tab:AddTextbox({

	Name = "Ken Range",

	Default = "Ken Range(30k+ lag)",

	TextDisappear = true,

	Callback = function(KenRange)

		game.Players.LocalPlayer.VisionRadius.Value = KenRange

	end	 

})

Tab:AddButton({

	Name = "Reset",

	Callback = function()

game.Players.LocalPlayer.Character:BreakJoints()

  	end

})

Tab:AddTextbox({

	Name = "Title",

	Default = "Title",

	TextDisappear = true,

	Callback = function(title)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateTitle", title)

	end

})

Tab:AddButton({

	Name = "Pirates",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Pirates")

  	end

})

Tab:AddButton({

	Name = "Marines",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Marines")

  	end

})

Tab:AddDropdown({

	Name = "Buso Color",

	Default = nil,

	Options = {"Rainbow Saviour","Winter Sky", "Pure Red", "Snow White","Absolute Zero","Fiery Rose","Heat Wave","Plump Purple","Blue Jeans","Green Lizard","Slimy Green","Yellow Sunshine","Bright Yellow","Orange Soda"},

	Callback = function(busoColor)

if busoColor == "Rainbow Saviour" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Rainbow Saviour")

   elseif busoColor == "Winter Sky" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Winter Sky")

   elseif busoColor == "Pure Red" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Pure Red")

   elseif busoColor == "Snow White" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Snow White")

   elseif busoColor == "Absolute Zero" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Absolute Zero")

   elseif busoColor == "Heat Wave" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Heat Wave")

   elseif busoColor == "Fiery Rose" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Fiery Rose")

   elseif busoColor == "Plump Purple" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Plump Purple")

   elseif busoColor == "Blue Jeans" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Blue Jeans")

   elseif busoColor == "Green Lizard" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Green Lizard")

   elseif busoColor == "Slimy Green" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Slimy Green")

   elseif busoColor == "Yellow Sunshine" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Yellow Sunshine")

   elseif busoColor == "Bright Yellow" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Bright Yellow")

   elseif busoColor == "Orange Soda" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Orange Soda")

end

end

})

Tab:AddTextbox({

	Name = "Mastery info",

	Default = nil,

	TextDisappear = true,

	Callback = function(plrName1)

     for _,obj in pairs(getPlayerByNick(plrName1).Backpack:GetChildren()) do

    if obj.ClassName == 'Tool' then

        OrionLib:MakeNotification({

	Name = "Stats",

	Content = 'Name:'.. obj.Name ..'| Mastery:'.. obj.Level.Value ..'.',

	Image = "rbxassetid://4483345998",

	Time = 15

})

end	  

end

end

})

Tab:AddTextbox({

    Name = "Check Stats",

    Default = nil,

    TextDisappear = true,

    Callback = function(plrName)

        OrionLib:MakeNotification({

            Name = "Beli:"..getPlayerByNick(plrName).Data.Beli.Value.."Frags:"..getPlayerByNick(plrName).Data.Fragments.Value..'.',

            Content = "Player's stats",

            Image = "rbxassetid://12496227758",

            Time = 10

        })

    end

})

Tab:AddButton({

	Name = "Check Accessories Info",

	Callback = function()

OrionLib:MakeNotification({

	Name = ''.. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Nerd") ..'',

	Content = "Nerd",

	Image = "rbxassetid://4483345998",

	Time = 5

})

end

})

Tab:AddButton({

	Name = "X-ray",

	Callback = function()

local sc = (debug and debug.setconstant) or setconstant

	local gc = (debug and debug.getconstants) or getconstants

local pop = game.Players.LocalPlayer.PlayerScripts.PlayerModule.CameraModule.ZoomController.Popper

	for _, v in pairs(getgc()) do

		if type(v) == 'function' and getfenv(v).script == pop then

			for i, v1 in pairs(gc(v)) do

				if tonumber(v1) == .25 then

					sc(v, i, 0)

				elseif tonumber(v1) == 0 then

					sc(v, i, .25)

				end

			end

		end

	end

end

})

Tab:AddButton({

	Name = "No Fog",

	Callback = function()

game.Lighting.FogEnd = 100000

	for i,v in pairs(Lighting:GetDescendants()) do

		if v:IsA("Atmosphere") then

			v:Destroy()

		end

	end

end

})

Tab:AddButton({

	Name = "MaxZoom inf",

	Callback = function()

game.Players.LocalPlayer.CameraMaxZoomDistance = 999999

end

})

Tab:AddButton({

	Name = "MaxZoom normal",

	Callback = function()

game.Players.LocalPlayer.CameraMaxZoomDistance = 100

end

})

end
