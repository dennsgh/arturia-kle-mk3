# Arturia KeyLab Essential MK3 FL Studio Script

## Overview

This project provides an advanced MIDI controller script for the **Arturia KeyLab Essential MK3**, specifically designed for **FL Studio**. It allows deeper integration of the controller with FL Studio's internal features like channels, plugins, mixer, and transport, and includes advanced features such as plugin parameter mapping and screen feedback.

The script offers the following features:
- Navigation between different FL Studio windows (Mixer, Channel Rack, Browser, Playlist).
- Control of FL Studio’s transport (Play, Stop, Record, Rewind, Fast-Forward, Looping, etc.).
- Control of mixer parameters (Volume, Panning, Muting, Soloing, etc.).
- Parameter mapping for native plugins (FLEX, Sytrus, FPC, etc.).
- Integration with Arturia's **Analog Lab** and **V Collection**.
- Visual feedback via the Arturia KeyLab’s built-in display and LEDs.
- Automatic handling of track selection and effect management.

## Table of Contents

- [Files](#files)
- [Installation](#installation)
- [Usage](#usage)
- [File Details](#file-details)
- [Supported Plugins](#supported-plugins)
- [Contributing](#contributing)
- [License](#license)

## Files

This project includes the following Python files, each serving a specific purpose:

- `KLEss3Plugin.py`: Handles MIDI mapping for plugin parameters, allowing smooth control of various FL Studio native plugins.
- `KLEss3Navigation.py`: Manages navigation within FL Studio, including controlling transport, mixer, and various windows (Browser, Channel Rack, Mixer, Playlist).
- `KLEss3Return.py`: Provides visual feedback on the KeyLab’s screen, such as volume levels, panning, track names, and more.
- `KLEss3Buttons.py`: Defines behavior for contextual buttons on the controller.
- `device_KLEss3.py`: Main script that initializes and manages the overall integration with FL Studio.
- `MachineState.py`: Defines constants representing the state of various hardware controls (e.g., encoders, DAW connection).
- `ArturiaVCOL.py`: Contains mapping for Arturia V Collection plugins.
- `LedIds.py`: Defines LED mappings for feedback lights on the KeyLab.
- `Icons.py`: Contains icon mappings for the KeyLab display.
- `KLEss3Pages.py`: Handles the display pages on the KeyLab, such as displaying plugin parameters or mixer information.
- `KLEss3Display.py`: Manages the lower-level screen rendering logic for the KeyLab.
- `KLEss3Process.py`: Main MIDI event processor that routes incoming MIDI events to their respective handlers.
- `KLEss3Dispatch.py`: Dispatches MIDI events to the appropriate functions.
- `Displays.py`: Auto-generated file that defines display types used in the KeyLab.
- `ArturiaCrossKeyboardKLEss3.py`: Shared functions across different Arturia controllers.

## Usage

Once installed, you can use your Arturia KeyLab Essential MK3 to control various aspects of FL Studio:

- **Transport Controls**: Use the Play, Stop, Record, Rewind, Fast-Forward, and Loop buttons to control FL Studio’s transport.
- **Mixer Control**: Use the faders and knobs to control mixer parameters like volume and panning.
- **Plugin Control**: When a supported plugin is focused, knobs and faders will map to specific parameters within that plugin. You can also navigate through plugin presets.
- **Screen Feedback**: The KeyLab's display will show useful feedback, including current track names, plugin parameter changes, and transport status.
- **Part/Track Navigation**: Use the Part buttons and main encoder to navigate through tracks, patterns, and playlists.

## File Details

### KLEss3Plugin.py
This script handles MIDI mappings for various native FL Studio plugins, allowing the KeyLab to automatically control different plugin parameters. A specific parameter map is created for each supported plugin.

### KLEss3Navigation.py
Manages navigation through different windows in FL Studio. It handles transport, mixer, and general DAW commands like saving, undoing, and switching between windows.

### KLEss3Return.py
This script provides visual feedback to the KeyLab's display and LEDs, showing track names, volume levels, plugin parameters.

### KLEss3Buttons.py
Handles the behavior of the contextual buttons on the KeyLab. The buttons change dynamically depending on the focused window (e.g., Mixer, Channel Rack, Browser).

### device_KLEss3.py
The main script for initializing and managing the KeyLab integration with FL Studio. It sets up event handlers for transport, navigation, and mixer control.

### ArturiaVCOL.py
Contains support for Arturia's **V Collection** plugins, allowing for seamless control over these instruments within FL Studio.

## Supported Plugins

The script supports a wide range of FL Studio native plugins, including but not limited to:

- **FLEX**
- **FPC**
- **FL Keys**
- **Sytrus**
- **Harmless**
- **Harmor**
- **MiniSynth**
- **PoiZone**
- **Sakura**
- **BooBass**
- **SimSynth Live**
- **Autogun**
- **Drumaxx**
- **Toxic Biohazard**

In addition to native plugins, the script also integrates with **Arturia V Collection** and **Analog Lab**.

## Contributing

Contributions to this project are welcome! If you find any issues or have suggestions for new features, feel free to submit a pull request or raise an issue.

To contribute:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/new-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
