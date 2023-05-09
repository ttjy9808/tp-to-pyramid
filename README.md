local localplayer = game.Players.LocalPlayer
local Char = localplayer.Character or workspace:FindFirstChild(localplayer.Name)
        local HRP = Char and Char:FindFirstChild("HumanoidRootPart")
        if not Char or not HRP then
           
        end
        local p = HRP.Position
        local hrd = game.Players.LocalPlayer.Character.HumanoidRootPart
        local x = -262.19
        local y = 161.43
        local z = -1346.78
        hrd.CFrame = CFrame.new(p.x, 1000, p.z)
        wait(0.5)
        local currentPos = Vector3.new(p.x, 1000, p.z)
        local targetPos = Vector3.new(x, 1000, z)

        local direction = (targetPos - currentPos).Unit
        local distance = (targetPos - currentPos).Magnitude
        local steps = math.floor(distance / 10) 
        for i = 1, steps do
            currentPos = currentPos + direction * 10
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end

        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(0.1)
        local p = hrd.Position
        
        local currentPos = Vector3.new(x, 1000, z)
        local targetPos = Vector3.new(x, y, z)

        local direction = (targetPos - currentPos).Unit
        local distance = (targetPos - currentPos).Magnitude
        local steps = math.floor(distance / 10) 
        for i = 1, steps do
            currentPos = currentPos + direction * 10 
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end
        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait()
