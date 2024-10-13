local LBLG = Instance.new("ScreenGui", getParent)
local LBL = Instance.new("TextLabel", getParent)
local player = game.Players.LocalPlayer

LBLG.Name = "LBLG"
LBLG.Parent = game.CoreGui
LBLG.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
LBLG.Enabled = true
LBL。Name = "LBL "
LBL。Parent = LBLG
LBL。BackgroundColor3 = Color3.new(1，1，1)
LBL。BackgroundTransparency = 1
LBL。BorderColor3 = Color3.new(0，0，0)
LBL。Position = UDim2.new(0.75，0，0.010，0)
LBL。Size = UDim2.new(0，133，0，30)
LBL。Font = Enum。字体. GothamSemibold
LBL。Text = "TextLabel "
LBL。TextColor3 = Color3.new(1，1，1)
LBL。TextScaled = true
LBL。TextSize = 14
LBL。TextWrapped = true
LBL。可见=真

本地FpsLabel = LBL
本地心跳= game:get service(“run service”)。心跳
本地最后一次迭代，开始
本地FrameUpdateTable = { }

本地函数HeartbeatUpdate()
LastIteration = tick()
对于Index = #FrameUpdateTable，1，-1 do
FrameUpdateTable[指数+ 1]= (FrameUpdateTable[索引]> = LastIteration - 1)和FrameUpdateTable[索引]或零
结束
FrameUpdateTable[1]=最后一次迭代
local current fps =(tick()-Start > = 1且#FrameUpdateTable)或(# frame updatetable/(tick()-Start))
current fps = current fps-current fps % 1
FpsLabel。Text =("时间:"..os.date("%H ").."时"..os.date("%M ").."分"..os.date("%S "))
结束
Start = tick()
心跳:连接(心跳更新)
游戏:get service(" starter GUI "):set core(" send notification "，{ Title = "と傻猫脚本』";Text = "核对用户身份证明中♧";持续时间= 2；})
游戏:get service(" starter GUI "):set core(" send notification "，{ Title = "と傻猫脚本』";Text = "用户身份证明核对完毕♣";持续时间= 4；})

local ui = loadstring(game:http get(" https://raw . githubusercontent . com/ding ding 123 hhh/hun/main/jmlibrary 1 . Lua ")))；        
local win = ui:new("傻猫脚本")
--
local UITab1 = win:Tab("『信息』",'7734068321')

local about = UITab1:section("『作者信息』",false)

about:Label("傻猫脚本")
about:Label("作者QQ：2089142678")
about:Label("作者：一只小傻猫")
about:Label("脚本持续更新中")
about:Label("脚本疯狂优化中")

local about = UITab1:section("『玩家信息』",false)

about:Label("你的账号年龄:"..player.AccountAge.."天")
about:Label("你的注入器:"..identifyexecutor())
about:Label("你的用户名:"..game.Players.LocalPlayer.Character.Name)
about:Label("你现在的服务器名称:"..game:GetService("MarketplaceService"):GetProductInfo(game.PlaceId).Name)
about:Label("你现在的服务器id:"..game.GameId)
about:Label("你的用户ID:"..game.Players.LocalPlayer.UserId)
about:Label("获取客户端ID:"..game:GetService("RbxAnalyticsService"):GetClientId())


local UITab2 = win:Tab("『公告』",'7734068321')

local about = UITab2:section("『公告』",true)

about:Label("感谢所有支持傻猫脚本的人")
about:Label("已修复完bug")
about:Label("♦")
about:Label("       ")
about:Label("感谢大家支持傻猫脚本")


local UITab3 = win:Tab("『通用』",'7734068321')

local about = UITab3:section("『通用』",true)

about:Button("玩家加入游戏提示",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/boyscp/scriscriptsc/main/bbn.lua"))()
end)

about:Button("获得管理员权限",function()
loadstring(game:HttpGet("https://pastebin.com/raw/sZpgTVas"))()
end)

about:Button("死亡笔记",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/tt/main/%E6%AD%BB%E4%BA%A1%E7%AC%94%E8%AE%B0%20(1).txt"))()
end)

about:Button("汉化穿墙",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/TtmScripter/OtherScript/main/Noclip"))()
end)
    
about:Button("飞行",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/tt/main/jm%E9%A3%9E..lua"))()
end)

about:Button("透视",function()  
    _G.FriendColor = Color3.fromRGB(0, 0, 255)
        local function ApplyESP(v)
       if v.Character and v.Character:FindFirstChildOfClass'Humanoid' then
           v.Character.Humanoid.NameDisplayDistance = 9e9
           v.Character.Humanoid.NameOcclusion = "NoOcclusion"
           v.Character.Humanoid.HealthDisplayDistance = 9e9
           v.Character.Humanoid.HealthDisplayType = "AlwaysOn"
           v.Character.Humanoid.Health = v.Character.Humanoid.Health -- triggers changed
       end
    end
    for i,v in pairs(game.Players:GetPlayers()) do
       ApplyESP(v)
       v.CharacterAdded:Connect(function()
           task.wait(0.33)
           ApplyESP(v)
       end)
    end
    
    game.Players.PlayerAdded:Connect(function(v)
       ApplyESP(v)
       v.CharacterAdded:Connect(function()
           task.wait(0.33)
           ApplyESP(v)
       end)
    end)
    
        local Players = game:GetService("Players"):GetChildren()
    local RunService = game:GetService("RunService")
    local highlight = Instance.new("Highlight")
    highlight.Name = "Highlight"
    
    for i, v in pairs(Players) do
        repeat wait() until v.Character
        if not v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
            local highlightClone = highlight:Clone()
            highlightClone.Adornee = v.Character
            highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
            highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            highlightClone.Name = "Highlight"
        end
    end
    
    game.Players.PlayerAdded:Connect(function(player)
        repeat wait() until player.Character
        if not player.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
            local highlightClone = highlight:Clone()
            highlightClone.Adornee = player.Character
            highlightClone.Parent = player.Character:FindFirstChild("HumanoidRootPart")
            highlightClone.Name = "Highlight"
        end
    end)
    
    game.Players.PlayerRemoving:Connect(function(playerRemoved)
        playerRemoved.Character:FindFirstChild("HumanoidRootPart").Highlight:Destroy()
    end)
    
    RunService.Heartbeat:Connect(function()
        for i, v in pairs(Players) do
            repeat wait() until v.Character
            if not v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
                local highlightClone = highlight:Clone()
                highlightClone.Adornee = v.Character
                highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
                highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
                highlightClone.Name = "Highlight"
                task.wait()
            end
    end
    end)
    end)

about:Toggle("夜视","Toggle",false,function(Value)
if Value then

		    game.Lighting.Ambient = Color3.new(1, 1, 1)

		else

		    game.Lighting.Ambient = Color3.new(0, 0, 0)

		end
end)

about:Toggle("自动互动", "Auto Interact", false, function(state)
        if state then
            autoInteract = true
            while autoInteract do
                for _, descendant in pairs(workspace:GetDescendants()) do
                    if descendant:IsA("ProximityPrompt") then
                        fireproximityprompt(descendant)
                    end
                end
                task.wait(0.25) -- Adjust the wait time as needed
            end
        else
            autoInteract = false
        end
    end)

about:Toggle("无限跳","Toggle",false,function(Value)
        Jump = Value
        game.UserInputService.JumpRequest:Connect(function()
            if Jump then
                game.Players.LocalPlayer.Character.Humanoid:ChangeState("Jumping")
            end
        end)
    end)

about:Slider("步行速度!", "WalkSpeed", game.Players.LocalPlayer.Character.Humanoid.WalkSpeed, 16, 400, false, function(Speed)
  spawn(function() while task.wait() do game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Speed end end)
end)

about:Slider("跳跃高度!", "JumpPower", game.Players.LocalPlayer.Character.Humanoid.JumpPower, 50, 400, false, function(Jump)
  spawn(function() while task.wait() do game.Players.LocalPlayer.Character.Humanoid.JumpPower = Jump end end)
end)

about:Button("甩人",function()
loadstring(game:HttpGet("https://pastebin.com/raw/zqyDSUWX"))()
end)
about:Slider('设置重力', 'Sliderflag', 196.2, 196.2, 1000,false, function(Value)
        game.Workspace.Gravity = Value
    end)
    
about:Button("替身",function()
loadstring(game:HttpGet(('https://raw.githubusercontent.com/SkrillexMe/SkrillexLoader/main/SkrillexLoadMain')))()
end)

about:Button("爬墙",function()
loadstring(game:HttpGet("https://pastebin.com/raw/zXk4Rq2r"))()
end)

about:Button("iw指令", function()
  loadstring(game:HttpGet(('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'),true))()
end)

about:Button("情云同款自瞄可调", function()
局部fov = 100局部平滑度= 10局部十字线距离= 5局部run service = game:GetService(" run service ")局部UserInputService = game:GetService(" UserInputService ")局部玩家= game:GetService("Players ")局部Cam = game。workspace . current camera local fo vring = drawing . new(" Circle ")fo vring。Visible = true FOVring。厚度= 2 FOVring。Color = Color3.fromRGB(0，255，0)for vring。填充=假FOVring。半径= fov FOVring。位置=凸轮。ViewportSize / 2本地播放器=播放器。本地播放器本地Player GUI = Player:wait for child(" Player GUI ")local screen GUI = instance . new(" screen GUI ")screen GUI。Name = "FovAdjustGui" ScreenGui。parent = player GUI local Frame = instance . new(" Frame ")Frame。Name = "MainFrame "框架。background color 3 = color 3 . from RGB(30，30，30) Frame。border color 3 = color 3 . from RGB(128，0，128)帧。BorderSizePixel = 2帧。Position = UDim2.new(0.3，0，0.3，0)帧。Size = UDim2.new(0.4，0，0.4，0)帧。活动=真实帧。Draggable =真实框架。parent = screen GUI local minimize button = Iinstance . new(" text button ")minimize button。Name = "MinimizeButton "最小化按钮。Text = "-" MinimizeButton。TextColor3 = Color3.fromRGB(255，255，255) MinimizeButton。background color 3 = color 3 . from RGB(50，50，50) MinimizeButton。Position = UDim2.new(0.9，0，0，0) MinimizeButton。Size = UDim2.new(0.1，0，0.1，0) MinimizeButton。parent = Frame local is minimized = false minimize button。mouse button 1 click:Connect(function()is minimized = not is minimized if is minimized then Frame:TweenSize(udim 2 . new(0.1，0，0.1，0)，Enu米（meter的缩写））EasingDirection.Out，Enum。EasingStyle.Quad，0.3，true) MinimizeButton。text = "+" else Frame:TweenSize(udim 2 . new(0.4，0，0.4，0)，Enum。EasingDirection.Out，Enum。EasingStyle.Quad，0.3，true) MinimizeButton。text = "-" end end)local FOV label = instance . new(" text label ")FOV label。Name = "FovLabel" FovLabel。Text = "自瞄范围“FovLabel。TextColor3 = Color3.fromRGB(255，255，255) FovLabel。background transparency = 1 FOV label。Position = UDim2.new(0.1，0，0.1，0) FovLabel。Size = UDim2.new(0.8，0，0.2，0) FovLabel。父=框架局部FOV slider = instance . new(" TextBox ")FOV slider。Name = "FovSlider" FovSlider。Text = tostring(fov) FovSlider。TextColor3 = Color3.fromRGB(255，255，255) FovSlider。background color 3 = color 3 . from RGB(50，50，50) FovSlider。Position = UDim2.new(0.1，0，0.3，0) FovSlider。Size = UDim2.new(0.8，0，0.2，0) FovSlider。parent = Frame local smoothness label = instance . new(" text label ")smoothness label。name = " smooth ness label " smooth ness label。Text = "自瞄平滑度“SmoothnessLabel。TextColor3 = Color3.fromRGB(255，255，255)SmoothnessLabel。background transparency = 1 smoothness label。Position = UDim2.new(0.1，0，0.5，0) SmoothnessLabel。Size = UDim2.new(0.8，0，0.2，0) SmoothnessLabel。parent = Frame local smoothness slider = instance . new(" TextBox ")smoothness slider。name = " smoothnesslider " smoothnesslider。text = tostring(smooth)smooth ness slider。TextColor3 = Color3.fromRGB(255，255，255) SmoothnessSlider。background color 3 = color 3 . from RGB(50，50，50) SmoothnessSlider。Position = UDim2.new(0.1，0，0.7，0) SmoothnessSlider。磺胺异恶唑e = UDim2.new(0.8，0，0.2，0) SmoothnessSlider。parent = Frame local crosshirdistancelabel = instance . new(" text label ")crosshirdistancelabel。name = " crosshirdistancelabel " crosshirdistancelabel。Text = "自瞄预判距离" CrosshairDistanceLabel。TextColor3 = Color3.fromRGB(255，255，255)crosshirdistancelabel。background transparency = 1 crosshirdistancelabel。Position = UDim2.new(0.1，0，0.9，0)crosshirdistancelabel。Size = UDim2.new(0.8，0，0.2，0)crosshirdistancelabel。Parent =框架局部十字线距离侧边= instance . new(" TextBox ")crosshirdistanceslider。name = " crosshirdistanceslider " crosshirdistanceslider。text = tostring(crosshirdistance)crosshirdistanceslider。TextColor3 = Color3.fromRGB(255，255，255)crosshirdistanceslider。background color 3 = color 3 . from RGB(50，50，50)crosshirdistanceslider。Position = UDim2.new(0.1，0，1.1，0)crosshirdistanceslider。Size = UDim2.new(0.8，0，0.2，0)crosshirdistanceslider。parent = Frame local targetc Frame = Cam。CFrame本地函数updateDrawings() local camViewportSize = Cam。ViewportSize FOVring。position = camViewportSize/2 fo vring。Radius = fov end局部函数onKeyDown(input)如果输入。KeyCode == Enum。KeyCode.Delete然后run service:unbindfromdrenderstep(" FOV update ")FOV ring:Remove()end end UserInputService。InputBegan:Connect(onKeyDown)局部函数getClosestPlayerInFOV(trg _ part)local nearest = nil local last = math . huge local player mouse pos = Cam。ViewportSize / 2 for _，ipairs中的player(Players:get Players())do if player ~ = Players。LocalPlayer然后锁定al part =玩家。人物和玩家。character:findfirst child(trg _ part)如果part那么local ePos，is visible = Cam:WorldToViewportPoint(part。Position)本地距离= (Vector2.new(ePos.x，ePos.y) - playerMousePos)。如果距离< last且isVisible，且距离< fov，则last =距离最近=选手结束结束结束返回最近结束RunService。render stepped:Connect(function()update drawings()local closest = getClosestPlayerInFOV(" Head ")if closest and closest。人物:FindFirstChild(“头”)那么local targetCharacter =最近。字符局部targetHead = targetCharacter。head local target rootpart = target character:findfirst child(" HumanoidRootPart ")local is moving = target rootpart。速度。幅度> 0.1局部目标位置如果正在移动，则目标位置=目标方向。位置+ (targetHead。c frame . look vector * crosshirdistance)else target position = target head。position end targetc frame = c frame . new(Cam。CFrame.Position，target Position)else target CFrame = Cam。框架端凸轮。CFrame = Cam。CFrame:Lerp(targetCFrame，1/smooth)end)FOV slider。focus lost:Connect(function(enterPressed，inputThatCausedFocusLoss)如果enter pressed，则local newFov = tonumber(FovSlider。text)if new FOV then FOV = new FOV else FOV slider。text = tostring(FOV)end end end)smoothness slider。focus lost:Connect(function(enterPressed，inputThatCausedFocusLoss)如果enter pressed，则local newSmoothness = to number(smoothness slider。text)if newSmoothness then smoothness = newSmoothness else smoothness slider。Text = tostring(smoothness) end end end)十字线距离侧边。focus lost:Connect(function(enterPressed，inputThatCausedFocusLoss)如果enter pressed，则local new crosshirdistance = to number(crosshirdistanceslider。text)if new crosshirdistance then crosshirdistance = new crosshirdistance else crosshirdistance slider。Text = tostring(十字线距离)end end end)
结束)

about:Button("汉化阿尔宙斯自瞄",function()
loadstring(game:http get(" https://raw . githubusercontent . com/ding ding 123 hhh/SGB/main/% E4 % B8 % 81% E4 % B8 % 81% 20% E6 % B1 % 89% E5 % 8C % 96% E8 % 87% AA % E7 % 9E % 84 . txt "))()
结束)

关于:按钮("工具挂“，函数()
loadstring(game:http get(" https://raw . githubusercontent . com/Bebo-Mods/BeboScripts/main/standawekening . Lua "))()
结束)

关于:按钮("甩飞“，函数()
loadstring(game:http get(" https://raw . githubusercontent . com/ding ding 123 hhh/hknvh/main/% E7 % 94% A9 % E9 % A3 % 9e . txt "))()
end)

about:Button("铁拳",function()
loadstring(game:http get(' https://raw . githubusercontent . com/0 Ben 1/Fe/main/obf _ RF 6 iqurzu 1 fqrytcnlbav w34c 9n 55 S9 g9 g 3g ckz 086 RC 47m 6632 sed 4 zzyb 0 aygv . Lua . txt '))()
结束)

关于：切换(“ESP显示名字“AMG”，启用,功能（启用)
如果enabled then ENABLED = true for _，则ipairs(Players:GetPlayers())中的运动员会在PlayerAdded(播放器)终端播放器上运行添加的播放器:连接(onPlayerAdded)玩家player remove:Connect(onplayerrevering)local local player = Players。LocalPlayer if localPlayer和本地播放器。Character then for _，player in IPA IRS(Players:get Players())do if player。性格；角色；字母然后创建名称标签（球员)终点终点终点跑服务。heart beat:Connect(function()if ENABLED then for _，ipairs中的player(Players:get Players())do if player。字符然后创建名称标签(player)end end end)else ENABLED = false for _，player in IP airs(Players:get Players())do onplayerremoved(player)end run service:unbindromdrenderstep(" move ")end
结束)

关于:Toggle("圈ESP "，" ESP "，false，函数(状态)
对于_，玩家成对(游戏。Players:GetPlayers()) do
如果玩家~=游戏。玩家，那就本地玩家
如果陈述然后
local Highlight = instance . new(" Highlight ")
突出显示。家长=玩家。性格；角色；字母
突出显示。Adornee =玩家。性格；角色；字母

                    local billboard = Instance.new("BillboardGui")
                    billboard.Parent = player.Character
                    billboard.Adornee = player.Character
                    billboard.Size = UDim2.new(0, 100, 0, 100)
                    billboard.StudsOffset = Vector3.new(0, 3, 0)
                    billboard.AlwaysOnTop = true

                    local nameLabel = Instance.new("TextLabel")
                    nameLabel.Parent = billboard
                    nameLabel.Size = UDim2.new(1, 0, 1, 0)
                    nameLabel.BackgroundTransparency = 1
                    nameLabel.Text = player.Name
                    nameLabel.TextColor3 = Color3.new(1, 1, 1)
                    nameLabel.TextStrokeTransparency = 0.5
                    nameLabel.TextScaled = true

                    local circle = Instance.new("ImageLabel")
                    circle.Parent = billboard
                    circle.Size = UDim2.new(0, 50, 0, 50)
                    circle.Position = UDim2.new(0.5, 0, 0.5, 0) -- Center the circle
                    circle.AnchorPoint = Vector2.new(0.5, 0.5) -- Set the anchor point to the center
                    circle.BackgroundTransparency = 1
                    circle.Image = "rbxassetid://2200552246" -- Replace with your circle image asset ID
                else
                    if player.Character:FindFirstChildOfClass("Highlight") then
                        player.Character:FindFirstChildOfClass("Highlight"):Destroy()
                    end
                    if player.Character:FindFirstChildOfClass("BillboardGui") then
                        player.Character:FindFirstChildOfClass("BillboardGui"):Destroy()
                    end
                end
            end
        end
    end)

about:Button("透视1",function()
loadstring(game:HttpGet('https://pastebin.com/raw/MA8jhPWT'))()
end)

about:Button("透视2",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/Lucasfin000/SpaceHub/main/UESP'))()
end)

about:Button("无敌『不适用』",function()
loadstring(game:HttpGet('https://pastebin.com/raw/H3RLCWWZ'))()
end)

about:Button("隐身（E）",function()
loadstring(game:HttpGet('https://pastebin.com/raw/nwGEvkez'))()
end)

about:Button("电脑键盘",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt", true))()
end)

about:Button("飞车",function()
loadstring(game:HttpGet("https://pastebin.com/raw/G3GnBCyC", true))()
end)

about:Button("踏空行走",function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/Float'))()
end)

about:Button("飞车2",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/vb/main/%E9%A3%9E%E8%BD%A6.lua"))()
end)

about:Button("旋转",function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/dingding123hhh/tt/main/%E6%97%8B%E8%BD%AC.lua"))()
end)

about:Button("紫莎",function()
game.Players.LocalPlayer.Character.Humanoid.Health=0
end)

about:Button("飞檐走壁",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/zXk4Rq2r"))()
end)

about:Button("夜视仪",function()
    _G.OnShop = trueloadstring(game:HttpGet('https://raw.githubusercontent.com/DeividComSono/Scripts/main/Scanner.lua'))()
end)

about:Button("正常范围",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/jiNwDbCN"))()
end)

about:Button("中等范围",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/x13bwrFb"))()
end)

about:Button("高级范围",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/KKY9EpZU"))()
end)

about:Button("反挂机",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/9fFu43FF"))()
end)

about:Button("无限跳",function()
    loadstring(game:HttpGet("https://pastebin.com/raw/V5PQy3y0", true))()
end)

local UITab99 = win:Tab("『FE』",'7734068321')

local about = UITab99:section("『FE』",true)

about:Button("FE C00lgui", function()
loadstring(game:GetObjects("rbxassetid://8127297852")[1].Source)()
end)
about:Button("FE 1x1x1x1", function()
loadstring(game:HttpGet(('https://pastebin.com/raw/JipYNCht'),true))()
end)
about:Button("FE大长腿", function()
    loadstring(game:HttpGet('https://gist.githubusercontent.com/1BlueCat/7291747e9f093555573e027621f08d6e/raw/23b48f2463942befe19d81aa8a06e3222996242c/FE%2520Da%2520Feets'))()
end)
about:Button("FE用头", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/BK4Q0DfU"))()
end)
about:Button("复仇者", function()
    loadstring(game:HttpGet(('https://pastefy.ga/iGyVaTvs/raw'),true))()
end)
about:Button("鼠标", function()
    loadstring(game:HttpGet(('https://pastefy.ga/V75mqzaz/raw'),true))()
end)
about:Button("变怪物", function()
    loadstring(game:HttpGetAsync("https://pastebin.com/raw/jfryBKds"))()
end)
about:Button("香蕉枪", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/MrNeRD0/Doors-Hack/main/BananaGunByNerd.lua"))()
end)
about:Button("超长🐔巴", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/ESWSFND7", true))()
end)
about:Button("操人", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/XiaoYunCN/UWU/main/AHAJAJAKAK/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A/A.LUA", true))()
end)
about:Button("FE动画中心", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Animation-Hub/main/Animation%20Gui", true))()
end)
about:Button("FE变玩家", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/XR4sGcgJ"))()
end)
about:Button("FE猫娘R63", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Tescalus/Pendulum-Hubs-Source/main/Pendulum%20Hub%20V5.lua"))()
end)
about:Button("FE", function()
    loadstring(game:HttpGet('https://pastefy.ga/a7RTi4un/raw'))()
end)

local UITab4 = win:Tab("『力量传奇』",'7734068321')

local about = UITab4:section("『力量传奇』",true)

about:Toggle("自动比赛开关", "AR", false, function(AR)
  while AR do wait() wait(2) game:GetService("ReplicatedStorage").rEvents.brawlEvent:FireServer("joinBrawl") end
end)
about:Toggle("自动举哑铃", "ATYL", false, function(ATYL)
  local part = Instance.new('Part', workspace) part.Size = Vector3.new(500, 20, 530.1) part.Position = Vector3.new(0, 100000, 133.15) part.CanCollide = true part.Anchored = true local rs = game:GetService("RunService").RenderStepped while ATYL do wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0) for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do if v.ClassName == "Tool" and v.Name == "Weight" then v.Parent = game.Players.LocalPlayer.Character end end game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep") end
end)
about:Toggle("自动俯卧撑", "ATFWC", false, function(ATFWC)
  local part = Instance.new('Part', workspace) part.Size = Vector3.new(500, 20, 530.1) part.Position = Vector3.new(0, 100000, 133.15) part.CanCollide = true part.Anchored = true local rs = game:GetService("RunService").RenderStepped while ATFWC do wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0) for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do if v.ClassName == "Tool" and v.Name == "Pushups" then v.Parent = game.Players.LocalPlayer.Character end end game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep") end
end)
about:Toggle("自动仰卧起坐", "ATYWQZ", false, function(ATYWQZ)
  local part = Instance.new('Part', workspace) part.Size = Vector3.new(500, 20, 530.1) part.Position = Vector3.new(0, 100000, 133.15) part.CanCollide = true part.Anchored = true local rs = game:GetService("RunService").RenderStepped while ATYWQZ do wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0) for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do if v.ClassName == "Tool" and v.Name == "Situps" then v.Parent = game.Players.LocalPlayer.Character end end end game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
end)
about:Toggle("自动倒立身体", "ATDL", false, function(ATDL)
  local part = Instance.new('Part', workspace) part.Size = Vector3.new(500, 20, 530.1) part.Position = Vector3.new(0, 100000, 133.15) part.CanCollide = true part.Anchored = true local rs = game:GetService("RunService").RenderStepped while ATDL do wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0) for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do if v.ClassName == "Tool" and v.Name == "Handstands" then v.Parent = game.Players.LocalPlayer.Character end end end game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
end)
about:Toggle("自动锻炼", "ATAAA", false, function(ATAAA)
local part = Instance.new('Part '，workspace)部件。Size = Vector3.new(500，20，530.1)零件。Position = Vector3.new(0，100000，133.15)零件。CanCollide =真实部分。在ATAAA做wait()游戏时Anchored = true。players . local player . character . humanoidrootpart . c frame = part。CFrame + Vector3.new(0，50，0)用于I，v成对(游戏。players . local player . backpack:get children())do if v . class Name = = "工具"和v.Name == "倒立"或v.Name == "仰卧起坐"或v.Name == "俯卧撑"或v.Name == "重量"然后v:findfirtschildofclass("数字值")。Value = 0重复wait()直到游戏开始。players . local player . backpack:FindFirstChildOfClass(“工具”)游戏。Players . local player . character:WaitForChild("人形"):equip tool(v)game:get service(" Players "). local player . muscleevent:FireServer(" rep ")end end
结束)

关于:切换("自动重生"，" ATRE "，false，函数(ATRE)
而ATRE do wait()game:get service(" replicated storage ")revents . rebirthremote:InvokeServer(" rebirthRequest ")end
结束)
关于:按钮("收集宝石“，函数()
jk = {} for _，v成对(游戏:GetService("ReplicatedStorage ")。Chest rewards:get descendants())do if v.Name ~= "光明因缘宝箱"或v . Name ~ = "邪恶因缘宝箱"则table.insert(jk，v.Name) end end for i = 1，# JK do wait(2)game:get service(" replicated storage ")revents . checkchest remote:InvokeServer(JK[我])结束
结束)

关于:切换("沙滩跑步机10”，“PPJ10”，假，功能(PPJ10)
getgenv()ppj 10 = ppj 10而getgenv()ppj 10做wait()游戏。players . local player . character:WaitForChild(“人形”)。WalkSpeed = 10游戏。players . local player . character:WaitForChild(" HumanoidRootPart ")。CFrame = CFrame.new(238.671112，5.40315914，387.713165，-0.0160072874，-2.90710176e-08，-0.99987185，-3.3434191e-09，1，-2.90212157e-08，0.99987185，2.877players . local player . character:WaitForChild(" HumanoidRootPart ")。CFrame local Run service = game:get service(" RunService”)本地玩家=游戏:GetService(“玩家”)本地本地玩家=玩家。local player run service:BindToRenderStep(" move "，Enum。render priority . character . value+1，function() if localPlayer。角色然后本地人形=本地玩家。character:WaitForChild(" Humanoid ")if Humanoid then Humanoid:Move(vector 3 . new(10000，0，-1)，true)end end end)end if not getgenv()(ppj 10 then local run service = game:get service(" run service ")local player = game:get service(" Players ")local local player = Players。LocalPlayer run service:unbindfromdrenderstep(" move "，Enum。render priority . character . value+1，function() if localPlayer。角色然后本地人形=本地玩家。character:findfirst child(" Humanoid ")如果是Humanoid，那么Humanoid:Move(vector 3 . new(10000，0，-1)，true) end end end) end
结束)
关于:切换("健身房跑步机2000 "，" PPJ2000 "，假，函数(PPJ2000)
    if game.Players.LocalPlayer.Agility.Value >= 2000 then getgenv().PPJ2000 = PPJ2000 while getgenv().PPJ2000 do wait() game.Players.LocalPlayer.Character:WaitForChild("Humanoid").WalkSpeed = 10 game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").CFrame = CFrame.new(-3005.37866, 14.3221855, -464.697876, -0.015773816, -1.38508964e-08, 0.999875605, -5.13225586e-08, 1, 1.30429667e-08, -0.999875605, -5.11104332e-08, -0.015773816) local oldpos = game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").CFrame local RunService = game:GetService("RunService") local Players = game:GetService("Players") local localPlayer = Players.LocalPlayer RunService:BindToRenderStep("move", Enum.RenderPriority.Character.Value + 1, function() if localPlayer.Character then local humanoid = localPlayer.Character:WaitForChild("Humanoid") if humanoid then humanoid:Move(Vector3.new(10000, 0, -1), true) end end end) end end if not getgenv().PPJ2000 then local RunService = game:GetService("RunService") local Players = game:GetService("Players") local localPlayer = Players.LocalPlayer RunService:UnbindFromRenderStep("move", Enum.RenderPriority.Character.Value + 1, function() if localPlayer.Character then local humanoid = localPlayer.Character:FindFirstChild("Humanoid") if humanoid then humanoid:Move(Vector3.new(10000, 0, -1), true) end end end) end
结束)
关于:切换("神话健身房跑步机2000 "，" SHPPJ2000 "，假，函数(SHPPJ2000)
    if game.Players.LocalPlayer.Agility.Value >= 2000 then getgenv().SHPPJ2000 = SHPPJ2000 while getgenv().SHPPJ2000 do wait() game.Players.LocalPlayer.Character:WaitForChild("Humanoid").WalkSpeed = 10 game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").CFrame = CFrame.new(2571.23706, 15.6896839, 898.650391, 0.999968
