local OrionLib = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Orion/main/source'))()
local Window = OrionLib:MakeWindow({
    Name = "Title of the library",
    HidePremium = false,
    SaveConfig = true,
    ConfigFolder = "OrionTest"
})

local Tab = Window:MakeTab({
    Name = "scripts/main",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

Tab:AddButton({
    Name = "speed 50(good for cook burgers lol)",
    Callback = function()
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 50
    end    
})

Tab:AddButton({
    Name = "jump power 100(good for cook burgers lol)",
    Callback = function()
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 100
    end    
})

Tab:AddButton({
    Name = "inf yield(universal)",
    Callback = function()
        loadstring(game:HttpGet("https://scriptblox.com/raw/Infinite-Yield_500"))()
    end    
})

Tab:AddTextbox({
    Name = "WalkSpeed",
    Default = "15",
    TextDisappear = true,
    Callback = function(Value)
        local newWalkSpeed = tonumber(Value)
        if newWalkSpeed then
            game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = newWalkSpeed
        else
            warn("Введите корректное числовое значение для скорости игрока")
        end
    end	  
})

Tab:AddTextbox({
    Name = "JumpPower",
    Default = "15",
    TextDisappear = true,
    Callback = function(Value)
        local newJumpPower = tonumber(Value)
        if newJumpPower then
            game.Players.LocalPlayer.Character.Humanoid.JumpPower = newJumpPower
        else
            warn("Введите корректное числовое значение для прыжка игрока")
        end
    end	  
})

Tab:AddButton({
    Name = "mfly💀(universal)",
    Callback = function()
        loadstring(game:HttpGet("https://scriptblox.com/raw/Universal-Script-Mfly-9410"))()
    end    
})

Tab:AddButton({
    Name = "chat bypass(some games)",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Synergy-Networks/products/main/BetterBypasser/loader.lua",true))()
    end    
})

Tab:AddButton({
    Name = "10 (Repeated)",
    Callback = function()
        local count = 0
        local maxCount = 10
        local interval = 0.2

        local function fireServerRepeatedly()
            if count < maxCount then
                count = count + 1
                if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                    game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
                end
                wait(interval)
                fireServerRepeatedly()
            end
        end

        fireServerRepeatedly()
    end    
})

local ToggleActive = false
local Interval = 0.05
local Timer

Tab:AddToggle({
    Name = "give kill",
    Default = false,
    Callback = function(Value)
        ToggleActive = Value
        if ToggleActive then
            Timer = game:GetService("RunService").Heartbeat:Connect(function()
                if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                    game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
                end
                wait(Interval)
            end)
        else
            if Timer then
                Timer:Disconnect()
            end
        end
    end    
})

local Tab2 = Window:MakeTab({
    Name = "slap battles spam sound",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

Tab2:AddButton({
    Name = "10",
    Callback = function()
        for i = 1, 10 do
            if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
            end
            wait(0.2)
        end
    end    
})

Tab2:AddButton({
    Name = "25",
    Callback = function()
        for i = 1, 25 do
            if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
            end
            wait(0.2)
        end
    end    
})

Tab2:AddButton({
    Name = "50",
    Callback = function()
        for i = 1, 50 do
            if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
            end
            wait(0.2)
        end
    end    
})

Tab2:AddButton({
    Name = "100",
    Callback = function()
        for i = 1, 100 do
            if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
            end
            wait(0.2)
        end
    end    
})

Tab2:AddButton({
    Name = "250",
    Callback = function()
        for i = 1, 250 do
            if game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button then
                game.Players.LocalPlayer.PlayerGui.GlovesButton.KillstreakBtn.Button:FireServer()
            end
            wait(0.2)
        end
    end    
})
