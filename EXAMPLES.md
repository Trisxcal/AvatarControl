## Musician Example

### Adds musician and plays the animation after a time period:
```lua
local Musicians = game.Workspace.Musicians

ACS:AddAvatar(Musicians.Cello, "Front")
wait(4)
ACS:PlayAvatarAnimation("Cello")
```

### Loops the playing and idle animation:
```lua
local Musicians = game.Workspace.Musicians

AvatarControl:AddAvatar(Musicians.Cello, "Left")

while wait(4) do
	AvatarControl:PlayAvatarAnimation(Musicians.Cello, 6, 3, true)
	wait(4)
	AvatarControl:PlayAvatarAnimation(Musicians.Cello, 0.4, 3, false)
	wait(4)
	AvatarControl:PlayAvatarAnimation(Musicians.Cello, 0.4, 3, true)
	wait(4)
	AvatarControl:PlayAvatarAnimation(Musicians.Cello, 0.4, 3, false)
end
```
