# Patch Notes - v0.2.0 (Alpha)
## New
- Example [retargeting assets](../../user-guide/retargeting/) have been included to demonstrate and facilitate the process of retargeting from the Motorica skeleton to other character skeletons.
- A [new website](https://motoricaai.github.io/MoStudioDocs/) has been created to store the Motorica Studio **user documentation** and other miscellaneous content, such as the patch notes you are reading.

## Improvement
- The style browser now uses a folder structure, with styles grouped into categories similar to the [web version](https://mogen.motorica.ai/) of MoGen. Styles can be searched using the search field at the top.
- Various icons throughout the Motorica Editor have been updated.
- The editor mode selector now displays the name and icon of the active editor mode.
- The plugin content directory has been cleaned up and [documented](../../user-guide/included-assets/).

## Bug Fix
- Fixed a bug that would cause user login to fail if the user password contains "&" or "+".
- Fixed gizmo transform not updating when jumping (left-clicking) through the Sequencer timeline.
- Fixed gizmo transform not updating when the selected Actor's transform is changed from the Details panel.

## Additional Notes
- New retargeting assets have been added to the plugin. The old `IK Rig` asset `IK_Motorica`, that came with *Motorica Studio v0.1.0*, is now deprecated. The new asset is `Plugin > Content > Retargeting > MotoricaStudio > IK_MoStudio_minimal`. If you have any references to the old IK Rig asset in your project, please update them to `Plugin > Content > Retargeting > MotoricaStudio > IK_MoStudio_legacy`.
