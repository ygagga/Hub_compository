local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "ðŸ¡ Brookhaven RP Script",
   LoadingTitle = "Doc Hub",
   LoadingSubtitle = "by Mid_NightCreper24",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Doc Hub | Creper"
   },
   Discord = {
      Enabled = true,
      Invite = "7CM3rVSX7V", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "Doc Hub | Key System",
      Subtitle = "Link in Discord Server",
      Note = "Join server from Misc Tab",
      FileName = "DockHubKey14", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = true, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"https://pastebin.com/raw/3q9rQsQ8"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local MainTab = Window:CreateTab("ðŸ  Home", nil) -- Title, Image
local MainSection = MainTab:CreateSection("Main")

Rayfield:Notify({
   Title = "You have successfully executed the script!",
   Content = "The script was successfully executed, and you are ready to go!",
   Duration = 5,
   Image = nil,
   Actions = { -- Notification Buttons
      Ignore = {
         Name = "Okay!",
         Callback = function()
         print("The user tapped Okay!")
      end
   },
},
})

local Button = MainTab:CreateButton({
   Name = "Kill All",
   Callback = function()
   -- Gui to Lua
-- Version: 3.2

-- Instances:

local KillGui = Instance.new("ScreenGui")
local Opener = Instance.new("TextButton")
local UIGradient = Instance.new("UIGradient")
local Frame = Instance.new("ImageLabel")
local Player = Instance.new("TextBox")
local UIGradient_2 = Instance.new("UIGradient")
local Kill = Instance.new("TextButton")
local Cancel = Instance.new("TextButton")
local LKill = Instance.new("TextButton")
local UIGradient_3 = Instance.new("UIGradient")

--Properties:

KillGui.Name = "KillGui"
KillGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
KillGui.ResetOnSpawn = false

Opener.Name = "Opener"
Opener.Parent = KillGui
Opener.BackgroundColor3 = Color3.fromRGB(80, 255, 116)
Opener.BackgroundTransparency = 1.000
Opener.BorderSizePixel = 0
Opener.Position = UDim2.new(0.890184641, 0, 0.665688097, 0)
Opener.Size = UDim2.new(0, 113, 0, 50)
Opener.ZIndex = 2
Opener.Font = Enum.Font.SourceSans
Opener.Text = "Open"
Opener.TextColor3 = Color3.fromRGB(255, 255, 255)
Opener.TextScaled = true
Opener.TextSize = 14.000
Opener.TextWrapped = true

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 0)), ColorSequenceKeypoint.new(0.23, Color3.fromRGB(238, 0, 255)), ColorSequenceKeypoint.new(0.48, Color3.fromRGB(0, 0, 255)), ColorSequenceKeypoint.new(0.63, Color3.fromRGB(32, 244, 255)), ColorSequenceKeypoint.new(0.78, Color3.fromRGB(4, 255, 0)), ColorSequenceKeypoint.new(0.89, Color3.fromRGB(255, 255, 0)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 0))}
UIGradient.Parent = Opener

Frame.Name = "Frame"
Frame.Parent = KillGui
Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame.BackgroundTransparency = 1.000
Frame.Position = UDim2.new(0.753321111, 0, 0.741761386, 0)
Frame.Size = UDim2.new(0, 253, 0, 170)
Frame.Visible = false
Frame.Image = "rbxassetid://2851926732"
Frame.ImageColor3 = Color3.fromRGB(72, 255, 96)
Frame.ScaleType = Enum.ScaleType.Slice
Frame.SliceCenter = Rect.new(12, 12, 12, 12)

Player.Name = "Player"
Player.Parent = Frame
Player.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Player.BackgroundTransparency = 0.750
Player.BorderSizePixel = 0
Player.Position = UDim2.new(0.0967741907, 0, 0.152100846, 0)
Player.Size = UDim2.new(0, 200, 0, 50)
Player.ZIndex = 2
Player.Font = Enum.Font.FredokaOne
Player.PlaceholderText = "Player To Kill"
Player.Text = ""
Player.TextColor3 = Color3.fromRGB(255, 255, 255)
Player.TextScaled = true
Player.TextSize = 14.000
Player.TextWrapped = true

UIGradient_2.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 0)), ColorSequenceKeypoint.new(0.23, Color3.fromRGB(238, 0, 255)), ColorSequenceKeypoint.new(0.48, Color3.fromRGB(0, 0, 255)), ColorSequenceKeypoint.new(0.63, Color3.fromRGB(32, 244, 255)), ColorSequenceKeypoint.new(0.78, Color3.fromRGB(4, 255, 0)), ColorSequenceKeypoint.new(0.89, Color3.fromRGB(255, 255, 0)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 0))}
UIGradient_2.Parent = Player

Kill.Name = "Kill"
Kill.Parent = Frame
Kill.BackgroundColor3 = Color3.fromRGB(141, 255, 142)
Kill.BackgroundTransparency = 1.000
Kill.BorderSizePixel = 0
Kill.Position = UDim2.new(0, 0, 0.700840294, 0)
Kill.Size = UDim2.new(0, 73, 0, 50)
Kill.ZIndex = 2
Kill.Font = Enum.Font.SourceSans
Kill.Text = "Kill"
Kill.TextColor3 = Color3.fromRGB(255, 255, 255)
Kill.TextScaled = true
Kill.TextSize = 14.000
Kill.TextWrapped = true

Cancel.Name = "Cancel"
Cancel.Parent = Frame
Cancel.BackgroundColor3 = Color3.fromRGB(141, 255, 142)
Cancel.BackgroundTransparency = 1.000
Cancel.BorderSizePixel = 0
Cancel.Position = UDim2.new(0.705645204, 0, 0.700840294, 0)
Cancel.Size = UDim2.new(0, 73, 0, 50)
Cancel.ZIndex = 2
Cancel.Font = Enum.Font.SourceSans
Cancel.Text = "Cancel"
Cancel.TextColor3 = Color3.fromRGB(255, 255, 255)
Cancel.TextScaled = true
Cancel.TextSize = 14.000
Cancel.TextWrapped = true

LKill.Name = "LKill"
LKill.Parent = Frame
LKill.BackgroundColor3 = Color3.fromRGB(141, 255, 142)
LKill.BackgroundTransparency = 1.000
LKill.BorderSizePixel = 0
LKill.Position = UDim2.new(0.342741907, 0, 0.700840294, 0)
LKill.Size = UDim2.new(0, 73, 0, 50)
LKill.ZIndex = 2
LKill.Font = Enum.Font.SourceSans
LKill.Text = "Loopkill"
LKill.TextColor3 = Color3.fromRGB(255, 255, 255)
LKill.TextScaled = true
LKill.TextSize = 14.000
LKill.TextWrapped = true

UIGradient_3.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 0)), ColorSequenceKeypoint.new(0.23, Color3.fromRGB(238, 0, 255)), ColorSequenceKeypoint.new(0.48, Color3.fromRGB(0, 0, 255)), ColorSequenceKeypoint.new(0.63, Color3.fromRGB(32, 244, 255)), ColorSequenceKeypoint.new(0.78, Color3.fromRGB(4, 255, 0)), ColorSequenceKeypoint.new(0.89, Color3.fromRGB(255, 255, 0)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 0))}
UIGradient_3.Parent = Frame

-- Scripts:

local function HJEL_fake_script() -- KillGui.LocalScript 
	local script = Instance.new('LocalScript', KillGui)

	script.Parent.Opener.MouseButton1Click:Connect(function()
		script.Parent.Frame.Visible = true
	end)
	
	script.Parent.Frame.Cancel.MouseButton1Click:Connect(function()
		script.Parent.Frame.Visible = false
	end)
	
	script.Parent.Frame.Kill.MouseButton1Click:Connect(function()
		game.Players:FindFirstChild(script.Parent.Frame.Player.Text).Character.Humanoid.Health = 0
		script.Parent.Frame.Visible = false
	end)
	
	script.Parent.Frame.LKill.MouseButton1Click:Connect(function()
		while true do
			game.Players:WaitForChild(script.Parent.Frame.Player.Text).Character.Humanoid.Health = 0
			wait(1)
		end
		
		script.Parent.Frame.Visible = false
	end)
end
coroutine.wrap(HJEL_fake_script)()
   end,
})

local Slider = MainTab:CreateSlider({
   Name = "Walkspeed Slider",
   Range = {0, 300},
   Increment = 1,
   Suffix = "Speed",
   CurrentValue = 16,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
   end,
})

local Dropdown = MainTab:CreateDropdown({
   Name = "Items",
   Options = {"Get All Tools","Get Sofa","Get Crystal","Get Crystals","Get Agency Book","Get Fire Hose","None"}
   CurrentOption = {"None"},
   MultipleOptions = false,
   Flag = "item", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Option)
        print(Option)
   end,
})

local ItemTab = Window:CreateTab("ðŸ›‹ï¸Items", nil) -- Title, Image
local Section = ItemTab:CreateSection("Items")

local Button = ItemTab:CreateButton({
   Name = "All Items",
   Callback = function()
        print(All Items)
   end,
})

local Button = ItemTab:CreateButton({
   Name = "Sofa",
   Callback = function()
        print(Sofa)
   end,
})

local Button = ItemTab:CreateButton({
   Name = "Crystal",
   Callback = function()
        print(Crystal)
   end,
})

local Button = ItemTab:CreateButton({
   Name = "Agency Book",
   Callback = function()
        print(Agency Book)
   end,
})

local Button = ItemTab:CreateButton({
   Name = "Fire Hose",
   Callback = function()
        print(Fire Hose)
   end,
})

local MiscTab = Window:CreateTab("ðŸŽ²Items", nil) -- Title, Image
local Section = MiscTab:CreateSection("Items")

local Toggle = MiscTab:CreateToggle({
   Name = "Cool",
   CurrentValue = false,
   Flag = "toggleexample", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
        print('hello')
   end,
})

local Input = MiscTab:CreateInput({
   Name = "Jump Power",
   PlaceholderText = "1-200",
   RemoveTextAfterFocusLost = true,
   Callback = function(Text)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = (Text)
   end,
})
