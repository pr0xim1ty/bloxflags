[shield-repository-license]:      https://img.shields.io/github/license/theletron/bloxflags
[shield-repository-latest]:       https://img.shields.io/github/v/release/theletron/bloxflags?color=7439DB
[shield-preset-count]:            https://img.shields.io/badge/currently_listed_presets-51-yellow

[repository-license]:             https://github.com/theletron/bloxflags/blob/main/LICENSE
[repository-latest]:              https://github.com/theletron/bloxflags/releases/latest

> [!WARNING]
> **This repository is under maintenance. Information may be incorrect or out of date. Please check back at a later date.**

> [!CAUTION]
> Fast flags are extremely powerful, being that they are intended to only be used by Roblox engineers. While they can be very useful, they can cause issues with stability and functionality if you don't know what you're doing.
>
> You should only use the flag list editor if you know what you're doing. You should only configure flags that you know exactly what they do.
>
> We especially do not recommend using any flags that claim to "optimise ping", "+250 fps boost" and more. These are clickbait and don't work.

<!--
> [!IMPORTANT]
> In the near future, Roblox plans to restrict local flag configurations. This was supposed to have [already been implemented](https://i.redd.it/4c5u68gczbkc1.jpeg), **but it hasn't been.**
>
> **This doesn't mean you shouldn't use this list at this time.**
!-->

<div align=center>
    <img alt="Bloxflags logo" src="Images/Branding/Bloxflags-full-dark.png#gh-dark-mode-only" width="420">
    <img alt="Bloxflags logo" src="Images/Branding/Bloxflags-full-light.png#gh-light-mode-only" width="420">
</div>

<div align=center>

[![License][shield-repository-license]][repository-license]
![Currently Listed Presets][shield-preset-count]
[![Version][shield-repository-latest]][repository-latest]

</div>

---

Bloxflags is a collection of [fast flags](https://github.com/theletron/bloxflags/wiki/What-are-fast-flags%3F) grouped as presets for use with the Roblox engine.

Preset doesn't work? Feature suggestion? Question? [Check out existing issues.](https://github.com/theletron/bloxflags/issues) If you can't find an issue relevant to your context, [submit an issue here!](https://github.com/theletron/bloxflags/issues/new/choose)

## Requirements

* <img alt="Bloxstrap" src="https://raw.githubusercontent.com/bloxstraplabs/bloxstrap/main/Images/Bloxstrap.png" width="24" style="vertical-align:middle"> **[Bloxstrap (for Windows)](https://bloxstraplabs.com/)**
* <img alt="AppleBlox" src="https://raw.githubusercontent.com/AppleBlox/appleblox/main/.github/assets/logo.png" width="24" style="vertical-align:middle"> **[AppleBlox (for Mac)](https://appleblox.com/)**

## Preset Type Navigation

* **[Graphical](https://github.com/theletron/bloxflags/tree/main#graphical)**
* **[Improvements](https://github.com/theletron/bloxflags/tree/main#improvements)**
* **[UI](https://github.com/theletron/bloxflags/tree/main#user-interface-ui)**
* **[UX](https://github.com/theletron/bloxflags/tree/main#user-experience-ux)**
* **[Roblox UI Version](https://github.com/theletron/bloxflags/tree/main#roblox-ui-version)**
* **[Audio](https://github.com/theletron/bloxflags/tree/main#audio)**
* **[Debugging](https://github.com/theletron/bloxflags/tree/main#debugging)**
* **[Experimental](https://github.com/theletron/bloxflags/tree/main#experimental)**

<h1 align=center>Graphical</h1>

### Disable 240 FPS Limit
> [!WARNING]
> Increasing your FPS limit beyond 240 FPS **actually does more than you expect**. So there's a very small chance that increasing it beyond this limit could have unintended side effects, including but not limited to:
> * increased ping
> * crashes when teleporting/joining games
>
> It doesn't happen for everyone, but at least check if it happens for you.
>
> **For more information, see [this](https://github.com/bloxstraplabs/bloxstrap/wiki/A-guide-to-FastFlags/#framerate-limit).**
```json
{
    "FFlagTaskSchedulerLimitTargetFpsTo2402": false,
}
```

### Override Graphics Quality Level + Max Render Distance
> [!WARNING]
> This preset won't work on games with custom render distance systems.

> [!TIP]
> You can increase the graphics quality with the value, just like the graphics slider.
>
> **Minimum: 1 (lowest quality)** <br>
> **Recommended: 6 (sweet spot for low-end users)** <br>
> **Maximum: 21 (highest quality)**
```json
{
    "DFIntDebugFRMQualityLevelOverride": 1
}
```

### Override Graphics Quality Level on Startup
```json
{
    "FIntRomarkStartWithGraphicQualityLevel": 1
}
```

### No Textures
```json
{
    "FIntDebugTextureManagerSkipMips": 8
}
```

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

### Low Render Distance
> [!IMPORTANT]
> Only works with experiences that have [streaming](https://create.roblox.com/docs/workspace/streaming) enabled.
```json
{
    "DFIntDebugRestrictGCDistance": 1
}
```

### Disable LOD Based on Distance
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

<h1 align=center>Improvements</h1>

### Remove VC Beta Badge
```json
{
    "FFlagControlBetaBadgeWithGuac": false
}
```

### GUI Hiding Options in Settings
> [!IMPORTANT]
> Only appears if you have [gui hiding options](https://github.com/bloxstraplabs/bloxstrap/wiki/A-guide-to-FastFlags#gui-hiding) enabled.
```json
{
    "FFlagUserShowGuiHideToggles": true,
    "FFlagUserShowGuiHideToggles2": true,
    "FFlagGuiHidingApiSupport2": true
}
```

### Increased Camera Sensitivity Decimal Limit
> [!NOTE]
> Roblox changed the limit for the camera sensitivity to 3. Before, it used to be 5. **This preset reverts this change.**
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
> Increasing this value will give you more time to reconnect in case of network loss. <br>
> **This value is in miliseconds.**
>
> **Default: 10000** <br>
> **Recommended: 60000**
```json
{
    "DFIntDefaultTimeoutTimeMs": 10000
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

### Dev Console Log Limit
> [!TIP]
> Increasing this option will make your life easier if you are a developer.
>
> **Default: 500** <br>
> **Recommended: 5000**
```json
{
    "FIntNewDevConsoleMaxLogCount": 500
}
```

<h1 align=center>User Interface (UI)</h1>

### Rename 'Charts' tab back to 'Discovery'
```json
{
    "FFlagLuaAppChartsPageRenameIXP": false
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

### Remove Language Feedback Button
```json
{
    "FFlagDisableFeedbackSoothsayerCheck": false
}
```

### Remove Player List Close Button
```json
{
    "FFlagDisablePlayerListDisplayCloseBtn": true
}
```

### Rename "Reset Character" to "Respawn" in Escape Menu
###### [@theletron](https://github.com/theletron)
```json
{
    "FFlagInExperienceMenuResetButtonTextToRespawn": true
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

### Old Invite Menu
```json
{
    "FFlagEnableNewInviteMenuIXP2": false
}
```

### Remove Parental Controls Tab in Client Settings
```json
{
    "FFlagLuaAppsEnableParentalControlsTab": false
}
```

### Verified Badge
> [!IMPORTANT]
> Clientsided.
>
> **Replace "userId" with your user id.**
```json
{
    "FStringWhitelistVerifiedUserId": "userId"
}
```

### Verified Badge on Everyone
> [!IMPORTANT]
> Clientsided.
```json
{
    "FFlagOverridePlayerVerifiedBadge": true
}
```

<h1 align=center>User Experience (UX)</h2>

### Disable Purchases
```json
{
    "DFFlagOrder66": true
}
```

<h1 align=center>Roblox UI Version</h2>

> [!IMPORTANT]
> V1 Menu and V3 Menu has been completely removed from Roblox. It is not possible to use it.

> [!WARNING]
> Currently, only Chrome Menu and Chrome UI is supported. V2 Menu and V2 UI does not have the latest updates and may cause instability issues.

> [!TIP]
> V1 Menu:
> <img alt="V1 Menu" src="https://raw.githubusercontent.com/theletron/bloxflags/Images/Screenshots/v1-menu.png" width="24" style="vertical-align:middle">
>
> V2 Menu:
> <img alt="V2 Menu" src="https://raw.githubusercontent.com/theletron/bloxflags/Images/Screenshots/v2-menu.png" width="24" style="vertical-align:middle">
>
> V3 Menu:
> <img alt="V3 Menu" src="https://raw.githubusercontent.com/theletron/bloxflags/Images/Screenshots/v3-menu.png" width="24" style="vertical-align:middle">
>
> Chrome Menu:
> <img alt="Chrome Menu" src="https://raw.githubusercontent.com/theletron/bloxflags/Images/Screenshots/chrome-menu.png" width="24" style="vertical-align:middle">
>
> V2 UI:
> <img alt="V2 UI" src="https://raw.githubusercontent.com/theletron/bloxflags/Images/Screenshots/v2-ui.png" width="24" style="vertical-align:middle">
>
> Chrome UI:
> <img alt="V1 Menu" src="https://raw.githubusercontent.com/theletron/bloxflags/Images/Screenshots/chrome-ui.png" width="24" style="vertical-align:middle">

### V2 Menu + V2 UI
```json
{
    "FIntNewInGameMenuPercentRollout3": 0,
    "FFlagEnableInGameMenuChromeABTest4": false
}
```

### V4 Menu + V2 UI
```json
{
    "FIntNewInGameMenuPercentRollout3": 0,
    "FFlagEnableInGameMenuChromeABTest4": false
}
```

### V4 Menu + V4 UI
```json
{
    "FIntNewInGameMenuPercentRollout3": 0,
    "FFlagEnableInGameMenuChromeABTest4": true
}
```

<h1 align=center>Audio</h1>

### Voice Chat Hear Distance
> [!TIP]
> **Default:**
>
> **Minimum Distance: 7** <br>
> **Maximum Distance: 80**
>
> **Recommended:**
>
> **Maximum Distance: 120**
```json
{
    "DFIntVoiceChatRollOffMinDistance": 7,
    "DFIntVoiceChatRollOffMaxDistance": 80
}
```

### Voice Chat Volume
```json
{
    "DFIntVoiceChatVolumeThousandths": 1000
}
```

### No Sounds
```json
{
    "FFlagDebugRomarkMockingAudioDevices": true
}
```

<h1 align=center>Debugging</h1>

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
```json
{
    "FFlagUserClickToMoveSupportAgentCanClimb2": false
}
```

<h1 align=center>Experimental</h1>

> [!CAUTION]
> It is not recommended to use these presets.

### Text Size Options in Settings
> [!CAUTION]
> Alpha feature. You may experience unexpected behaviour.
```json
{
    "FFlagEnablePreferredTextSizeScale": true,
    "FFlagEnablePreferredTextSizeSettingInMenus2": true
}
```

<h2 align=center>Rendering</h1>

> [!CAUTION]
> You can change your renderer to DirectX 11 or DirectX 10 on Bloxstrap.
>
> These renderers are not supported. Here are the side effects:
> * OpenGL: low performance
> * Vulkan: crashes frequently
>
> **Only change your renderer if you know what you are doing.**

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
