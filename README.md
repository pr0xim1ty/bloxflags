[shield-repository-license]:  https://img.shields.io/github/license/theletron/bloxflags
[shield-repository-latest]:   https://img.shields.io/github/v/release/theletron/bloxflags?color=7439DB
[shield-preset-count]:        https://img.shields.io/badge/currently_listed_presets-51-yellow

[repository-license]:         https://github.com/theletron/bloxflags/blob/main/LICENSE
[repository-latest]:          https://github.com/theletron/bloxflags/releases/latest

> [!CAUTION]
> FastFlags are extremely powerful, being that they are intended to only be used by Roblox engineers. While they can be very useful, they can cause issues with stability and functionality if you don't know what you're doing. <br> <br> You should only use the flag list editor if you know what you're doing. You should only configure flags that you know exactly what they do. <br> <br> We especially do not recommend importing any flags that claim to "optimise ping", "+250 fps boost" and more. These are clickbait and don't work.

> [!IMPORTANT]
> In the near future, Roblox plans to restrict local flag configurations. This was supposed to have already been implemented, but it hasn't been.
> **This doesn't mean you shouldn't use this flag list at this time.**

<div style="text-align: center;">
    <img alt="Bloxflags logo" src="Images/Branding/Bloxflags-full-dark.png#gh-dark-mode-only" width="420">
    <img alt="Bloxflags logo" src="Images/Branding/Bloxflags-full-light.png#gh-light-mode-only" width="420">
</div>

<div style="text-align: center;">

[![License][shield-repository-license]][repository-license]
![Currently Listed Presets][shield-preset-count]
[![Version][shield-repository-latest]][repository-latest]

</div>

----

This is a collection of [fast flags](https://github.com/theletron/bloxflags/wiki/What-are-fast-flags%3F) grouped as presets for use with the Roblox engine.

## Requirements

* <img alt="Bloxstrap" src="https://raw.githubusercontent.com/bloxstraplabs/bloxstrap/main/Images/Bloxstrap.png" width="24" style="vertical-align: middle;"/> **[Bloxstrap (for Windows)](https://bloxstraplabs.com/)**
* <img alt="AppleBlox" src="https://raw.githubusercontent.com/AppleBlox/appleblox/main/.github/assets/logo.png" width="24" style="vertical-align: middle;"/> **[AppleBlox (for Mac)](https://appleblox.com/)**

## Preset Type Navigation

* **[Lighting](https://github.com/theletron/bloxflags/tree/main#lighting)**
* **[Graphical](https://github.com/theletron/bloxflags/tree/main#graphical)**
* **[Improvements](https://github.com/theletron/bloxflags/tree/main#improvements)**
* **[Roblox UI Version](https://github.com/theletron/bloxflags/tree/main#roblox-ui-version)***
* **[UI](https://github.com/theletron/bloxflags/tree/main#user-interface)**
* **[Audio](https://github.com/theletron/bloxflags/tree/main#audio)**
* **[Debugging](https://github.com/theletron/bloxflags/tree/main#debugging)**
* **[Experimental](https://github.com/theletron/bloxflags/tree/main#experimental)**

<h1 style="text-align: center;">Lighting</h1>

### Enable GPU Light Culling
> [!NOTE]
> Light culling is a technique used in computer graphics to improve rendering by determining which lights affect which objects in a scene.
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

<h1 style="text-align: center;">Graphical</h1>

### No Textures
```json
{
    "FIntDebugTextureManagerSkipMips": 8
}
```

### Low Render Distance
> [!IMPORTANT]
> Only works with experiences that have [streaming](https://create.roblox.com/docs/workspace/streaming) enabled.
```json
{
    "DFIntDebugRestrictGCDistance": 1
}
```

### Override Graphics Quality Level on Startup
```json
{
    "FIntRomarkStartWithGraphicQualityLevel": 1
}
```

### Override Render Distance
> [!WARNING]
> This doesn't work on all experiences. If you set it to 1 and it doesn't change when you increase it, it's probably capped by the game. Remove the flag or increase the value to 6 or above. This probably won't affect you. It only applies to games with a custom render distance engine.
> [!TIP]
> The render distance increases with the value. Here are the values you can use: **<br> 1 = 1 bar of graphics quality (Recommended) <br> 6 = 3 bars of graphics quality  <br> 21 = 10 bars of graphics quality**
```json
{
    "DFIntDebugFRMQualityLevelOverride": 1
}
```

### Disable LOD based on distance
```json
{
    "DFIntCSGLevelOfDetailSwitchingDistance": 0,
    "DFIntCSGLevelOfDetailSwitchingDistanceL12": 0,
    "DFIntCSGLevelOfDetailSwitchingDistanceL23": 0,
    "DFIntCSGLevelOfDetailSwitchingDistanceL34": 0
}
```

### Remove Grass
```json
{
    "FIntFRMMinGrassDistance": 0,
    "FIntFRMMaxGrassDistance": 0,
    "FIntRenderGrassDetailStrands": 0
}
```

### Grass Motion Speed
> [!TIP]
> The speed of the grass increases with the value.
```json
{
    "FIntGrassMovementReducedMotionFactor": 0
}
```

### Disable Dynamic Head Animations
```json
{
    "DFIntAnimationLodFacsDistanceMin": 0,
    "DFIntAnimationLodFacsDistanceMax": 0,
    "DFIntAnimationLodFacsVisibilityDenominator": 0
}
```

<h1 style="text-align: center;">Improvements</h1>

### Disable 240 FPS cap
```json
{
    "FFlagTaskSchedulerLimitTargetFpsTo2402": false,
}
```

### Text Size Options in Settings
```json
{
    "FFlagEnablePreferredTextSizeScale": true,
    "FFlagEnablePreferredTextSizeSettingInMenus2": true
}
```

### GUI Hiding Options in Settings
> [!IMPORTANT]
> Only works if you have [gui hiding options](https://github.com/bloxstraplabs/bloxstrap/wiki/A-guide-to-FastFlags#gui-hiding) enabled.
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
```json
{
    "FFlagFixSensitivityTextPrecision": false,
}
```

### Smooth Trackpad Scrolling in Client Home
> [!IMPORTANT]
> Doesn't work as well with normal external mice.
> [!NOTE]
> Instead of scrolling in large and equal chunks every time you scroll with a trackpad, it scrolls smoothly without skipping the small parts it would normally skip.
```json
{
    "FFlagBetterTrackpadScrolling": true
}
```

### Blue Theme
```json
{
    "FFlagLuaAppEnableFoundationColors7": true,
    "FFlagLuaAppFoundationColorsABTest7": true,
    "FFlagLuaAppUseUIBloxColorPalettes1": false,
    "FFlagUIBloxUseNewThemeColorPalettes": false
}
```

### Original Theme
> [!NOTE]
> Roblox is now slowly rolling out the new blue theme with AB tests. The ability to turn off the blue theme is not certain in the future.
```json
{
    "FFlagLuaAppEnableFoundationColors7": false,
    "FFlagLuaAppFoundationColorsABTest7": false,
    "FFlagLuaAppUseUIBloxColorPalettes1": true,
    "FFlagUIBloxUseNewThemeColorPalettes": true
}
```

### Disable Ad Portals
> [!NOTE]
> If you don't want to accidentally touch ad portals, this is for you.
```json
{
    "FFlagAdServiceEnabled": false
}
```

### Disable Telemetry
> [!NOTE]
> Does not completely disable all telemetry, but it does disable a lot of it.
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

### Time until Timeout
> [!TIP]
> Increasing this value will give you more time to reconnect in case of network loss. **This value is in miliseconds.** <br> **Default: 10000**
```json
{
    "DFIntDefaultTimeoutTimeMs": 60000
}
```

### Subscriptions Page
> [!NOTE]
> Located in client settings.
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

### Dev Console Log Limit
> [!TIP]
> Increasing this option will make your life easier if you are a developer. <br> **This flag has the default value.**
```json
{
    "FIntNewDevConsoleMaxLogCount": 500
}
```

<h1 style="text-align: center;">User Interface</h1>

### Rename Charts back to Discovery
```json
{
    "FFlagLuaAppChartsPageRenameIXP": false
}
```

### Old Marketplace Search Bar
```json
{
    "FFlagAXSearchLandingPageIXPEnabled4": false
}
```

### Old Chat Tab
```json
{
    "FStringNewChatTabExperimentLayerValue": "",
    "FFlagEnableNewChatTabExperiment5": false
}
```

### Remove Parental Controls Tab in Client Settings
```json
{
    "FFlagLuaAppsEnableParentalControlsTab": false
}
```

### Rename "Reset Character" to "Respawn" in Escape Menu
###### [@theletron](https://github.com/theletron)
```json
{
    "FFlagInExperienceMenuResetButtonTextToRespawn": true
}
```

### Verified Badge
> [!IMPORTANT]
> Clientsided. <br> Replace "userId" with your user id.
```json
{
    "FStringWhitelistVerifiedUserId": "userId"
}
```

### Return New Invite Menu
```json
{
    "FFlagEnableNewInviteMenuIXP2": false
}
```

### Remove Haptics Option
```json
{
    "FFlagAddHapticsToggle": false
}
```

### Remove VR Option
```json
{
    "FFlagAlwaysShowVRToggleV3": false
}
```

### Remove Chat Translation Message
```json
{
    "FFlagChatTranslationEnableSystemMessage": false
}
```

### Remove Chat Translation Options
```json
{
    "FFlagChatTranslationSettingEnabled3": false
}
```

### Remove Experience Language Option
###### [@theletron](https://github.com/theletron)
```json
{
    "FIntV1MenuLanguageSelectionFeaturePerMillageRollout": 0
}
```

### Remove Language Feedback Button in Settings
###### @atweak
```json
{
    "FFlagDisableFeedbackSoothsayerCheck": false
}
```

### Remove Player List Close Button
###### @easternbloxxer
```json
{
    "FFlagDisablePlayerListDisplayCloseBtn": true
}
```

<h2 style="text-align: center;">UI Versions</h2>

> [!IMPORTANT]
> V1 and V3 Menu has been completely removed from Roblox. It is not possible to use it.

> [!CAUTION]
> Currently, only V4 is supported. V2 Menu and V2 UI does not have the latest and may cause instability issues.

### V2 Menu + UI
```json
{
    "FIntNewInGameMenuPercentRollout3": 100,
    "FFlagEnableInGameMenuChromeABTest4": false
}
```

### V3 Menu + UI
```json
{
    "FIntNewInGameMenuPercentRollout3": 0,
    "FFlagEnableInGameMenuChromeABTest4": true
}
```

### V2 UI
```json
{
    "FIntNewInGameMenuPercentRollout3": 0,
    "FFlagEnableInGameMenuChromeABTest4": false
}
```

<h1 style="text-align: center;">Audio</h1>

### Voice Chat Hear Distance
> [!TIP]
> **Default: <br> Minimum Distance: 7 <br> Maximum Distance: 80**
```json
{
    "DFIntVoiceChatRollOffMinDistance": 7,
    "DFIntVoiceChatRollOffMaxDistance": 80
}
```

### Audio Physical Velocity
###### @0100152000022000 (Sky)
```json
{
    "FFlagSoundsUsePhysicalVelocity": true
}
```

### Voice Chat Volume
> [!TIP]
> Default: 1000
###### @0100152000022000 (Sky)
```json
{
    "DFIntVoiceChatVolumeThousandths": 100000
}
```

### No Sounds
###### @cam1494
```json
{
    "FFlagDebugRomarkMockingAudioDevices": true
}
```

<h1 style="text-align: center;">Debugging</h1>

### Display FPS
> [!TIP]
> Shift + F5 displays FPS too, with more information.
```json
{
    "FFlagDebugDisplayFPS": true
}
```

### Always Display Stats
```json
{
    "FFlagDebugAlwaysDisplayRenderStats": true
}
```

### Disabe Click to Move Climbing
###### @atweak
```json
{
    "FFlagUserClickToMoveSupportAgentCanClimb2": false
}
```

<h1 style="text-align: center;">Experimental</h1>

> [!CAUTION]
> These presets are for fun and testing. They may **not work**, may cause **instability** and **unexpected results**, or simply **not useful at all**.

### Disable Purchases
###### @hazey_hazel
```json
{
    "DFFlagOrder66": true
}
```

### Verified Badge on Everyone
> [!IMPORTANT]
> Clientsided.
###### @bloodrvn
```json
{
    "FFlagOverridePlayerVerifiedBadge": true
}
```

<h2 style="text-align: center;">Rendering</h1>

> [!WARNING]
> You can change your renderer to DirectX 11 or DirectX 10 on Bloxstrap. <br> These renderers are unstable and can cause bugs, crashes and instability. <br> **Only change your renderer if you know what you are doing.**

### OpenGL
```json
{
    "FFlagDebugGraphicsDisableDirect3D11": true,
    "FFlagDebugGraphicsPreferOpenGL": true
}
```

### Vulkan
```json
{
    "FFlagDebugGraphicsDisableDirect3D11": true,
    "FFlagDebugGraphicsPreferVulkan": true
}
```
