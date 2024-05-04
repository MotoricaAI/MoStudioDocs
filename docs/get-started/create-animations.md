# Generate Animations

Currently, animations can be generated only in Motorica Studio Editor. This section describes different workflows for generating animations.

## Create Animation for Preset Path

1. Enable [*Preset Mode*](ui-editor-modes.md#preset-mode)

    ![](../assets/images/ms-editor-editor-mode-preset.png)

2. Choose a preset type in the *Preset Controls* panel and configure its parameters.

    ![](../assets/images/ms-editor-preset-controls-panel-configured.png)

3. Select one or more styles in the *Style Browser*.

    ![](../assets/images/ms-editor-style-browser-selected-style-with-style-mixer.png)

4. Press *Generate Animation*.

    ![](../assets/images/ms-editor-generate-animation-button.png)

    A notification will appear when the animation is ready.

    ![](../assets/images/ms-editor-animation-generated-notification.png)

    The animation will be inserted into the *Animation* track of the *Locomotion Actor*.

    ![](../assets/images/ms-editor-timeline-animation-track-with-animation.png)

5. [Preview your animation.](#preview-generated-animation)

## Create Animation for Custom Path

1. Enable [*Keyframe Mode*](ui-editor-modes.md#keyframe-mode)

    ![](../assets/images/ms-editor-editor-mode-keyframe.png)

2. Add a *Locomotion Actor* to the scene.

    ![](../assets/images/ms-editor-toolbar-add-actor-button.png)

3. Select the Actor by left-clicking it in the viewport.

    ![](../assets/images/ms-editor-viewport-with-character-tpose.png)

4. Set the current frame in the *Timeline* to `0`.

    ![](../assets/images/ms-editor-timeline-scrubber-at-zero.png)

5. Move and rotate the Actor using the viewport gizmo.
    
    ![](../assets/images/ms-editor-viewport-gizmo.png)

    !!! tip
        You can precisely set the values for location and rotation in the following places:
        
        - the channel value in the *Timeline* track
        - the channel value in *Sequencer Curves*
        - the channel value in the *Details* panel under "Transform", as long as the *Actor* is selected
        
6. Set the keyframe for *Location* and *Rotation* channels.

    ![](../assets/images/ms-editor-timeline-add-keyframe.png)

    ![](../assets/images/ms-editor-timeline-keyframes-added.png)

    !!! tip
        Enable "auto-key" in the *Timeline* to automatically create keys when you move the character with the gizmo.

        ![](../assets/images/ms-editor-timeline-autokey-button.png)

7. Move the scrubber in the *Timeline* to another frame.

    ![](../assets/images/ms-editor-timeline-scrubber-at-two-with-key.png)

8. Repeat steps 4 to 6 until you are ready with your path.

    ![](../assets/images/ms-editor-timeline-filled-with-curve-editor.png)

9. Select one or more styles in the *Style Browser*.

    ![](../assets/images/ms-editor-style-browser-selected-style-with-style-mixer.png)

10. Press *Generate Animation*.

    ![](../assets/images/ms-editor-generate-animation-button.png)

    A notification will appear when the animation is ready.

    ![](../assets/images/ms-editor-animation-generated-notification.png)

    The animation will be inserted into the *Animation* track of the *Locomotion Actor*.

    ![](../assets/images/ms-editor-timeline-animation-track-with-animation.png)

11. [Preview your animation.](#preview-generated-animation)

## Preview Generated Animation

Generated animations are applied to the corresponding Locomotion Actor and can be previewed in the viewport.

![](../assets/images/ms-editor-viewport-with-character-animated.png)

![](../assets/images/ms-editor-timeline-with-viewport-animation-slides.png)

Drag the playback scrubber or press *Play* to preview your animation.

![](../assets/images/ms-editor-timeline-scrubber-at-two-with-key.png)

![](../assets/images/ue-sequencer-play-button.png)

## Save Animation as Animation Asset

You can save an animation as an `Animation Sequence` asset to your project and use it like any other animation. To do so, press the *Save Animation* button in the details panel.

![](../assets/images/ms-editor-save-animation-button.png)

!!! note
    Make sure that you have selected a locomotion actor in the viewport. Otherwise, you will not see the options in the *Details* panel.

A *Save As* dialog box will appear.

![](../assets/images/ms-editor-save-animation-dialog.png)

1. Select a **folder** where you want to save the animation.
2. Write the **name** of your animation asset.
3. Press **Save** to save the animation in your project.

You can find the saved animation via the *Content Browser*.

![](../assets/images/ue-content-browser-saved-animation-asset.png)

Double-click the *Animation Sequence* asset to preview it using the default UE *Animation Editor*.

![](../assets/images/ue-animation-editor-with-motorica-animation.png)

## Export as FBX

`Animation Sequence` assets can be exported to FBX. This is default functionality provided in the Unreal Engine `Animation Editor`.

To export the animation as FBX:

1. Double-click on the `Animation Asset`

    ![](../assets/images/ue-content-browser-saved-animation-asset-arrow.png)

    ![](../assets/images/ue-animation-editor-with-motorica-animation.png)

2. Click *Export Asset > Animation Data* and export using the default settings.

    ![](../assets/images/ue-animation-editor-export-asset-animation-data.png)

    !!! note
        The image above is using UE 5.3. Other UE versions may show a different UI.
   
[Download UE Plugin](#){ .md-button .md-button--primary }
