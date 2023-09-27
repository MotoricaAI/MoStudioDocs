# Retargeting
Motorica Studio ships with assets that you can use for retargeting. While an explanation of these assets is provided [below](./#assets), a tutorial on how to use them is currently missing. Please have a look at these YouTube tutorials instead:

- [Motorica - Generative AI for animation - Unreal](https://www.youtube.com/watch?v=-UY5rom6LGE)
- [Motorica - Generative AI for animation - Plugin Unreal](https://www.youtube.com/watch?v=3qmHzPH06O4)
- [Motorica a Metahuman con Mixamo Animation Retargeting 2](https://www.youtube.com/watch?v=R5euNHUcUec&t)

## Assets
The plugin includes assets that you can use to retarget Motorica animations onto other characters. **These assets are intended for use in UE 5.1 and above** as we experienced issues with retargeting in UE 5.0 (partially discussed [here](https://forums.unrealengine.com/t/retargeting-root-bone-ue5/506512) and [here](https://forums.unrealengine.com/t/ue5-retargeted-root-motion-animations-have-innacurate-pelvis-hip-placement/514656)).

To view these assets, enable "Show Plugin Content" in the Content Browser settings.

![](../images/content-browser-settings-show-plugin-content.png)

And navigate to `Plugins > Motorica Studio > Content`.

![](../images/content-browser-folder-plugin.png)

Note: The folder names may be different depending on the plugin version you are using.

### Retargeting folder

![](../images/content-browser-folder-plugin-retargeting.png)

- **BP_RuntimeRTG_Base** - A spawnable `Actor Blueprint` that sets up runtime retargeting between the Motorica skeleton and other skeletons. This blueprint serves as a base which other blueprints extend.
- **LS_RuntimeRTG** - A `Level Sequence` asset demonstrating runtime retargeting from the Motorica skeleton to a set of Mixamo skeletons and MetaHuman skeletons.

#### MetaHuman
![](../images/content-browser-folder-plugin-retargeting-metahuman.png)

- **ABP_MetaHuman_extended** - `Animation Blueprint` used for runtime retargeting from the Motorica skeleton to the MetaHuman skeleton. It uses the `RTG_MetaHuman_extended_MoStudio_minimal` IK Retargeter asset.
- **ABP_MetaHuman_minimal** - `Animation Blueprint` used for runtime retargeting from the Motorica skeleton to the MetaHuman skeleton. It uses the `RTG_MetaHuman_minimal_MoStudio_minimal` IK Retargeter asset.
- **BP_RuntimeRTG_MetaHuman_extended** - A spawnable `Actor Blueprint` that extends from `BP_RuntimeRTG_Base`. It sets up runtime retargeting from the Motorica skeleton to the MetaHuman skeleton using `ABP_MetaHuman_extended`.
- **BP_RuntimeRTG_MetaHuman_minimal** - A spawnable `Actor Blueprint` that extends from `BP_RuntimeRTG_Base`. It sets up runtime retargeting from the Motorica skeleton to the MetaHuman skeleton using `ABP_MetaHuman_minimal`.
- **IK_MetaHuman_extended** - `IK Rig` asset that configures the default MetaHuman skeleton for retargeting. It contains bone chains for the spine, legs, arms, head, root, and fingers. This is a slightly modified copy of the original MetaHuman IK Rig.
- **IK_MetaHuman_minimal** - `IK Rig` asset that configures the default MetaHuman skeleton for retargeting. It contains bone chains for the spine, legs, arms, head and root, excluding fingers.
- **RTG_MetaHuman_extended_MoStudio_minimal** - `IK Retargeter` asset that retargets from the `IK_MoStudio_minimal` IK Rig to the `IK_MetaHuman_extended` IK Rig. The source skeleton was adjusted to match the A-pose of the target skeleton. IK goals are disabled.
- **RTG_MetaHuman_minimal_MoStudio_minimal** - `IK Retargeter` asset that retargets from the `IK_MoStudio_minimal` IK Rig to the `IK_MetaHuman_minimal` IK Rig. The source skeleton was adjusted to match the A-pose of the target skeleton.

#### Mixamo
![](../images/content-browser-folder-plugin-retargeting-mixamo-mutant.png)

All Mixamo characters share similar assets. The following assets are for the *Mixamo Mutant* character:

- **ABP_Mixamo_Mutant** - `Animation Blueprint` used for runtime retargeting from the Motorica skeleton to the Mixamo Mutant skeleton. It uses the `RTG_Mixamo_Mutant` IK Retargeter asset.
- **BP_RuntimeRTG_Mixamo_Mutant** - A spawnable `Actor Blueprint` that extends from `BP_RuntimeRTG_Base`. It sets up runtime retargeting from the Motorica skeleton to the Mixamo Mutant skeleton using `ABP_Mixamo_Mutant`.
- **IK_Mixamo_Mutant** - `IK Rig` asset that configures the Mixamo Mutant skeleton for retargeting. It contains bone chains for the spine, legs, arms, head and root, excluding fingers.
- **RTG_Mixamo_Mutant** - `IK Retargeter` asset that retargets from the `IK_MoStudio_minimal` IK Rig to the `IK_Mixamo_Mutant` IK Rig.

#### MotoricaStudio
![](../images/content-browser-folder-plugin-retargeting-motoricastudio.png)

- **ABP_MoStudio_minimal** - `Animation Blueprint` used for runtime retargeting from the Motorica skeleton to itself. It uses the `RTG_MoStudio_minimal` IK Retargeter asset.
- **BP_RuntimeRTG_MoStudio_minimal** - A spawnable `Actor Blueprint` that extends from `BP_RuntimeRTG_Base`. It sets up runtime retargeting from the Motorica skeleton to itself using `ABP_MoStudio_minimal`.
- **IK_MoStudio_legacy** - This is the legacy `IK Rig` asset that was provided in *Motorica Studio v0.1.0*. It is included for compatibility purposes. The recommendation is to use `IK_MoStudio_minimal` instead. If you are using the old `IK_Motorica` IK Rig, you should update the references to this asset.
- **IK_MoStudio_minimal** - `IK Rig` asset that configures the Motorica skeleton for retargeting. It contains bone chains for the spine, legs, arms, head and root, excluding fingers. This asset is commonly used in `IK Retargeter` assets as the retargeting *source*.
- **RTG_MoStudio_minimal** - `IK Retargeter` asset that retargets from the `IK_MoStudio_minimal` IK Rig to itself. This is mainly used for debugging purposes.
