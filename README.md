local ScreenGui = Instance.new("ScreenGui")
    local Toggle = Instance.new("TextButton")
    
    ScreenGui.Name = "ScreenGui"
    ScreenGui.Parent = game.CoreGui
    
    Toggle.Name = "Toggle"
    Toggle.Parent = ScreenGui
    Toggle.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
    Toggle.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)
    Toggle.Size = UDim2.new(0, 50, 0, 50)
    Toggle.Font = Enum.Font.Code
    Toggle.Text = "M"
    Toggle.TextColor3 = Color3.fromRGB(255, 0, 0)
    Toggle.TextScaled = true
    Toggle.MouseButton1Down:connect(function()
        game:GetService("VirtualInputManager"):SendKeyEvent(true,305,false,game)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,305,false,game)
    end)

local DarkraiX = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Kavo-Ui/main/Darkrai%20Ui", true))()

local Library = DarkraiX:Window("Darkrai X","","",Enum.KeyCode.RightControl);
Tab1 = Library:Tab("Credit")

Tab1:Button("Discord [Copy]",function()
    setclipboard("https://discord.gg/YFWNKr2N")
end)
Tab1:Button("YouTube [Copy]",function()
    setclipboard("Perfect v")
end)

Tab1 = Library:Tab("Main")

Tab1:Toggle("white screen",false,function(state)
if state then
    game:GetService("RunService"):Set3dRenderingEnabled(false)
else
    game:GetService("RunService"):Set3dRenderingEnabled(true)
    end
    end)
    

    
    
Tab1:Toggle("auto farm",false,function(value)
_G.Auto_Farm = value 

function totarget(p)
    local Distance2 = (p.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
    local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = p})
    tween:Play()
    if Distance2 <= 75 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
    end
end

function checklevel()
    local lv = game:GetService("Players").LocalPlayer.Data.Level.Value
    if lv == 1 or lv <= 9 then
        Mon = "Bandit [Lv. 5]"
        Title = "Bandit"
        QuestName = "BanditQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1061.15271, 16.7367725, 1548.93018, -0.836085379, -3.89774577e-08, 0.548599303, -1.17575967e-08, 1, 5.31300408e-08, -0.548599303, 3.79710414e-08, -0.836085379)
        CFrameMon = CFrame.new(1151.11829, 16.7761021, 1599.73499, -0.999999762, 0, -0.000701809535, 0, 1, 0, 0.000701809535, 0, -0.999999762)
        CFramePuk = CFrame.new(1101.75903, 67.6758957, 1617.50391, -0.399259984, -5.24373327e-08, -0.916837752, -1.74068084e-08, 1, -4.96134582e-08, 0.916837752, -3.84945009e-09, -0.399259984)
    elseif lv == 10 or lv <= 14 then
        Mon = "Monkey [Lv. 14]"
        Title = "Monkey"
        QuestName = "JungleQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1479.76099, 23.195364, 106.327942, 0.96289885, 5.22265786e-10, -0.269862473, 6.59528099e-10, 1, 4.28857172e-09, 0.269862473, -4.30744285e-09, 0.96289885)
        CFramePuk = CFrame.new(-1776.32959, 61.1782455, 66.8902054, -0.912609756, -2.38546143e-08, 0.408831745, -2.14773621e-08, 1, 1.04056577e-08, -0.408831745, 7.15677129e-10, -0.912609756)
        elseif lv == 15 or lv <= 29 then
        Mon = "Gorilla [Lv. 20]"
        Title = "Gorilla"
        QuestName = "JungleQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1242.46655, 6.62262297, -523.166382, -0.974416733, 9.23166681e-08, -0.224748924, 9.58993027e-08, 1, -5.02435071e-09, 0.224748924, -2.64490758e-08, -0.974416733)
        CFramePuk = CFrame.new(-1133.4574, 40.8067436, -526.086792, 0.647179008, -2.76535794e-10, 0.762338042, 3.26674865e-08, 1, -2.73699801e-08, -0.762338042, 4.26169464e-08, 0.647179008)
        elseif lv == 30 or lv <= 59 then
        Mon = "Pirate [Lv. 35]"
        Title = "Pirate"
        QuestName = "BuggyQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1139.88965, 4.7520504, 3827.90503, -0.95198369, -7.75120483e-08, 0.306148738, -6.30059915e-08, 1, 5.72642094e-08, -0.306148738, 3.52253871e-08, -0.95198369)
        CFrameMon = CFrame.new(-1215.88757, 4.7520504, 3911.45483, -0.948559701, 1.90610709e-08, 0.316598237, 1.40048027e-08, 1, -1.82460873e-08, -0.316598237, -1.28736071e-08, -0.948559701)
        CFramePuk = CFrame.new(-1102.82251, 13.7520409, 3897.0918, 0.34478578, 7.98670641e-08, 0.938681364, -8.6188912e-08, 1, -5.34263798e-08, -0.938681364, -6.24832666e-08, 0.34478578)
        elseif lv == 60 or lv <= 74 then
        Mon = "Desert Bandit [Lv. 60]"
        Title = "Desert Bandit"
        QuestName = "DesertQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(896.22998, 6.43846273, 4389.97314, -0.810346186, -1.22518671e-08, 0.585951447, -7.40761976e-08, 1, -8.15349068e-08, -0.585951447, -1.09476559e-07, -0.810346186)
        CFrameMon = CFrame.new(916.301697, 6.44910288, 4465.08936, -0.879750133, 5.01538153e-08, 0.47543633, 1.81982003e-08, 1, -7.1816018e-08, -0.47543633, -5.45280692e-08, -0.879750133)
        CFramePuk = CFrame.new(907.621094, 15.2893982, 4569.33301, 0.997965753, 4.14430845e-09, -0.0637524351, -4.89009677e-09, 1, -1.15421592e-08, 0.0637524351, 1.18304344e-08, 0.997965753)
        elseif lv == 75 or lv <= 89 then
        Mon = "Desert Officers [Lv. 75]"
        Title = "Desert Officers"
        QuestName = "DesertQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(896.22998, 6.43846273, 4389.97314, -0.810346186, -1.22518671e-08, 0.585951447, -7.40761976e-08, 1, -8.15349068e-08, -0.585951447, -1.09476559e-07, -0.810346186)
        CFrameMon = CFrame.new(1106.35938, 105.771019, -1447.26941, 0.959117353, 8.90850327e-09, -0.283008605, -7.54482521e-09, 1, 5.90840799e-09, 0.283008605, -3.53160634e-09, 0.959117353)
        CFramePuk = CFrame.new(1070.2074, 128.426575, -1419.05676, 0.804665864, -2.49654608e-08, -0.593727946, -7.79732012e-09, 1, -5.26161834e-08, 0.593727946, 4.69679335e-08, 0.804665864)
        elseif lv == 90 or lv <= 99 then
        Mon = "Snow Bandit [Lv. 90]"
        Title = "Snow Bandit"
        QuestName = "SnowQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1386.0033, 87.2727661, -1298.39661, 0.159108937, -2.90485733e-08, -0.987260997, -1.67417067e-08, 1, -3.21215268e-08, 0.987260997, 2.16392557e-08, 0.159108937)
        CFrameMon = CFrame.new(1315.17627, 87.2727661, -1398.82874, 0.600238323, 2.80005263e-09, 0.799821198, -3.3809191e-09, 1, -9.63584657e-10, -0.799821198, -2.12575046e-09, 0.600238323)
        CFramePuk = CFrame.new(1384.10522, 88.0562744, -1399.72559, -0.298243642, 5.96704958e-05, 0.954489768, 1.56380211e-05, 1, -5.76292805e-05, -0.954489768, -2.26123484e-06, -0.298243642)
        elseif lv == 100 or lv <= 119 then
        Mon = "Snowman [Lv. 100]"
        Title = "Snowman"
        QuestName = "SnowQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(1386.0033, 87.2727661, -1298.39661, 0.159108937, -2.90485733e-08, -0.987260997, -1.67417067e-08, 1, -3.21215268e-08, 0.987260997, 2.16392557e-08, 0.159108937)
        CFrameMon = CFrame.new(1331.1731, 87.2727661, -1403.21533, -0.936040282, -6.82415404e-08, -0.351892859, -6.86833133e-08, 1, -1.1228388e-08, 0.351892859, 1.36589442e-08, -0.936040282)
        CFramePuk = CFrame.new(1383.62964, 88.2521515, -1400.70789, -0.0657547936, -6.38455901e-08, 0.997835815, -5.11353271e-08, 1, 6.06143828e-08, -0.997835815, -4.70389736e-08, -0.0657547936)
        elseif lv == 120 or lv <= 149 then
        Mon = "Chief Petty Officer [Lv. 120]"
        Title = "Chief Petty Officer"
        QuestName = "MarineQuest2"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5037.15771, 28.6778202, 4325.00684, -0.0731988624, -2.59374815e-08, 0.997317374, -4.73310386e-08, 1, 2.2533353e-08, -0.997317374, -4.55546498e-08, -0.0731988624)
        CFrameMon = CFrame.new(-4661.94287, 20.6778202, 4418.93311, 0.926162243, 4.56484983e-08, 0.377125233, -4.73508486e-08, 1, -4.75685846e-09, -0.377125233, -1.34515767e-08, 0.926162243)
        CFramePuk = CFrame.new(-4601.92969, 56.1800232, 4411.21338, 0.67949599, 5.56269768e-08, 0.733679175, -6.24450394e-08, 1, -1.79858226e-08, -0.733679175, -3.35933308e-08, 0.67949599)
        elseif lv == 150 or lv <= 174 then
        Mon = "Sky Bandit [Lv. 150]"
        Title = "Sky Bandit"
        QuestName = "SkyQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-4840.30273, 717.695129, -2620.95679, -0.847650766, 4.5544656e-08, -0.530554593, 1.61341696e-08, 1, 6.00664194e-08, 0.530554593, 4.23552891e-08, -0.847650766)
        CFrameMon = CFrame.new(-4929.18701, 278.091858, -2838.04004, -0.297278345, 4.9028186e-09, -0.954790831, 2.28252972e-08, 1, -1.9717914e-09, 0.954790831, -2.2379556e-08, -0.297278345)
        CFramePuk = CFrame.new(-4955.46875, 295.769989, -2898.77271, 0.996960938, 3.85883752e-08, 0.077903375, -3.26949774e-08, 1, -7.69255593e-08, -0.077903375, 7.41447295e-08, 0.996960938)
        elseif lv == 175 or lv <= 189 then
        Mon = "Dark Master [Lv. 175]"
        Title = "Dark Master"
        QuestName = "SkyQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-4840.30273, 717.695129, -2620.95679, -0.847650766, 4.5544656e-08, -0.530554593, 1.61341696e-08, 1, 6.00664194e-08, 0.530554593, 4.23552891e-08, -0.847650766)
        CFrameMon = CFrame.new(-5270.30957, 388.677734, -2267.552, 0.531413496, -7.30369791e-08, -0.847112596, 1.14061166e-07, 1, -1.4665515e-08, 0.847112596, -8.88291964e-08, 0.531413496)
        CFramePuk = CFrame.new(-5224.9917, 429.902802, -2278.28247, -0.614156365, 1.17443903e-08, 0.789184391, 1.55013797e-08, 1, -2.81825097e-09, -0.789184391, 1.05025997e-08, -0.614156365)
        elseif lv == 190 or lv <= 209 then
        Mon = "Prisoner [Lv. 190]"
        Title = "Prisoner"
        QuestName = "PrisonerQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(5113.50293, 0.205914706, 469.620941, -0.634902835, 8.16982215e-09, 0.772592008, 4.75692126e-08, 1, 2.85169985e-08, -0.772592008, 5.48571144e-08, -0.634902835)
        CFrameMon = CFrame.new(5363.46484, 1.65915167, 426.865723, -0.287108511, -1.14441145e-09, -0.95789808, 3.63262949e-08, 1, -1.20827055e-08, 0.95789808, -3.8265938e-08, -0.287108511)
        CFramePuk = CFrame.new(5113.50293, 0.205914706, 469.620941, -0.634902835, 8.16982215e-09, 0.772592008, 4.75692126e-08, 1, 2.85169985e-08, -0.772592008, 5.48571144e-08, -0.634902835)
        elseif lv == 210 or lv <= 224 then
        Mon = "Dangerous Prisoner [Lv. 210]"
        Title = "Dangerous Prisoner"
        QuestName = "PrisonerQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(5113.50293, 0.205914706, 469.620941, -0.634902835, 8.16982215e-09, 0.772592008, 4.75692126e-08, 1, 2.85169985e-08, -0.772592008, 5.48571144e-08, -0.634902835)
        CFrameMon = CFrame.new(5500.78564, 0.952296555, 1012.77899, -0.929960787, -9.19636705e-08, 0.367658705, -9.08889959e-08, 1, 2.02374242e-08, -0.367658705, -1.4596119e-08, -0.929960787)
        CFramePuk = CFrame.new(5429.0752, 1.67767107, 1042.24902, -0.193744212, 1.85586853e-08, 0.981052101, -5.7973363e-08, 1, -3.03660634e-08, -0.981052101, -6.275814e-08, -0.193744212)
        elseif lv == 225 or lv <= 274 then
        Mon = "Toga Warrior [Lv. 250]"
        Title = "Toga Warrior"
        QuestName = "ColosseumQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1577.70129, 7.41512585, -2984.88794, 0.570523262, -1.8461348e-08, 0.821281433, 2.36739406e-09, 1, 2.08341433e-08, -0.821281433, -9.94206673e-09, 0.570523262)
        CFrameMon = CFrame.new(-1803.3092, 7.46833324, -2853.92993, 0.510445118, 8.66911947e-08, -0.859910369, -8.71798633e-08, 1, 4.9064024e-08, 0.859910369, 4.99223773e-08, 0.510445118)
        CFramePuk = CFrame.new(-1778.61353, 43.802063, -2737.51343, -0.872123301, -8.75902941e-08, 0.489286125, -7.34171124e-08, 1, 4.81548916e-08, -0.489286125, 6.07502759e-09, -0.872123301)
        elseif lv == 275 or lv <= 299 then
        Mon = "Gladiator [Lv. 275]"
        Title = "Gladiator"
        QuestName = "ColosseumQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1577.70129, 7.41512585, -2984.88794, 0.570523262, -1.8461348e-08, 0.821281433, 2.36739406e-09, 1, 2.08341433e-08, -0.821281433, -9.94206673e-09, 0.570523262)
        CFrameMon = CFrame.new(-1269.81189, 58.7645569, -3183.03906, 0.146738812, -2.70176788e-08, 0.98917526, 1.61042113e-08, 1, 2.49243648e-08, -0.98917526, 1.22725163e-08, 0.146738812)
        CFramePuk = CFrame.new(-1290.80139, 7.46833324, -3235.68481, 0.886816263, -8.97978296e-08, -0.462122172, 8.71031816e-08, 1, -2.71644804e-08, 0.462122172, -1.61624101e-08, 0.886816263)
        elseif lv == 300 or lv <= 329 then
        Mon = "Military Soldier [Lv. 300]"
        Title = "Military Soldier"
        QuestName = "MagmaQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5315.22168, 12.2625732, 8516.74023, 0.560634196, 2.15887699e-08, -0.828063548, 5.69708458e-09, 1, 2.9928561e-08, 0.828063548, -2.14965237e-08, 0.560634196)
        CFrameMon = CFrame.new(-5475.31738, 8.61646175, 8467.87988, 0.990054905, -1.33513884e-08, -0.140681356, 9.18453136e-09, 1, -3.02683851e-08, 0.140681356, 2.86752737e-08, 0.990054905)
        CFramePuk = CFrame.new(-5525.55713, 46.9433594, 8507.68359, 0.273948908, 0, 0.961744249, 0, 1, 0, -0.961744249, 0, 0.273948908)
        elseif lv == 330 or lv <= 374 then
        Mon = "Military Spy [Lv. 330]"
        Title = "Military Spy"
        QuestName = "MagmaQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-5315.22168, 12.2625732, 8516.74023, 0.560634196, 2.15887699e-08, -0.828063548, 5.69708458e-09, 1, 2.9928561e-08, 0.828063548, -2.14965237e-08, 0.560634196)
        CFrameMon = CFrame.new(-5839.32666, 77.256424, 8814.23828, 0.200517297, -3.12384749e-08, 0.979690135, -4.7199471e-08, 1, 4.15465919e-08, -0.979690135, -5.45716681e-08, 0.200517297)
        CFramePuk = CFrame.new(-5767.75732, 122.01947, 8804.89648, 0.214001924, -4.70807144e-08, -0.976833224, 5.41794343e-08, 1, -3.63278119e-08, 0.976833224, -4.5150049e-08, 0.214001924)
    end
end

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
totarget(CFrameQuest)
wait(.3)
local args = {
    [1] = "StartQuest",
    [2] = QuestName,
    [3] = QuestNumber
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        for i,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon and v2.Name == Mon then
            totarget(v.HumanoidRootPart.CFrame * CFrame.new(0,1,15))
            v.HumanoidRootPart.Size = Vector3.new(60,2.5,60)
            v.HumanoidRootPart.CFrame = CFrameMon
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
            v2.HumanoidRootPart.CanCollide = false
            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
        end
        end
    end
                end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
    if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, Title) then
local args = {
    [1] = "AbandonQuest"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            if not game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
                totarget(CFramePuk)
            end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon then
            if v.Humanoid.Health == 0 then
            v:Destroy()
            end
            end
            end
            end
        end)
    end
end)
    end)
    
Tab1 = Library:Tab("fruit")
    
Tab1:Button("buyfruit",function()
    local args = {
    [1] = "Cousin",
    [2] = "Buy"
}

game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))
end)local ScreenGui = Instance.new("ScreenGui")
    local Toggle = Instance.new("TextButton")
    
    ScreenGui.Name = "ScreenGui"
    ScreenGui.Parent = game.CoreGui
    
    Toggle.Name = "Toggle"
    Toggle.Parent = ScreenGui
    Toggle.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
    Toggle.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)
    Toggle.Size = UDim2.new(0, 50, 0, 50)
    Toggle.Font = Enum.Font.Code
    Toggle.Text = "M"
    Toggle.TextColor3 = Color3.fromRGB(255, 0, 0)
    Toggle.TextScaled = true
    Toggle.MouseButton1Down:connect(function()
        game:GetService("VirtualInputManager"):SendKeyEvent(true,305,false,game)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,305,false,game)
    end)

local DarkraiX = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Kavo-Ui/main/Darkrai%20Ui", true))()

local Library = DarkraiX:Window("Darkrai X","","",Enum.KeyCode.RightControl);
Tab1 = Library:Tab("Credit")

Tab1:Button("Discord [Copy]",function()
    setclipboard("https://discord.gg/YFWNKr2N")
end)
Tab1:Button("YouTube [Copy]",function()
    setclipboard("Perfect v")
end)

Tab1 = Library:Tab("Main")

Tab1:Toggle("white screen",false,function(state)
if state then
    game:GetService("RunService"):Set3dRenderingEnabled(false)
else
    game:GetService("RunService"):Set3dRenderingEnabled(true)
    end
    end)
    

    
    
Tab1:Toggle("auto farm",false,function(value)
_G.Auto_Farm = value 

function totarget(p)
    local Distance2 = (p.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
    local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = p})
    tween:Play()
    if Distance2 <= 75 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
    end
end

function checklevel()
    local lv = game:GetService("Players").LocalPlayer.Data.Level.Value
    if lv == 1 or lv <= 9 then
        Mon = "Bandit [Lv. 5]"
        Title = "Bandit"
        QuestName = "BanditQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1061.15271, 16.7367725, 1548.93018, -0.836085379, -3.89774577e-08, 0.548599303, -1.17575967e-08, 1, 5.31300408e-08, -0.548599303, 3.79710414e-08, -0.836085379)
        CFrameMon = CFrame.new(1151.11829, 16.7761021, 1599.73499, -0.999999762, 0, -0.000701809535, 0, 1, 0, 0.000701809535, 0, -0.999999762)
        CFramePuk = CFrame.new(1101.75903, 67.6758957, 1617.50391, -0.399259984, -5.24373327e-08, -0.916837752, -1.74068084e-08, 1, -4.96134582e-08, 0.916837752, -3.84945009e-09, -0.399259984)
    elseif lv == 10 or lv <= 14 then
        Mon = "Monkey [Lv. 14]"
        Title = "Monkey"
        QuestName = "JungleQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1479.76099, 23.195364, 106.327942, 0.96289885, 5.22265786e-10, -0.269862473, 6.59528099e-10, 1, 4.28857172e-09, 0.269862473, -4.30744285e-09, 0.96289885)
        CFramePuk = CFrame.new(-1776.32959, 61.1782455, 66.8902054, -0.912609756, -2.38546143e-08, 0.408831745, -2.14773621e-08, 1, 1.04056577e-08, -0.408831745, 7.15677129e-10, -0.912609756)
        elseif lv == 15 or lv <= 29 then
        Mon = "Gorilla [Lv. 20]"
        Title = "Gorilla"
        QuestName = "JungleQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1242.46655, 6.62262297, -523.166382, -0.974416733, 9.23166681e-08, -0.224748924, 9.58993027e-08, 1, -5.02435071e-09, 0.224748924, -2.64490758e-08, -0.974416733)
        CFramePuk = CFrame.new(-1133.4574, 40.8067436, -526.086792, 0.647179008, -2.76535794e-10, 0.762338042, 3.26674865e-08, 1, -2.73699801e-08, -0.762338042, 4.26169464e-08, 0.647179008)
        elseif lv == 30 or lv <= 59 then
        Mon = "Pirate [Lv. 35]"
        Title = "Pirate"
        QuestName = "BuggyQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1139.88965, 4.7520504, 3827.90503, -0.95198369, -7.75120483e-08, 0.306148738, -6.30059915e-08, 1, 5.72642094e-08, -0.306148738, 3.52253871e-08, -0.95198369)
        CFrameMon = CFrame.new(-1215.88757, 4.7520504, 3911.45483, -0.948559701, 1.90610709e-08, 0.316598237, 1.40048027e-08, 1, -1.82460873e-08, -0.316598237, -1.28736071e-08, -0.948559701)
        CFramePuk = CFrame.new(-1102.82251, 13.7520409, 3897.0918, 0.34478578, 7.98670641e-08, 0.938681364, -8.6188912e-08, 1, -5.34263798e-08, -0.938681364, -6.24832666e-08, 0.34478578)
        elseif lv == 60 or lv <= 74 then
        Mon = "Desert Bandit [Lv. 60]"
        Title = "Desert Bandit"
        QuestName = "DesertQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(896.22998, 6.43846273, 4389.97314, -0.810346186, -1.22518671e-08, 0.585951447, -7.40761976e-08, 1, -8.15349068e-08, -0.585951447, -1.09476559e-07, -0.810346186)
        CFrameMon = CFrame.new(916.301697, 6.44910288, 4465.08936, -0.879750133, 5.01538153e-08, 0.47543633, 1.81982003e-08, 1, -7.1816018e-08, -0.47543633, -5.45280692e-08, -0.879750133)
        CFramePuk = CFrame.new(907.621094, 15.2893982, 4569.33301, 0.997965753, 4.14430845e-09, -0.0637524351, -4.89009677e-09, 1, -1.15421592e-08, 0.0637524351, 1.18304344e-08, 0.997965753)
        elseif lv == 75 or lv <= 89 then
        Mon = "Desert Officers [Lv. 75]"
        Title = "Desert Officers"
        QuestName = "DesertQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(896.22998, 6.43846273, 4389.97314, -0.810346186, -1.22518671e-08, 0.585951447, -7.40761976e-08, 1, -8.15349068e-08, -0.585951447, -1.09476559e-07, -0.810346186)
        CFrameMon = CFrame.new(1106.35938, 105.771019, -1447.26941, 0.959117353, 8.90850327e-09, -0.283008605, -7.54482521e-09, 1, 5.90840799e-09, 0.283008605, -3.53160634e-09, 0.959117353)
        CFramePuk = CFrame.new(1070.2074, 128.426575, -1419.05676, 0.804665864, -2.49654608e-08, -0.593727946, -7.79732012e-09, 1, -5.26161834e-08, 0.593727946, 4.69679335e-08, 0.804665864)
        elseif lv == 90 or lv <= 99 then
        Mon = "Snow Bandit [Lv. 90]"
        Title = "Snow Bandit"
        QuestName = "SnowQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1386.0033, 87.2727661, -1298.39661, 0.159108937, -2.90485733e-08, -0.987260997, -1.67417067e-08, 1, -3.21215268e-08, 0.987260997, 2.16392557e-08, 0.159108937)
        CFrameMon = CFrame.new(1315.17627, 87.2727661, -1398.82874, 0.600238323, 2.80005263e-09, 0.799821198, -3.3809191e-09, 1, -9.63584657e-10, -0.799821198, -2.12575046e-09, 0.600238323)
        CFramePuk = CFrame.new(1384.10522, 88.0562744, -1399.72559, -0.298243642, 5.96704958e-05, 0.954489768, 1.56380211e-05, 1, -5.76292805e-05, -0.954489768, -2.26123484e-06, -0.298243642)
        elseif lv == 100 or lv <= 119 then
        Mon = "Snowman [Lv. 100]"
        Title = "Snowman"
        QuestName = "SnowQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(1386.0033, 87.2727661, -1298.39661, 0.159108937, -2.90485733e-08, -0.987260997, -1.67417067e-08, 1, -3.21215268e-08, 0.987260997, 2.16392557e-08, 0.159108937)
        CFrameMon = CFrame.new(1331.1731, 87.2727661, -1403.21533, -0.936040282, -6.82415404e-08, -0.351892859, -6.86833133e-08, 1, -1.1228388e-08, 0.351892859, 1.36589442e-08, -0.936040282)
        CFramePuk = CFrame.new(1383.62964, 88.2521515, -1400.70789, -0.0657547936, -6.38455901e-08, 0.997835815, -5.11353271e-08, 1, 6.06143828e-08, -0.997835815, -4.70389736e-08, -0.0657547936)
        elseif lv == 120 or lv <= 149 then
        Mon = "Chief Petty Officer [Lv. 120]"
        Title = "Chief Petty Officer"
        QuestName = "MarineQuest2"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5037.15771, 28.6778202, 4325.00684, -0.0731988624, -2.59374815e-08, 0.997317374, -4.73310386e-08, 1, 2.2533353e-08, -0.997317374, -4.55546498e-08, -0.0731988624)
        CFrameMon = CFrame.new(-4661.94287, 20.6778202, 4418.93311, 0.926162243, 4.56484983e-08, 0.377125233, -4.73508486e-08, 1, -4.75685846e-09, -0.377125233, -1.34515767e-08, 0.926162243)
        CFramePuk = CFrame.new(-4601.92969, 56.1800232, 4411.21338, 0.67949599, 5.56269768e-08, 0.733679175, -6.24450394e-08, 1, -1.79858226e-08, -0.733679175, -3.35933308e-08, 0.67949599)
        elseif lv == 150 or lv <= 174 then
        Mon = "Sky Bandit [Lv. 150]"
        Title = "Sky Bandit"
        QuestName = "SkyQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-4840.30273, 717.695129, -2620.95679, -0.847650766, 4.5544656e-08, -0.530554593, 1.61341696e-08, 1, 6.00664194e-08, 0.530554593, 4.23552891e-08, -0.847650766)
        CFrameMon = CFrame.new(-4929.18701, 278.091858, -2838.04004, -0.297278345, 4.9028186e-09, -0.954790831, 2.28252972e-08, 1, -1.9717914e-09, 0.954790831, -2.2379556e-08, -0.297278345)
        CFramePuk = CFrame.new(-4955.46875, 295.769989, -2898.77271, 0.996960938, 3.85883752e-08, 0.077903375, -3.26949774e-08, 1, -7.69255593e-08, -0.077903375, 7.41447295e-08, 0.996960938)
        elseif lv == 175 or lv <= 189 then
        Mon = "Dark Master [Lv. 175]"
        Title = "Dark Master"
        QuestName = "SkyQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-4840.30273, 717.695129, -2620.95679, -0.847650766, 4.5544656e-08, -0.530554593, 1.61341696e-08, 1, 6.00664194e-08, 0.530554593, 4.23552891e-08, -0.847650766)
        CFrameMon = CFrame.new(-5270.30957, 388.677734, -2267.552, 0.531413496, -7.30369791e-08, -0.847112596, 1.14061166e-07, 1, -1.4665515e-08, 0.847112596, -8.88291964e-08, 0.531413496)
        CFramePuk = CFrame.new(-5224.9917, 429.902802, -2278.28247, -0.614156365, 1.17443903e-08, 0.789184391, 1.55013797e-08, 1, -2.81825097e-09, -0.789184391, 1.05025997e-08, -0.614156365)
        elseif lv == 190 or lv <= 209 then
        Mon = "Prisoner [Lv. 190]"
        Title = "Prisoner"
        QuestName = "PrisonerQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(5113.50293, 0.205914706, 469.620941, -0.634902835, 8.16982215e-09, 0.772592008, 4.75692126e-08, 1, 2.85169985e-08, -0.772592008, 5.48571144e-08, -0.634902835)
        CFrameMon = CFrame.new(5363.46484, 1.65915167, 426.865723, -0.287108511, -1.14441145e-09, -0.95789808, 3.63262949e-08, 1, -1.20827055e-08, 0.95789808, -3.8265938e-08, -0.287108511)
        CFramePuk = CFrame.new(5113.50293, 0.205914706, 469.620941, -0.634902835, 8.16982215e-09, 0.772592008, 4.75692126e-08, 1, 2.85169985e-08, -0.772592008, 5.48571144e-08, -0.634902835)
        elseif lv == 210 or lv <= 224 then
        Mon = "Dangerous Prisoner [Lv. 210]"
        Title = "Dangerous Prisoner"
        QuestName = "PrisonerQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(5113.50293, 0.205914706, 469.620941, -0.634902835, 8.16982215e-09, 0.772592008, 4.75692126e-08, 1, 2.85169985e-08, -0.772592008, 5.48571144e-08, -0.634902835)
        CFrameMon = CFrame.new(5500.78564, 0.952296555, 1012.77899, -0.929960787, -9.19636705e-08, 0.367658705, -9.08889959e-08, 1, 2.02374242e-08, -0.367658705, -1.4596119e-08, -0.929960787)
        CFramePuk = CFrame.new(5429.0752, 1.67767107, 1042.24902, -0.193744212, 1.85586853e-08, 0.981052101, -5.7973363e-08, 1, -3.03660634e-08, -0.981052101, -6.275814e-08, -0.193744212)
        elseif lv == 225 or lv <= 274 then
        Mon = "Toga Warrior [Lv. 250]"
        Title = "Toga Warrior"
        QuestName = "ColosseumQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1577.70129, 7.41512585, -2984.88794, 0.570523262, -1.8461348e-08, 0.821281433, 2.36739406e-09, 1, 2.08341433e-08, -0.821281433, -9.94206673e-09, 0.570523262)
        CFrameMon = CFrame.new(-1803.3092, 7.46833324, -2853.92993, 0.510445118, 8.66911947e-08, -0.859910369, -8.71798633e-08, 1, 4.9064024e-08, 0.859910369, 4.99223773e-08, 0.510445118)
        CFramePuk = CFrame.new(-1778.61353, 43.802063, -2737.51343, -0.872123301, -8.75902941e-08, 0.489286125, -7.34171124e-08, 1, 4.81548916e-08, -0.489286125, 6.07502759e-09, -0.872123301)
        elseif lv == 275 or lv <= 299 then
        Mon = "Gladiator [Lv. 275]"
        Title = "Gladiator"
        QuestName = "ColosseumQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1577.70129, 7.41512585, -2984.88794, 0.570523262, -1.8461348e-08, 0.821281433, 2.36739406e-09, 1, 2.08341433e-08, -0.821281433, -9.94206673e-09, 0.570523262)
        CFrameMon = CFrame.new(-1269.81189, 58.7645569, -3183.03906, 0.146738812, -2.70176788e-08, 0.98917526, 1.61042113e-08, 1, 2.49243648e-08, -0.98917526, 1.22725163e-08, 0.146738812)
        CFramePuk = CFrame.new(-1290.80139, 7.46833324, -3235.68481, 0.886816263, -8.97978296e-08, -0.462122172, 8.71031816e-08, 1, -2.71644804e-08, 0.462122172, -1.61624101e-08, 0.886816263)
        elseif lv == 300 or lv <= 329 then
        Mon = "Military Soldier [Lv. 300]"
        Title = "Military Soldier"
        QuestName = "MagmaQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-5315.22168, 12.2625732, 8516.74023, 0.560634196, 2.15887699e-08, -0.828063548, 5.69708458e-09, 1, 2.9928561e-08, 0.828063548, -2.14965237e-08, 0.560634196)
        CFrameMon = CFrame.new(-5475.31738, 8.61646175, 8467.87988, 0.990054905, -1.33513884e-08, -0.140681356, 9.18453136e-09, 1, -3.02683851e-08, 0.140681356, 2.86752737e-08, 0.990054905)
        CFramePuk = CFrame.new(-5525.55713, 46.9433594, 8507.68359, 0.273948908, 0, 0.961744249, 0, 1, 0, -0.961744249, 0, 0.273948908)
        elseif lv == 330 or lv <= 374 then
        Mon = "Military Spy [Lv. 330]"
        Title = "Military Spy"
        QuestName = "MagmaQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-5315.22168, 12.2625732, 8516.74023, 0.560634196, 2.15887699e-08, -0.828063548, 5.69708458e-09, 1, 2.9928561e-08, 0.828063548, -2.14965237e-08, 0.560634196)
        CFrameMon = CFrame.new(-5839.32666, 77.256424, 8814.23828, 0.200517297, -3.12384749e-08, 0.979690135, -4.7199471e-08, 1, 4.15465919e-08, -0.979690135, -5.45716681e-08, 0.200517297)
        CFramePuk = CFrame.new(-5767.75732, 122.01947, 8804.89648, 0.214001924, -4.70807144e-08, -0.976833224, 5.41794343e-08, 1, -3.63278119e-08, 0.976833224, -4.5150049e-08, 0.214001924)
    end
end

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
totarget(CFrameQuest)
wait(.3)
local args = {
    [1] = "StartQuest",
    [2] = QuestName,
    [3] = QuestNumber
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        for i,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon and v2.Name == Mon then
            totarget(v.HumanoidRootPart.CFrame * CFrame.new(0,1,15))
            v.HumanoidRootPart.Size = Vector3.new(60,2.5,60)
            v.HumanoidRootPart.CFrame = CFrameMon
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
            v2.HumanoidRootPart.CanCollide = false
            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
        end
        end
    end
                end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
    if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, Title) then
local args = {
    [1] = "AbandonQuest"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            if not game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
                totarget(CFramePuk)
            end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon then
            if v.Humanoid.Health == 0 then
            v:Destroy()
            end
            end
            end
            end
        end)
    end
end)
    end)
    
Tab1 = Library:Tab("fruit")
    
Tab1:Button("buyfruit",function()
    local args = {
    [1] = "Cousin",
    [2] = "Buy"
}

game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))
end
