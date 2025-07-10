-- Load OrionLib
local OrionLib = loadstring(game:HttpGet('https://raw.githubusercontent.com/Snxdfer/back-ups-for-libs/main/Orion.lua'))()

-- Create main window
local Window = OrionLib:MakeWindow({
    Name = "Mr_V4L3TiNO1109 HUB",
    HidePremium = false,
    SaveConfig = true,
    ConfigFolder = "Config"
})

-- Brookhaven Tab
local BrookhavenTab = Window:MakeTab({
    Name = "Brookhaven",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

-- Lista de scripts Brookhaven (com Fê Emotes adicionado e Coquette Hub removido)
local Scripts = {
    {"Gumball Hub", "https://raw.githubusercontent.com/JaozinScripts/Gumball-Hub/refs/heads/main/GumballHubRetorn2.1.1.1.lua"},
    {"Sander X", "https://rawscripts.net/raw/Brookhaven-RP-Sander-XY-35845"},
    {"Chaos Hub", "https://raw.githubusercontent.com/Venom-devX/ChaosHub/main/loader.lua"},
    {"Rael Hub", "https://raw.githubusercontent.com/Laelmano24/Rael-Hub/main/main.txt"},
    {"Shadow Hub", "https://raw.githubusercontent.com/realgengar/scripts/refs/heads/main/Gui%20Version.Lua"},
    {"Speed Wave", "https://raw.githubusercontent.com/Shadow6698/vheiclespeed/main/Main.txt"},
    {"Duplicator Carros", "https://raw.githubusercontent.com/kigredns/Flame-Object/refs/heads/main/script.lua"},
    {"Yin Hub (executa Ayla Hub)", "https://rawscripts.net/raw/Brookhaven-RP-Yin-Hub-21835"},
    {"SP Hub", "https://rawscripts.net/raw/Brookhaven-RP-SP-Hub-New-Uptade-1o3v-33364"},
    {"Brutus Hub", "https://rawscripts.net/raw/Brookhaven-RP-BRUTUS-HUB-REUPLOUD-44098"},
    {"Nytherune Hub", "https://raw.githubusercontent.com/wx-sources/spacecomm/refs/heads/main/nytheruneplus"},
    {"Farm Ballon", "https://raw.githubusercontent.com/Shadow6698/ballonfarm/main/Main.txt"},
    {"AutoTickets", "https://raw.githubusercontent.com/Shadow6698/farmbrookhaven/main/Main.txt"},
    {"RealzX Hub (HubFarms)", "https://rawscripts.net/raw/Brookhaven-RP-RealzXHub-New-Event-44226"},
    {"Fê Emotes", "https://scriptblox.com/raw/Brookhaven-RP-all-emotes-6849"},
}

-- Criar os botões na aba
for _, script in pairs(Scripts) do
    BrookhavenTab:AddButton({
        Name = script[1],
        Callback = function()
            loadstring(game:HttpGet(script[2]))()
        end
    })
end

-- Iniciar UI
OrionLib:Init()
