-- Pet & Seed Spawner (non-visual)
local player = game.Players.LocalPlayer
local args = {
    [1] = "PetNameHere" -- Ganti dengan nama pet yang valid di game
}

-- Contoh remote spawn pet
game:GetService("ReplicatedStorage").Remotes.SpawnPet:FireServer(unpack(args))

-- Delay sedikit sebelum seed
wait(1)

-- Contoh remote spawn seed
local seedArgs = {
    [1] = "SeedTypeHere" -- Ganti dengan nama seed
}
game:GetService("ReplicatedStorage").Remotes.SpawnSeed:FireServer(unpack(seedArgs))

print("✅ Pet dan seed telah di-spawn!")
