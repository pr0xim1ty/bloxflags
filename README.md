> [!WARNING]
> **This repository is under maintenance. Information may be incorrect or out of date. Please check back at a later date.**

# <img src="https://github.com/theletron/bloxflags/raw/main/Bloxflags.png" width="48"/> Bloxflags

![Currently listed presets](https://img.shields.io/badge/currently_listed_presets-50-yellow)
![Version](https://img.shields.io/badge/version-2.0.0-7238e6)

Collection of [FastFlags](https://github.com/pizzaboxer/bloxstrap/wiki/A-guide-to-FastFlags) in the Roblox engine.
Most of the FastFlags come from the [Bloxstrap discord server](https://discord.gg/nKjV3mGq6R). <br>

## Requirements
* <img src="https://github.com/bloxstraplabs/bloxstrap/blob/main/Images/Bloxstrap.png" width="20"/> **[Bloxstrap (for Windows)](https://bloxstraplabs.com/)**
* <img src="https://github.com/AppleBlox/appleblox/blob/main/.github/assets/logo.png" width="24"/> **[AppleBlox (for Mac)](https://appleblox.com/)**

## Preset Type Navigation
* **[Rendering](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#rendering)**
* **[Lighting](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file##lighting)**
* **[Graphical](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#graphical)**
* **[QoL](https://github.com/theletron/bloxflagst/tree/main?tab=readme-ov-file#qol)**
* **[UI](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#user-interface)**
* **[Audio](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#audio)**
* **[Debugging](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#debugging)**
* **[Experimental](https://github.com/theletron/bloxflags/tree/main?tab=readme-ov-file#experimental)**

<h1 align="center">Rendering</h1>

### OpenGL
```json
{
    "FFlagDebugGraphicsDisableDirect3D11": true,
    "FFlagDebugGraphicsPreferOpenGL": true
}
```

### Vulkan
> [!WARNING]
> May cause bugs, issues and instability.
```json
{
    "FFlagDebugGraphicsDisableDirect3D11": true,
    "FFlagDebugGraphicsPreferVulkan": true
}
```

<h1 align="center">Lighting</h1>

### Enable GPU Light Culling
> [!NOTE]
> Light culling is a technique in computer graphics used to optimize rendering by determining which lights affect which objects in a scene, reducing unnecessary lighting calculations and improving performance.
```json
{
    "FFlagFastGPULightCulling3": true
}
```

### Enable CPU Light Culling
```json
{
    "FFlagDebugForceFSMCPULightCulling": true
}
```

<h1 align="center">Graphical</h1>

### Occlusion Culling
> [!TIP]
> Only renders instances that is visible to the player. Improves FPS significantly on lower-end devices.
###### [@Maximum_ADHD](https://x.com/MaximumADHD/status/1832254232243617871)
```json
{
    "DFFlagUseVisBugChecks": true,
    "FFlagEnableVisBugChecks27": true,
    "FIntEnableVisBugChecksHundredthPercent27": 100
}
```

### Terrain Quality Manager
> [!TIP]
> The higher the number, the better the quality. 8, 16, 32 and 64 can be used
###### [@spectroscopic](https://discord.com/channels/1099468797410283540/1194889014981967932)
```json
{
    "FIntTerrainArraySliceSize": 8
}
```

### No Textures
###### [@.s_y_](https://discord.com/channels/1099468797410283540/1247944649822441634)
###### Updated from [@skylan031](https://discord.com/channels/1099468797410283540/1247944649822441634/1280952560596811796)
```json
{
    "FIntDebugTextureManagerSkipMips": 8
}
```

### Low Render Distance
> [!IMPORTANT]
> Only works with games that have StreamingEnabled enabled.
###### [@cam1494](https://discord.com/channels/1099468797410283540/1189687881170690128)
```json
{
    "DFIntDebugRestrictGCDistance": 1
}
```

### Disable LOD based on distance
###### [@beanacceleration](https://discord.com/channels/1099468797410283540/1146963091775553536/1146963091775553536)
```json
{
    "DFIntCSGLevelOfDetailSwitchingDistance": 0,
    "DFIntCSGLevelOfDetailSwitchingDistanceL12": 0,
    "DFIntCSGLevelOfDetailSwitchingDistanceL23": 0,
    "DFIntCSGLevelOfDetailSwitchingDistanceL34": 0
}
```

### Remove Grass
###### [Origin](https://discord.com/channels/1099468797410283540/1160254260915744809/1160257120395071579)
```json
{
    "FIntFRMMinGrassDistance": 0,
    "FIntFRMMaxGrassDistance": 0,
    "FIntRenderGrassDetailStrands": 0,
    "FIntRenderGrassHeightScaler": 0
}
```

### Grass Motion Speed
> [!TIP]
> The speed of the grass increases with the number.
###### [@spectroscopic](https://discord.com/channels/1099468797410283540/1292228979008339999)
```json
{
    "FIntGrassMovementReducedMotionFactor": 0
}
```

### Disable Dynamic Head Animations
###### [@atweak](https://discord.com/channels/1099468797410283540/1211694825628241980)
```json
{
    "DFIntAnimationLodFacsDistanceMin": 0,
    "DFIntAnimationLodFacsDistanceMax": 0,
    "DFIntAnimationLodFacsVisibilityDenominator": 0
}
```

<h1 align="center">QoL</h1>

### Disable 240 FPS cap
```json
{
    "FFlagTaskSchedulerLimitTargetFpsTo2402": false,
}
```

### Enable Captures Toggle for V4 + New UI
> [!IMPORTANT]
> This will **not** remove Captures and return the Record tab.
> It will add a toggle to turn on and off the Capture button.
> Only V4 + New UI doesn't have this toggle (V2 doesn't have the Captures tab)
###### @theletron
```json
{
    "FFlagEnableCapturesInChrome": false
}
```

### Text Size Options in Settings
###### [@0100152000022000 (Sky)](https://discord.com/channels/1099468797410283540/1278473853319774228)
```json
{
    "FFlagEnablePreferredTextSizeScale": true,
    "FFlagEnablePreferredTextSizeSettingInMenus2": true
}
```

### GUI Hiding Options in Settings
###### [@atweak](https://discord.com/channels/1099468797410283540/1219706245858984026)
```json
{
    "FFlagUserShowGuiHideToggles": true,
    "FFlagUserShowGuiHideToggles2": true,
    "FFlagGuiHidingApiSupport2": true
}
```

### Increased Camera Sensitivity Decimal Limit
> [!NOTE]
> Roblox changed the limit to 3, it used to be 5.
###### [@.s_y_](https://discord.com/channels/1099468797410283540/1278533638702628995)
```json
{
    "FFlagFixSensitivityTextPrecision": false,
}
```

### Smooth Trackpad Scrolling in Client Home
> [!NOTE]
> Instead of scrolling in large and equal chunks every time you scroll with a trackpad, it scrolls smoothly without skipping the small parts it would normally skip.
> Doesn't work as well with normal external mice.
###### [@satlybpro](https://discord.com/channels/1099468797410283540/1278525530559352914https://discord.com/channels/1099468797410283540/1300384121637441536)
```json
{
  "FFlagBetterTrackpadScrolling": true
}
```

### Blue Theme
###### [@.s_y_](https://discord.com/channels/1099468797410283540/1278525530559352914)
```json
{
    "FFlagLuaAppEnableFoundationColors5": true
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
    "DFIntTimestepArbiterThresholdCFLThou": 300
}
```

### Disable Ad Portals
> [!NOTE]
> If you accidentally touch ad portals, this is for you.
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
    "DFIntDefaultTimeoutTimeMs": 10000
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

### Old Marketplace Search Bar
###### [@thefrenchguy4](https://discord.com/channels/1099468797410283540/1281731256178180118)
```json
{
    "FFlagAXSearchLandingPageIXPEnabled4": false
}
```

### Old Chat Tab
###### [@thefrenchguy4](https://discord.com/channels/1099468797410283540/1280936777946890274)
```json
{
    "FStringNewChatTabExperimentLayerValue": "",
    "FFlagEnableNewChatTabExperiment5": false
}
```

### Remove Parental Controls Tab in Client Settings
###### [@thefrenchguy4](https://discord.com/channels/1099468797410283540/1280626112740982876)
```json
{
    "FFlagLuaAppsEnableParentalControlsTab": false
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
> Replace "userId" with your user id.
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
    "FIntV1MenuLanguageSelectionFeaturePerMillageRollout": 0
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
###### Default: Min 7, Max 80
> [!TIP]
> These are flags have default values.
```json
{
    "DFIntVoiceChatRollOffMinDistance": 7,
    "DFIntVoiceChatRollOffMaxDistance": 80
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
> [!TIP]
> Default: 1000
###### [@0100152000022000 (Sky)](https://discord.com/channels/1099468797410283540/1208100665138745424)
```json
{
    "DFIntVoiceChatVolumeThousandths": 100000
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
> [!TIP]
> Shift + F5 displays FPS too, with more information.
```json
{
    "FFlagDebugDisplayFPS": true
}
```

### Don't Render ScreenGuis
> [!IMPORTANT]
> Causes Client Home not to be displayed.
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
> These presets are for fun and testing. They may not work, may cause instability and unexpected results, or simply **not useful at all**.

### Disable Purchases
###### [@hazey_hazel](https://discord.com/channels/1099468797410283540/1153898300714532994)
```json
{
    "DFFlagOrder66": true
}
```

### Verified Badge on Everyone
> [!IMPORTANT]
> Clientsided.
###### [@bloodrvn](https://discord.com/channels/1099468797410283540/1167534034591694849)
```json
{
    "FFlagOverridePlayerVerifiedBadge": true
}
```
