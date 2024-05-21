-- Get the player and their character
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Function to make the character spin
local function spinCharacter()
    while true do
        for angle = 0, 360, 5 do
            character:SetPrimaryPartCFrame(character.PrimaryPart.CFrame * CFrame.Angles(0, math.rad(5), 0))
            wait(0.05) -- Adjust the speed of spinning by changing the wait time
        end
    end
end

-- Call the function to start spinning the character
spinCharacter()
