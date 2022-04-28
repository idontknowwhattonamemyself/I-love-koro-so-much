wait(4)
local jobid = game.JobId
local castlerockTime = workspace.MonsterSpawns.Triggers.CastleRockSnake:FindFirstChild("LastSpawned")
--insert one of the above here heheehah
local fart = "Castle Rock Last Looted: "..tostring(math.floor((os.time() - castlerockTime.Value) / 60)) .. " minutes ago.." 

local url = Webhook

local data = {
   ["content"] = "Castle Rock Last Looted:",
   ["embeds"] = {
       {
           ["title"] = fart,
           ["description"] = "Username: " .. game.Players.LocalPlayer.Name..",      Job ID: "..game.JobId,
           ["type"] = "rich",
           ["color"] = tonumber(0x7269da),
           ["image"] = {
               ["url"] = "http://www.roblox.com/Thumbs/Avatar.ashx?x=150&y=150&Format=Png&username=" ..
                   tostring(game:GetService("Players").LocalPlayer.Name)
           }
       }
   }
}
local newdata = game:GetService("HttpService"):JSONEncode(data)

local headers = {
   ["content-type"] = "application/json"
}
request = http_request or request or HttpPost or syn.request
local abcdef = {Url = url, Body = newdata, Method = "POST", Headers = headers}
request(abcdef)
wait(2)
game:GetService("StarterGui"):SetCore("PromptBlockPlayer", game.Players:GetChildren()[2])
wait(1)
local blockpos = game:GetService("CoreGui").RobloxGui.PromptDialog.ContainerFrame.ConfirmButton.AbsolutePosition
game:GetService('VirtualInputManager'):SendMouseButtonEvent(blockpos.X + 5, blockpos.Y + 40, 0, true, game, 0);
                task.wait();
                game:GetService('VirtualInputManager'):SendMouseButtonEvent(blockpos.X + 5, blockpos.Y + 40, 0, false, game, 0);
while task.wait(4) do 
game:GetService('TeleportService'):Teleport(3016661674)
end;
