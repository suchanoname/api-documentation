# C_BasePlayer

## Functions

## GetProp

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| table | string | Netvar table |
| name | string | Netvar name |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | Netvar dependant | Netvar value |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local player = localplayer:GetPlayer()
local health = player:GetProp("DT_BasePlayer", "m_iHealth")
print(health)
```

## SetProp

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| table | string | Netvar table |
| name | string | Netvar name |
| value | Netvar dependant | Netvar value |

```lua
cheat.RegisterCallback("draw", function() 
    local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
    local getplayer = localplayer:GetPlayer()
    getplayer:SetProp("DT_BasePlayer", "m_iHealth", 1) 
end)
```

## GetClassId

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| id | int | Class id |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local GetClassId = getplayer:GetClassId()
print(GetClassId)
```

## EntIndex

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | int | Entity index |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local ent_index = getplayer:EntIndex()
print(ent_index)
```

## SetModelIndex

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| index | int | Model index |

```lua
--soonTM
```

## IsVisible

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| from | Vector | - |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player visible |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local visible = getplayer:IsVisible(Vector.new(0, 0, 0))
print(visible)
```

## GetEyePosition

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Eye position in 3D space |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local eye_pos = getplayer:GetEyePosition()
print(eye_pos.x, eye_pos.y, eye_pos.z)
```

## GetActiveWeapon

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| weapon | C_BaseCombatWeapon* | Pointer to active weapon |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local active_weapon = getplayer:GetActiveWeapon()
print(active_weapon)
```

## GetHitboxCenter

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| vec | Vector | Hitbox center |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local hitbox_center = getplayer:GetHitboxCenter(0)
print(hitbox_center.x, hitbox_center.y, hitbox_center.z)
```

## GetName

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| name | string | Name |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local pl_name = getplayer:GetName()
print(pl_name)
```

## IsDormant

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player dormant |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local dormant = getplayer:IsDormant()
print(dormant)
```

## IsTeamMate

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| value | bool | Is player teammate |

```lua
local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
local getplayer = localplayer:GetPlayer()
local is_teammate = getplayer:IsTeamMate()
print(is_teammate)
```

## GetSequenceActivity

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| sec | int | Sequence |

### Return value:

| Name | Type | Description |
| :--- | :--- | :--- |
| act | int | Sequence activity |

```lua
--soonTM
```

## DrawHitbox

### Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| index | int | Hitbox index |
| clr | Color | Color |
| tick_n | int | Tick |

```lua
cheat.RegisterCallback("draw", function()
    local localplayer = g_EntityList:GetClientEntity(g_EngineClient:GetLocalPlayer())
    local getplayer = localplayer:GetPlayer()
    getplayer:DrawHitbox(3, Color.new(1, 1, 1, 1), g_GlobalVars.tickcount-1)
end)
```
