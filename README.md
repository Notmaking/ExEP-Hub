# ExEP-Hub
ExEP Hub is a clean roblox UI hub for exploiting. it comes with all the features your gonna want.
It has: flying, speed increase jumpHeight increase, and you can even make your own notification!
This is just P1 of ExEP Hub, there is a LOT more to come.
-------------------------------------------------------------------------------------------------
Main Script:   local WindUI = loadstring(game:HttpGet("https://github.com/Footagesus/WindUI/releases/latest/download/main.lua"))()

local Window = WindUI:CreateWindow({
    Title = "ExEP Hub",
    Icon = "circle-check-big", -- lucide icon
    Author = "by ExEP Development",
    Folder = "ExEP-UrNotGettingMe12@3",
    
    -- ↓ This all is Optional. You can remove it.
    Size = UDim2.fromOffset(580, 460),
    MinSize = Vector2.new(560, 350),
    MaxSize = Vector2.new(850, 560),
    Transparent = true,
    Theme = "Dark",
    Resizable = true,
    SideBarWidth = 200,
    BackgroundImageTransparency = 0.42,
    HideSearchBar = true,
    ScrollBarEnabled = false,
    
    -- ↓ Optional. You can remove it.
    --[[ You can set 'rbxassetid://' or video to Background.
        'rbxassetid://':
            Background = "rbxassetid://", -- rbxassetid
        Video:
            Background = "video:YOUR-RAW-LINK-TO-VIDEO.webm", -- video 
    --]]
    
    -- ↓ Optional. You can remove it.
    User = {
        Enabled = true,
        Anonymous = false,
        Callback = function()
            print("clicked")
        end,
    },
    
    --       remove this all, 
    -- !  ↓  if you DON'T need the key system
    KeySystem = { 
        -- ↓ Optional. You can remove it.
        Key = { "ExEP-REG", "ExEP-VIP" },
        
        Note = "ExEP Hub",
        
        -- ↓ Optional. You can remove it.
        Thumbnail = {
            Image = "rbxassetid://",
            Title = "Thumbnail",
        },
        
        -- ↓ Optional. You can remove it.
        URL = "https://bst.gg/y9b_",
        
        -- ↓ Optional. You can remove it.
        SaveKey = true, -- automatically save and load the key.
        
        -- ↓ Optional. You can remove it.
        -- API = {} ← Services. Read about it below ↓
    },
})

local Tab = Window:Tab({
    Title = "Main",
    Icon = "cog", -- optional
    Locked = false,
})

Window:Tag({
    Title = "v0.0.1",
    Color = Color3.fromHex("#30ff6a"),
    Radius = 13, -- from 0 to 13
})

WindUI:Notify({
    Title = "ExEP Development",
    Content = "Hub Loaded :3",
    Duration = 5, -- 3 seconds
    Icon = "circle-check",
})

local Button = Tab:Button({
    Title = "100 Speed",
    Desc = "Speed set to 100",
    Locked = false,
    Callback = function()
        print("Speed is now 16 lol")
    end
})

local Button = Tab:Button({
    Title = "Notif",
    Desc = "Notif",
    Locked = false,
    Callback = function()
        WindUI:Notify({
    Title = ":3",
    Content = "HEHE",
    Duration = 5, -- 3 seconds
    Icon = "laugh",
})
    end
})

local notificationsTab = Window:Tab({
    Title = "Notifications",
    Icon = "message-square-dot", -- optional
    Locked = false,
})

local Input = notificationsTab:Input({
    Title = "Custom Notif",
    Desc = "CN Title",
    Value = "Your Notif Content",
    InputIcon = "cog",
    Type = "Input", -- or "Textarea"
    Placeholder = "Enter text...",
    Callback = function(input) 
        WindUI:Notify({
    Title = (input),
    Duration = 3, -- 3 seconds
})
    end
})
