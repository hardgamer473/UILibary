  1. Creating the menu
local UILibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/hardgamer473/UILibary/refs/heads/main/UILibrary.lua"))()

  2. Create a Window
local win = UILibrary:CreateWindow("My Cool UI")

  3. Add Tabs
local tab = UILibrary:CreateTab(win, "Main")

 
 4. Normal Toggle
UILibrary:Toggle(tab, "God Mode", false, function(state)
    if state then
        print("God Mode Enabled")
    else
        print("God Mode Disabled")
    end
end)

 5. Loop Toggle
UILibrary:LoopToggle(tab, "Auto Jump", false, function()
    game.Players.LocalPlayer.Character.Humanoid.Jump = true
    task.wait(0.2)
end)

6. Sliders
UILibrary:Slider(tab, "WalkSpeed", 16, 100, 16, function(val)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = val
end)
