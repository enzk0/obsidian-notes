#### Print
```
print("my balls")
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