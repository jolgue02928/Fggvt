-- Compra "Fantasy Egg" 20 vezes por segundo (com cuidado!)
while true do
    local args = {
        [1] = "Fantasy Egg",
        [2] = 70
    }

    game:GetService("ReplicatedStorage").Network.Eggs_RequestPurchase:InvokeServer(unpack(args))

    task.wait(0.05) -- 0.05s = 20 vezes por segundo
end
