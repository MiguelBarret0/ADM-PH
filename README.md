-- Coloque este LocalScript em StarterGui
-- Nome do painel: PH PAINEL

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "PHPainel"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(0, 300, 0, 400)
Frame.Position = UDim2.new(0.1, 0, 0.1, 0)
Frame.BackgroundColor3 = Color3.fromRGB(30,30,30)
Frame.Parent = ScreenGui

local Title = Instance.new("TextLabel")
Title.Size = UDim2.new(1, 0, 0, 50)
Title.BackgroundColor3 = Color3.fromRGB(50,50,50)
Title.Text = "PH PAINEL"
Title.TextColor3 = Color3.new(1,1,1)
Title.Font = Enum.Font.SourceSansBold
Title.TextSize = 24
Title.Parent = Frame

-- Função auxiliar para criar botões
local function criarBotao(nome, ordem, func)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(1, -20, 0, 40)
    btn.Position = UDim2.new(0, 10, 0, 60 + (ordem * 50))
    btn.BackgroundColor3 = Color3.fromRGB(70,70,70)
    btn.TextColor3 = Color3.new(1,1,1)
    btn.Text = nome
    btn.Font = Enum.Font.SourceSansBold
    btn.TextSize = 20
    btn.Parent = Frame
    btn.MouseButton1Click:Connect(func)
end

-- Botões simulados (não fazem cheat, apenas mostram mensagem)
criarBotao("Jump Boost", 0, function()
    game.StarterGui:SetCore("SendNotification", {
        Title = "PH Painel";
        Text = "Você ativou Jump Boost (simulação)";
        Duration = 2;
    })
end)

criarBotao("Speed Boost", 1, function()
    game.StarterGui:SetCore("SendNotification", {
        Title = "PH Painel";
        Text = "Você ativou Speed Boost (simulação)";
        Duration = 2;
    })
end)

criarBotao("Fly Mode", 2, function()
    game.StarterGui:SetCore("SendNotification", {
        Title = "PH Painel";
        Text = "Você ativou Fly Mode (simulação)";
        Duration = 2;
    })
end)

criarBotao("Car Fly", 3, function()
    game.StarterGui:SetCore("SendNotification", {
        Title = "PH Painel";
        Text = "Você ativou Car Fly (simulação)";
        Duration = 2;
    })
end)

criarBotao("Jail", 4, function()
    game.StarterGui:SetCore("SendNotification", {
        Title = "PH Painel";
        Text = "Você prendeu um jogador (simulação)";
        Duration = 2;
    })
end)

criarBotao("Unjail", 5, function()
    game.StarterGui:SetCore("SendNotification", {
        Title = "PH Painel";
        Text = "Você soltou o jogador (simulação)";
        Duration = 2;
    })
end)# ADM-PH
