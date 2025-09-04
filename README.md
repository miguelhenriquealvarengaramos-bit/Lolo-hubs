 p = game.Players.LocalPlayer
local s = false
local spd = 50

game:GetService("UserInputService").InputBegan:Connect(function(i,g)
    if g then return end
    if i.KeyCode == Enum.KeyCode.ButtonR2 then -- BOTÃO USADO PARA MOBILE (mude se quiser)
        s = not s
        if s then
            local bv = Instance.new("BodyVelocity", p.Character.HumanoidRootPart)
            bv.Name = "flyvel"
            bv.MaxForce = Vector3.new(9e9, 9e9, 9e9)
            bv.Velocity = Vector3.new(0,spd,0)
        else
            if p.Character.HumanoidRootPart:FindFirstChild("flyvel") then
                p.Character.HumanoidRootPart.flyvel:Destroy()
            end
        end
    end
end)# Lolo-hubs
