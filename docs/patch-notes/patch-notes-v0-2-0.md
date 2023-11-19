# Patch Notes - v0.2.0 (Alpha)
## New
- Added [**assets**](../../user-guide/retargeting/) to demonstrate and facilitate the process of retargeting from the Motorica skeleton to other character skeletons.
- Set up a [**website**](https://motoricaai.github.io/MoStudioDocs/) to store the Motorica Studio user documentation. It also contains other miscellaneous content such as the patch notes you are reading.

## Improvement
- The **Style Browser** now uses a folder structure, with styles grouped into categories similar to the [web version](https://mogen.motorica.ai/) of MoGen. Styles can be searched using the search field at the top, and the mixing of styles is controlled via a checkbox.
- The **editor mode selector** now displays the name and icon of the active editor mode.
- Most toolbar and tab **icons** in the Motorica Studio Editor have been revised.
- The **plugin content** directory has been cleaned up and [documented](../../user-guide/included-assets/).

## Bug Fix
- Fixed a bug that causes **user login** to fail if the user password contains "&" or "+".
- Fixed **transform gizmo** not updating when left-clicking on the Sequencer timeline.
- Fixed **transform gizmo** not updating when the selected Actor's transform is changed from the Details panel.
- Fixed unable to **select objects** in the Motorica Studio Editor viewport after changing the map in the level editor. *(UE 5.1 and above)*
- Fixed unable to **select objects** in the Motorica Studio Editor viewport after pressing play-in-editor (PIE). *(UE 5.1 and above)*
- Fixed unable to **select objects** in the Motorica Studio Editor viewport after a manual or auto save is issued. *(UE 5.1 and above)*
- Fixed **potential crash** when switching to *Preset Mode* due to GC of the preset controls panel.

## Additional Notes
- New retargeting assets have been added to the plugin. The old `IK Rig` asset `IK_Motorica`, that came with *Motorica Studio v0.1.0*, is now deprecated. The new asset is `Plugin > Content > Retargeting > MotoricaStudio > IK_MoStudio_minimal`. If you have any references to the old IK Rig asset in your project, please update them to `Plugin > Content > Retargeting > MotoricaStudio > IK_MoStudio_legacy`.
