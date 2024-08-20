# Changelog (Motorica Studio)
## Motorica Studio v0.3.1
`Released on 2024-Aug-20`

#### New
- Added "Loop Animation" checkbox.

    !!! tip
        This works best with Motorica presets where the speed is constant and there is no acceleration.

- Added cloud login and registration support that uses an embedded browser.

#### Improvement
- Login errors are now displayed under the `Login` button.
- User credentials are no longer stored locally.

#### Removed
- Removed support for legacy servers
- Removed the following properties: APILocation, Email, Password

## Motorica Studio v0.3.0
`Released on 2024-Jun-13`

#### New
- Added button in the Motorica Studio Editor toolbar that opens the Motorica Studio plugin settings.
- Added a toolbar in the Motorica Studio Editor viewport that exposes snap settings for translation and rotation, perspective and orthographic modes, and lighting configuration.
- Added plugin support for Unreal Engine 5.4.
- Added skeleton asset `SK_Motorica_Char_UE_v1` that replaces the old `MoStudio_Character_Skeleton` asset. *([more info](get-started/included-assets.md#characters))*

    !!! warning
        `MoStudio_Character_Skeleton` is now *deprecated*. Read [this guide](how-to-guides/migrate-to-030.md) to retarget existing animations to the new skeleton.

#### Improvement
- Added default layout to the Motorica Studio editor UI. (No more floating tabs when the UI layout is reset.)
- Updated various UI icons.

#### Bug & Crash Fix
- Fixed crash when interacting with 3 or more styles in the Style Mixer.
- Fixed crash when trying to connect to API location that is unavailable or that was incorrectly entered in the plugin settings.
- Fixed crash after certain API calls to the Motorica servers fail.
- Fixed the Level Editor viewport toolbar becoming hidden when the Motorica Studio Editor Timeline is playing.
- Fixed the Level Editor viewport snap settings also affecting the Motorica Studio Editor viewport.
- Fixed some UI tabs disappearing in Motorica Studio Editor when right-clicking the Motorica Studio Editor tab.
- Fixed tabs spawning as "unrecognized tab" when the Motorica Studio editor layout is restored.
- Fixed crash when "Save Animation" is pressed but no animation has been generated.

#### Notes
- **We are officially dropping support for UE 5.0 and 5.1**. These versions are old, buggy, rarely used, and take up development resources. We will no longer maintain the plugin for these versions and we always recommend you use the latest UE version supported by Motorica Studio.
- Plugin settings are currently separated into multiple entries in `Edit > Project Settings > Plugins` due to codebase organization and limitations of Unreal Engine.

## Motorica Studio v0.2.0
`Released on 2023-Nov-22`

#### New
- Added demo animation assets for 6 styles and 8 presets. *([more info](get-started/included-assets.md#animations))*
- Added demo retargeting assets to demonstrate retargeting from the Motorica skeleton to MetaHuman, Mixamo, and UE5 mannequin. ([more info](get-started/retargeting.md#assets))
- Redesigned the Style Browser UI to show a hierarchical view of styles and style categories.
    - Toggle the checkbox or double-click the style row to enable / disable style blending.
    - Search styles using the search field at the top.
    - The Style Browser state is persistent between editor modes.
- Set up a [website](https://mostudiodocs.pages.dev/) for storing Motorica Studio documentation.

#### Improvement
- The editor mode selector now displays the name and icon of the active editor mode (*Keyframe*, *Preset*, etc.).
- Most toolbar and tab icons in the Motorica Studio Editor have been revised.
- The plugin content directory has been cleaned up and [documented](get-started/included-assets.md).

#### Bug & Crash Fix
- Fixed a bug that causes user login to fail if the user password contains "&" or "+".
- Fixed transform gizmo not updating when left-clicking on the Sequencer timeline.
- Fixed transform gizmo not updating when the selected Actor's transform is changed from the Details (properties) panel.
- Fixed unable to select objects in the Motorica Studio Editor viewport after changing the map in the level editor. *(UE 5.1 and above)*
- Fixed unable to select objects in the Motorica Studio Editor viewport after pressing play-in-editor (PIE). *(UE 5.1 and above)*
- Fixed unable to select objects in the Motorica Studio Editor viewport after a manual or auto save is issued. *(UE 5.1 and above)*
- Fixed potential crash when switching back to *Preset Mode* due to GC of the preset controls panel.
- Fixed root motion being extracted incorrectly.

#### Notes
- *Custom* editor mode is now called *Keyframe* editor mode.
- The `IK Rig` asset "*IK_Motorica*" from *Motorica Studio v0.1.0* is now deprecated. From now on, please use `Plugins > Motorica Studio Content > Retargeting > MotoricaStudio > IK_MoStudio`. References to the old `IK Rig` asset will need to be updated to `Plugins > Motorica Studio Content > Retargeting > MotoricaStudio > IK_MoStudio_legacy`.

## Motorica Studio v0.1.0
`Released on 2023-Jul-26`

- First official release of Motorica Studio for UE 5.0, 5.1, 5.2.
