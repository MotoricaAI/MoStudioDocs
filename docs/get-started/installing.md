# Install Motorica Studio

Motorica Studio currently does not follow a strict release cycle. Stay updated by joining our [Discord](https://discord.com/invite/KWRqNzcjYA) server for release announcements and check the latest changes in the [patch notes](../changelog.md).

## System Requirements

Unreal Engine needs to be installed to use Motorica Studio. A list of supported UE versions and target platforms is available in the [Downloads](../downloads.md) page.

## Register at Motorica

Motorica Studio requires an account. To register, go to the [Motorica website](https://www.motorica.ai/).

For your security:

- Use a combination of **numbers**, **symbols**, and **upper and lower case letters** in your password.
- Use a password that is **16 characters long** or more.
- Use a **unique** password (i.e. you have not used the password anywhere else).

## Download Motorica Studio

Go to the [Downloads](../downloads.md) page.

## Install Motorica Studio
### Install for All Projects

1. Extract the downloaded `.zip` to Unreal Engine's installation folder.
    - The default Windows location is `C:\Program Files\Epic Games\UE_[version]\Engine`
2. Load any UE project
      - For C++ projects, build and run using your IDE (e.g. Visual Studio):

        ![](../assets/images/open-project-cpp.png)

      - For BP projects, use the project executable:        

        ![](../assets/images/open-project-bp.png)

3. Enable the plugin via `Edit > Plugins > Installed | Animation > Motorica Studio`
4. Restart the UE editor
5. [Configure Motorica Studio](#configure-motorica-studio)

!!! note
    Each UE project has its own list of enabled plugins and plugin settings. Therefore, you must enable and configure Motorica Studio *separately* for each project.

### Install for a Single Project

1. Extract the downloaded `.zip` to your project's root folder
2. Load your UE project
      - For C++ projects, build and run using your IDE (e.g. Visual Studio):

        ![](../assets/images/open-project-cpp.png)

      - For BP projects, use the project executable:

        ![](../assets/images/open-project-bp.png)

3. Enable the plugin via `Edit > Plugins > Installed | Animation > Motorica Studio`
4. Restart the UE editor
5. [Configure Motorica Studio](#configure-motorica-studio)

## Configure Motorica Studio

If Motorica Studio was installed correctly, you will see this button in the level editor toolbar:

![](../assets/images/ue-level-editor-toolbar-motorica-button.png)

### Open Plugin Settings

Open the Motorica Studio editor and press the "Settings" button in the toolbar:

![](../assets/images/ms-editor-toolbar-settings-button.png)

Alternatively, navigate to `Edit > Project Settings > Plugins > Motorica Studio Networking`.

![](../assets/images/menu-edit-project-settings.png)
![](../assets/images/project-settings-plugins-motorica-studio.png)

### Configuration Values

- **API Location** - Write `https://mogen.motorica.ai/api/v1/`.
- **Email** - Write your Motorica account email.
- **Password** - Write your Motorica account password.

    !!! warning
        **The password is stored in plain-text in the plugin config file** at `YourProjectRoot > Config > DefaultMotoricaStudioConfig.ini`.
        
        Make sure to use a **unique password**!

        Make sure to **delete the config file when copying your project**!

![](../assets/images/motorica-studio-settings-example.png)

### Verify the Configuration

Verify that you entered your information correctly by logging in from the Motorica Studio Editor:

1. Open the *Motorica Studio editor*.

    ![](../assets/images/ue-level-editor-toolbar-motorica-button.png)

2. Login from the *Networking* panel. 

    ![](../assets/gifs/workflow-ms-editor-login.gif)

    If you see **"Login successful!"**, then your configuration was correct.

    If you see **"Login failed!"**, your configuration might be wrong. Please double-check the information in the plugin settings and try again. If the issue persists, reach out on [Discord](https://discord.com/invite/KWRqNzcjYA).
