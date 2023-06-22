local character = game.Players.LocalPlayer.Character
local lifeBricks = {
    game:GetService("Workspace").Lifebricks["1"],
    game:GetService("Workspace").Lifebricks["2"],
    game:GetService("Workspace").Lifebricks["3"],
    game:GetService("Workspace").Lifebricks["4"]
}

local currentIndex = 1
while true do
    local currentLifeBrick = lifeBricks[currentIndex]
    character.HumanoidRootPart.CFrame = currentLifeBrick.CFrame
    
    if currentIndex == 4 then
        game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId)
        break
    end
    
    currentIndex = currentIndex + 1
    wait(1)
end
