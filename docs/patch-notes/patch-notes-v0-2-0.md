# Patch Notes - v0.2.0
## New
- Added **demo animations** for 6 styles and 8 presets. *([more info](../../user-guide/included-assets/#animations))*
- Added **demo retargeting assets** to demonstrate retargeting from the Motorica skeleton to MetaHuman, Mixamo, and UE5 mannequin. ([more info](../../user-guide/retargeting/#assets))
- Set up a [**website**](https://motoricaai.github.io/MoStudioDocs/) for storing Motorica Studio documentation.

## Improvement
- Redesigned the **Style Browser** UI to show a hierarchical view of styles and style categories.
    - Toggle the checkbox or double-click the style row to enable / disable style blending.
    - Search styles using the search field at the top.
    - The Style Browser state is persistent between editor modes.
- The **editor mode selector** now displays the name and icon of the active editor mode (*Keyframe*, *Preset*, etc.).
- Most toolbar and tab **icons** in the Motorica Studio Editor have been revised.
- The **plugin content** directory has been cleaned up and [documented](../../user-guide/included-assets/).

## Bug Fix
- Fixed a bug that causes **user login** to fail if the user password contains "&" or "+".
- Fixed **transform gizmo** not updating when left-clicking on the Sequencer timeline.
- Fixed **transform gizmo** not updating when the selected Actor's transform is changed from the Details (properties) panel.
- Fixed unable to **select objects** in the Motorica Studio Editor viewport after changing the map in the level editor. *(UE 5.1 and above)*
- Fixed unable to **select objects** in the Motorica Studio Editor viewport after pressing play-in-editor (PIE). *(UE 5.1 and above)*
- Fixed unable to **select objects** in the Motorica Studio Editor viewport after a manual or auto save is issued. *(UE 5.1 and above)*
- Fixed **potential crash** when switching back to *Preset Mode* due to GC of the preset controls panel.
- Fixed **root motion** being extracted incorrectly.

## Additional Notes
- The `IK Rig` asset "*IK_Motorica*" from *Motorica Studio v0.1.0* is now deprecated. From now on, please use `Plugins > Motorica Studio Content > Retargeting > MotoricaStudio > IK_MoStudio`. References to the old `IK Rig` asset will need to be updated to `Plugins > Motorica Studio Content > Retargeting > MotoricaStudio > IK_MoStudio_legacy`.
