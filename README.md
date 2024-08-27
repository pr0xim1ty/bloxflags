# <img src="https://github.com/theletron/bloxflags/raw/main/Bloxflags.png" width="48"/> Bloxflags

![Currently listed](https://img.shields.io/badge/currently_listed-44-yellow)
![Version](https://img.shields.io/badge/version-1.0.0-7238e6)

Collection of [Fast Flags](https://github.com/pizzaboxer/bloxstrap/wiki/A-guide-to-FastFlags) in the Roblox engine.
Most of the fast flags are gotten from the [Bloxstrap discord server](https://discord.gg/nKjV3mGq6R). <br>
You can change many other options in the Bloxstrap Fast Flags menu.

## Requirements
* <img src="https://github.com/theletron/bloxflags/raw/main/Bloxstrap.png" width="20"/> **[Bloxstrap (Windows)](https://bloxstrap.pizzaboxer.xyz/)**
* <img src="https://github.com/theletron/bloxflags/raw/main/AppleBlox.png" width="24"/> **[AppleBlox (Mac)](https://appleblox.com/)**

## Configuration Type Navigation
* **[Rendering](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#rendering)**
* **[Lighting](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file##lighting)**
* **[Graphical](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#graphical)**
* **[QoL](https://github.com/theletron/bloxflagst/tree/main?tab=readme-ov-file#qol)**
* **[UI](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#user-interface)**
* **[Audio](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#audio)**
* **[Debugging](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#debugging)**
* **[Experimental](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#experimental)**

<h1 align="center">Rendering</h1>

### DirectX 11
```json
{
    "FFlagDebugGraphicsPreferD3D11": true
}
```

### DirectX 10
```json
{
    "FFlagDebugGraphicsPreferD3D11FL10": true
}
```

### Vulkan
```json
{
    "FFlagDebugGraphicsDisableDirect3D11": true,
    "FFlagDebugGraphicsPreferVulkan": true
}
```

### OpenGL
```json
{
    "FFlagDebugGraphicsDisableDirect3D11": true,
    "FFlagDebugGraphicsPreferOpenGL": true
}
```

<h1 align="center">Lighting</h1>

### Enable GPULightCulling
##### Light culling is an optimization technique used in computer graphics to reduce the number of lights considered when rendering a scene. It involves determining which lights are affecting specific areas of the scene and only calculating the lighting for those lights, thus improving performance.
```json
{
    "FFlagFastGPULightCulling3": true
}
```

### Enable CPULightCulling
```json
{
    "FFlagDebugForceFSMCPULightCulling": true
}
```

<h1 align="center">Graphical</h1>

### Terrain Quality Manager
##### 8, 16, 32 and 64 can be used
##### Higher the number, better the quality.
###### [@spectroscopic](https://discord.com/channels/1099468797410283540/1194889014981967932)
```json
{
    "FIntTerrainArraySliceSize": "8"
}
```

### Low Render Distance
> [!IMPORTANT]
> Only works on games which turned StreamingEnabled on.
###### [@cam1494](https://discord.com/channels/1099468797410283540/1189687881170690128)
```json
{
    "DFIntDebugRestrictGCDistance": "1"
}
```

### Disable LOD based on distance
###### @theletron
```json
{
    "DFIntCSGLevelOfDetailSwitchingDistance": "0",
    "DFIntCSGLevelOfDetailSwitchingDistanceL12": "0",
    "DFIntCSGLevelOfDetailSwitchingDistanceL23": "0",
    "DFIntCSGLevelOfDetailSwitchingDistanceL43": "0"
}
```

### Remove Grass
##### This configuration makes it have no size, thus removing it.
###### [Origin](https://discord.com/channels/1099468797410283540/1160254260915744809/1160257120395071579)
```json
{
    "FIntFRMMinGrassDistance": "0",
    "FIntFRMMaxGrassDistance": "0",
    "FIntRenderGrassDetailStrands": "0"
}
```

<h1 align="center">QoL</h1>

### Custom Accessory Positions
###### [@HealthyKarl](https://devforum.link/3089928/3)
```json
{
    "FFlagAXAccessoryAdjustment4": true,
    "FFlagAXAccessoryAdjustmentIXPEnabled": true,
    "FFlagAXAccessoryAdjustmentIXPEnabledForAll": true,
    "FFlagAXAvatarFetchResultCamelCase": true
}
```

### Disable 240 FPS cap
```json
{
    "FFlagTaskSchedulerLimitTargetFpsTo2402": false,
}
```

### GUI Hiding Options in Settings
###### [@atweak](https://discord.com/channels/1099468797410283540/1219706245858984026)
```json
{
    "FFlagUserShowGuiHideToggles": true,
    "GuiHidingApiSupport2": true
}
```

### Darker Theme
###### [@cam1419](https://discord.com/channels/1099468797410283540/1211370693514625067)
```json
{
    "FFlagLuaAppUseUIBloxColorPalettes1": true,
    "FFlagUIBloxUseNewThemeColorPalettes": true
}
```

### Stuttery Animation Fix
###### [@0100152000022000 (Sky)](https://discord.com/channels/1099468797410283540/1228713913235935242)
```json
{
    "DFIntTimestepArbiterThresholdCFLThou": "300"
}
```

### Disable Ads
###### [@atweak](https://discord.com/channels/1099468797410283540/1179502701118230529)
```json
{
    "FFlagAdServiceEnabled": false
}
```

### Disable Telemetry 
###### [@bluepilledgreat](https://gist.github.com/bluepilledgreat/c4307f927fef66628c423b9e208fa9cd)
```json
{
    "FFlagDebugDisableTelemetryEphemeralCounter": true,
    "FFlagDebugDisableTelemetryEphemeralStat": true,
    "FFlagDebugDisableTelemetryEventIngest": true,
    "FFlagDebugDisableTelemetryPoint": true,
    "FFlagDebugDisableTelemetryV2Counter": true,
    "FFlagDebugDisableTelemetryV2Event": true,
    "FFlagDebugDisableTelemetryV2Stat": true
}
```

### Timeout Time
##### Default: 10000
```json
{
    "DFIntDefaultTimeoutTimeMs": "10000"
}
```

### Subscriptions Page
###### [@cam1494](https://discord.com/channels/1099468797410283540/1211415227644645527)
```json
{
    "FFlagLuaAppDevSubsEnabled": true
}
```

### Remove VC Beta Badge
```json
{
    "FFlagControlBetaBadgeWithGuac": false
}
```

<h1 align="center">User Interface</h1>

### Rename "Charts" back to "Discovery"
###### [@cam1494](https://discord.com/channels/1099468797410283540/1254997424116863048)
```json
{
    "FFlagLuaAppChartsPageRenameIXP": false
}
```

### Revert Unibar Icon Change
###### @theletron
```json
{
    "FFlagUseNewUnibarIcon": false
}
```

### Remove Unibar Respawn Button
###### @theletron
```json
{
    "FFlagUnibarRespawn": false
}
```

### Verified Badge
> [!IMPORTANT]
> Clientsided.
###### [@atweak](https://discord.com/channels/1099468797410283540/1160200870517030963)
```json
{
    "FStringWhitelistVerifiedUserId": "userId"
}
```

### Return New Invite Menu
###### [@spectroscopic](https://discord.com/channels/1099468797410283540/1191455320275431444)
```json
{
    "FFlagEnableNewInviteMenuIXP2": false
}
```

### Remove Haptics Option
###### [@thefrenchguy4](https://discord.com/channels/1099468797410283540/1268891182302494772)
```json
{
    "FFlagAddHapticsToggle": false
}
```

### Remove VR Option
###### [@spectroscopic](https://discord.com/channels/1099468797410283540/1238434506818588682)
```json
{
    "FFlagAlwaysShowVRToggleV3": false
}
```

### Remove Chat Translation Message
###### [@toofastforboo](https://discord.com/channels/1099468797410283540/1277315962269339698)
```json
{
    "FFlagChatTranslationEnableSystemMessage": false
}
```

### Remove Chat Translation Options
###### [@spectroscopic](https://discord.com/channels/1099468797410283540/1204335548160938025)
```json
{
    "FFlagChatTranslationSettingEnabled3": false
}
```

### Remove Experience Language Option
###### @theletron
```json
{
    "FIntV1MenuLanguageSelectionFeaturePerMillageRollout": "0",
    "FIntV3MenuLanguageSelectionFeaturePerMillageRollout": "0"
}
```

### Remove Language Feedback Button in Settings
###### [@atweak](https://discord.com/channels/1099468797410283540/1231746431539351612)
```json
{
    "FFlagDisableFeedbackSoothsayerCheck": false
}
```

### Remove Player List Close Button
###### [@easternbloxxer](https://discord.com/channels/1099468797410283540/1211306325334822982)
```json
{
    "FFlagDisablePlayerListDisplayCloseBtn": true
}
```

<h1 align="center">Audio</h1>

### Voice Chat Hear Distance
###### Default: [Min 7 Max 80]
```json
{
    "DFIntVoiceChatRollOffMinDistance": "7",
    "DFIntVoiceChatRollOffMaxDistance": "80"
}
```

### Audio Physical Velocity
###### [@0100152000022000 (Sky)](https://discord.com/channels/1099468797410283540/1211417705572466698)
```json
{
    "FFlagSoundsUsePhysicalVelocity": true
}
```

### Voice Chat Volume
##### Default: 1000
###### [@0100152000022000 (Sky)](https://discord.com/channels/1099468797410283540/1208100665138745424)
```json
{
    "DFIntVoiceChatVolumeThousandths": "100000"
}
```

### No Sounds
###### [@cam1494](https://discord.com/channels/1099468797410283540/1211420049101815818)
```json
{
    "FFlagDebugRomarkMockingAudioDevices": true
}
```

<h1 align="center">Debugging</h1>

### Display FPS
##### Shift + F5 displays FPS too, with more information.
```json
{
    "FFlagDebugDisplayFPS": true
}
```

### Don't Render UI
##### Does not result in a black screen in games. However this flag causes the client menu to not load, causing a white screen instead.
###### [@tezos.](https://discord.com/channels/1099468797410283540/1232247819352674304)
```json
{
    "FFlagDebugDontRenderUI": true
}
```

### Don't Render ScreenGui's
##### ScreenGui is the instance that displays UI instances in Roblox. This means that nothing will load, resulting in a black screen in games.
###### [@atweak](https://discord.com/channels/1099468797410283540/1231750903078322256)
```json
{
    "FFlagDebugDontRenderScreenGui": true
}
```

### Disabe Click to Move Climbing
###### [@atweak](https://discord.com/channels/1099468797410283540/1231749733941510195)
```json
{
    "FFlagUserClickToMoveSupportAgentCanClimb2": false
}
```

<h1 align="center">Experimental</h1>

> [!CAUTION]
> These configuration are solely for fun. Might cause instability, unexpected results or **just not useful at all**.

### Convert R6 Animations to R15
> [!CAUTION]
> Buggy, only works for R15 and doesn't work on custom animations.
###### [@droidhmp1](https://discord.com/channels/998572881892094012/1201618145203458200/1201623210630856704)
```json
{
    "FFlagRemapAnimationR6ToR15Rig": true
}
```

### Disable Purchases
###### [@hazey_hazel](https://discord.com/channels/1099468797410283540/1153898300714532994)
```json
{
    "DFFlagOrder66": true
}
```

### Disable Dynamic Head Animations
###### [@atweak](https://discord.com/channels/1099468797410283540/1211694825628241980)
```json
{
    "DFIntAnimationLodFacsDistanceMin": "0",
    "DFIntAnimationLodFacsDistanceMax": "0",
    "DFIntAnimationLodFacsVisibilityDenominator": "0"
}
```

### Verified Badge on Everyone
> [!IMPORTANT]
> Clientsided.
###### [@atweak](https://discord.com/channels/1099468797410283540/1167534034591694849)
```json
{
    "FFlagOverridePlayerVerifiedBadge": true
}
```
