-- Script de Auto Farm para Dragon Ball Rage

-- Função para aumentar o Ki
local function autoKi(player)
    while true do
        wait(1)
        player.Ki.Value = player.Ki.Value + 10
    end
end

-- Função para aumentar a Defesa
local function autoDefense(player)
    while true do
        wait(1)
        player.Defense.Value = player.Defense.Value + 5
    end
end

-- Função para aumentar o Ataque
local function autoAttack(player)
    while true do
        wait(1)
        player.Attack.Value = player.Attack.Value + 7
    end
end

-- Função para auto Zenkai
local function autoZenkai(player)
    while true do
        wait(1)
        player.Zenkai.Value = player.Zenkai.Value + 1
    end
end

-- Inicializa as funções para o jogador
local player = game.Players.LocalPlayer

-- Função para iniciar os scripts
local function startScripts()
    spawn(function() autoKi(player) end)
    spawn(function() autoDefense(player) end)
    spawn(function() autoAttack(player) end)
    spawn(function() autoZenkai(player) end)
end

-- Conecta o botão à função de início
script.Parent.MouseButton1Click:Connect(startScripts)
