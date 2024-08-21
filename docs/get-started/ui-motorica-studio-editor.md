# Editor User Interface

The *Motorica Studio Editor* window is the place which houses all the main tools that Motorica Studio offers. This is where you can generate animations for your characters.

![](../assets/images/ms-editor.png)

## Launch the Editor

To open the Motorica Studio Editor, click the button with Motorica's logo in the Level Editor toolbar:

![](../assets/images/ue-level-editor-toolbar-motorica-button.png)

You can also open the window via `Window > Motorica Editor` from the main window:

![](../assets/images/ms-editor-open-menu-entry.png)

## Login to Motorica

Motorica Studio requires an internet connection.  You can login via the *Networking* panel:

![](../assets/gifs/workflow-ms-editor-login.gif)

## Toolbar

![](../assets/images/ms-editor-toolbar.png)

!!! note
    The "Save" and "Browse" buttons on the left are always disabled / greyed out. This is not a bug, but a choice made due to technical limitations of the default Unreal Engine asset editor toolbar.

### Level Switchers

There are two buttons that let you switch the current level shown in the Motorica Studio Editor viewport.

![](../assets/images/ms-editor-toolbar-level-switcher-buttons.png)

1. Clicking the "Wireframe Globe" button loads the default "Prototype" level that the Motorica Studio Editor starts with.
    ![](../assets/images/ms-editor-viewport-prototype-level.png)

2. Clicking the "Solid Globe" button loads the level that is currently opened in the main editor window. 
    ![](../assets/images/ue-level-editor-viewport-user-level.png)

    ![](../assets/images/ms-editor-viewport-user-level.png)

    Use this feature to more easily generate animations that fit within your scene.

    !!! note
        Because the plugin does not support generating animations for retargeted characters, you should keep in mind that the above contextualization will suffer from different bone lengths between the source and target skeletons, particularly the hip height.

    !!! warning
        World Partition / Streaming Levels are not supported by the editor. Loading such a level may cause the plugin editor viewport to display gray or black. In that case, you can either use the default “Prototype” level by pressing the Wireframe Globe button, or by loading a non-streaming level.

### Editor Mode Selector

![](../assets/images/ms-editor-toolbar-editor-mode-dropdown.png)

This selector switches the current *editor mode* of the Motorica Studio Editor. Read more about editor modes [on this page](./ui-editor-modes.md).

### Add Actor

The "Add Actor" button in the Motorica Studio Editor toolbar spawns a character in the viewport scene. This character is commonly refered to as a *Locomotion Actor*.

![](../assets/images/ms-editor-toolbar-add-actor-button.png)
![](../assets/images/ms-editor-viewport-with-character-tpose.png)

!!! warning
    When adding an actor to the scene, a track will spawn in the [*Timeline*](ui-editor-modes.md#timeline). **Do not rename this track!**

!!! bug
    When adding an actor for the first time using Motorica Studio, the UE editor will freeze while the mesh loads.

    ![](../assets/images/ms-editor-mesh-wait-popup.png)

    Please wait for the mesh to load and **do not close Unreal Engine**. This can take between 15 seconds and 3 minutes depending on your hardware.

You can spawn more than one Locomotion Actor in the scene:

![](../assets/images/ms-editor-viewport-with-multiple-characters-tpose.png)

!!! note
    Currently, animations can be generated only for Locomotion Actors. If you wish to apply the animations to other characters, you will need to [retarget](retargeting.md) the animations.

### Settings

![](../assets/images/ms-editor-toolbar-settings-button.png)

The "Settings" button opens the main Motorica Studio settings. This is a shorcut to the usual `Edit > Project Settings > Plugins > Motorica Studio`.

### Navigation Buttons

![](../assets/images/ms-editor-toolbar-additional-resource-buttons.png)

The end of the toolbar hosts several buttons that help you navigate to several useful resources:

1. **Motorica Studio Documentation** - A place where you can learn how to use and leverage Motorica Studio's tools. You are currently reading this.
2. **Community Page** - A place where you can engage with Motorica's community. Currently, we have a [Discord](https://discord.com/invite/KWRqNzcjYA) server with over 3k members!
3. **Bug Report Page** - A place where you can report bugs, share feedback, and request new features.

## Tabs

!!! TODO
    This section is not yet fully documented. However, tabs specific to editor modes [are documented](ui-editor-modes.md).

### Networking Panel

The *Networking* panel is only used for logging in to Motorica. That's it!

![](../assets/gifs/workflow-ms-editor-login.gif)

### Style Browser

![](../assets/images/ms-editor-tab-style-browser.png)

### Style Mixer

![](../assets/images/ms-editor-tab-style-mixer.png)

### Viewport

![](../assets/images/ms-editor-tab-viewport.png)
