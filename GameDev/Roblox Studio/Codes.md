#### Print
creating a print statement that prints out in the terminal:
```
print("my balls")
```

#### Functions
creating a basic function:
```
local function functionName(parameter1, parameter2, ...)
	codeLine1
	codeLine2
	return someOutput1, someOutput2
end

functionName(parameter1, parameter2, ...)
```

##### Wait For Child
- used mainly to *get* objects | models | folders | etc.

```
local someVariable = someFolder.someObject:WaitForChild("somePart|someModel")
```

##### Get Children
- used to get all of the instance's children
```
local someVariable = someFolder.someObject:GetChildren("somePart|someModel")
```

#### Tween
- used to move parts, models, and such

```
local tweenService = game:GetService("TweenService")
local part = script.Parent

local tweenInfo = TweenInfo.new(
	0.5,
	Enum.EasingStyle.Quad,
	Enum.EasingDirection.InOut,
	-1,
	true
)

local properties = {
	["CFrame"] = base.CFrame + Vector3.new(50, 0, 0)
}

local tween = tweenService:Create(base, tweenInfo, properties)

tween:Play()
```

###### When Tweening a Model
1. Click Model
2. Add a Script file under the chosen Model
3. Select a part and rename as *base*
4. Un-anchor all parts except the *base*
5. Weld all the parts

Replace the *part* with *base* in the given tween example above:
```
local base = script.Parent.PrimaryPart
```

###### When Colliding with Players
Trigger Warning, Physics is INVOLVED
1. Calculate velocity

```
local runService = game:GetService("RunService")

local lastPosition = base.Position

runService.Stepped:Connect(function (_, deltaTime)
	local currentPosition = base.Position
	local deltaPosition = currentPosition - lastPosition
	
	local velocity = deltaPosition / deltaTime
	
	part.AssemblyLinearVelocity = velocity
	
	lastPosition = currentPosition
end)
```

