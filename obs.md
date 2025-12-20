# OBS Studio Settings 

## Table of Contents
* [Video Settings for Sharp Text](#video-settings-for-sharp-text)
* [Audio Settings for Crystal Clarity](#audio-settings-for-crystal-clarity)
* [Dial in the Sweet Spot Volume](#dial-in-the-sweet-spot-volume)
* [Setting up the Pro Sound Filters](#setting-up-the-pro-sound-filters)
* [OBS Recording Hotkeys for macOS](#obs-recording-hotkeys-for-macos)
* [OBS Screen Capture Setup for macOS](#obs-screen-capture-setup-for-macos)

----
Use the following settings for the best video quality when screen capturing. 

## Video Settings for Sharp Text

1. Click *Settings* (bottom right corner)
2. Click the *Output* tab in the left sidebar
3. At the top, change *Output Mode* from "Simple" to "Advanced."

Stay on the "Output* tab and click the *Recording* sub-tab at the top.
- **Recording Format**: Find the dropdown and select **mkv** (remember to "Remux" to MP4 later under File > Remux Recordings).
- **Video Encoder**: Look for *NVIDIA NVENC H.264* or *AMD HW H.264*. If you don't see those, use **x264**.
- **Rate Control**: You may need to scroll down the tab to see this setting. Find the dropdown that likely says "CBR" and change it to CQP. **Note**: If you are using the x264 (CPU) encoder, "CQP" is called CRF. They serve the same purpose.
- **CQ (or CRF) Level**: Set this to 20. (Lower is higher quality; 16 is nearly perfect, 23 is standard).

**Resolution & FPS (The "Video" Tab)**<br>
Switch to the Video tab in the left sidebar of the Settings window.

- Base (Canvas) Resolution: Set this to 1920x1080 (or use the resolution for your input screen).
- Output (Scaled) Resolution: Set this to 1920x1080 as well. This ensures no blurring of your terminal text.
- Common FPS Values: Set this to 60 (or 30 if your computer is older).

**Tip**: If your input resolution is higher than the output resolution, go to the Video tab and ensure the Downscale Filter is set to Lanczos—this is the sharpest setting for text.

## Audio Settings for Crystal Clarity

To use your headphone microphone and ensure it sounds professional for your Linux tutorial, you need to tell OBS exactly which device to use and then "mix" it so it's clear and centered.

**Select your Headphone Mic**:

1. Open Settings in OBS (bottom right).
2. Go to the Audio tab on the left.
3. Look for the Global Audio Devices section.
4. Find Mic/Auxiliary Audio and click the dropdown. Select your specific headset name (e.g., "Logitech G733 Mic" or "Headset Microphone"). The Amazon headset is *Plantronics Blackwire 5220 Series*
5. Click Apply and OK.

**Configure for "Mono" (Important)**:<br>

Headset microphones often record in only the "Left" channel, which means your viewers might only hear you in their left ear.

1. Look at the *Audio Mixer* (the volume bars moving in the main OBS window).
2. Click the three vertical dots (or gear icon) next to your Mic/Aux bar.
3. Select Advanced Audio Properties.
4. Find your Mic/Aux in the list and check the box for Mono. This ensures your voice is centered in both ears.
5. Close the window.

## Dial in the Sweet Spot Volume 

While speaking at your normal teaching volume, watch the green/yellow/red bar in the Audio Mixer:
**The Goal**: You want your voice to consistently stay in the Yellow Zone (between -15dB and -10dB).

*The Adjustment:* If you are hitting the Red, slide the blue volume fader to the left. If you stay in the Green, slide it to the right.



## Setting up the Pro Sound Filters

Since headset microphones are positioned close to your mouth, they are prone to picking up heavy breathing, keyboard clicks, and background hum. Use these filters in OBS to achieve a professional broadcast sound.

### How to Apply
1. Go to the **Audio Mixer** in the main OBS window.
2. Click the **three vertical dots** (or gear icon) next to your **Mic/Aux**.
3. Select **Filters**.
4. Click the **+** icon in the bottom-left to add the following filters in this specific order:

| Filter Name | Why you need it | Recommended Setting |
| :--- | :--- | :--- |
| **Noise Suppression** | Eliminates background hum, AC noise, and computer fans. | Method: **RNNoise** (Higher quality, uses more CPU). |
| **Compressor** | Automatically lowers your volume when you are loud and boosts it when you whisper. | **Ratio: 4.00:1** (Standard for speech). Leave others at default. |
| **Limiter** | Acts as a "hard ceiling" to prevent your audio from ever distorting or "clipping." | **Threshold: -3.00 dB**. |

### Final Verification
Once applied, speak at your loudest "teaching voice." The level meter for your mic in the OBS mixer should stay in the **Yellow zone** and should never hit the very end of the **Red zone**.


## OBS Recording Hotkeys for macOS

To avoid showing the OBS window at the start and end of your Linux tutorials, use these keyboard shortcuts.

### 1. Configure Hotkeys in OBS
1. Go to **Settings > Hotkeys**.
2. Search for "Recording".
3. Assign the following combinations:

| Action | Shortcut |
| :--- | :--- |
| **Start Recording** | <kbd>⌥ Option</kbd> + <kbd>⌘ Cmd</kbd> + <kbd>S</kbd> |
| **Stop Recording** | <kbd>⌥ Option</kbd> + <kbd>⌘ Cmd</kbd> + <kbd>E</kbd> |
| **Pause/Unpause** | <kbd>⌥ Option</kbd> + <kbd>⌘ Cmd</kbd> + <kbd>W</kbd> |

### 2. Enable Global Input (macOS Permission)
For these keys to work while you are typed inside your Linux Terminal, you must give OBS permission to monitor your keyboard:
1. Open **System Settings** > **Privacy & Security** > **Accessibility**.
2. Toggle **OBS** to **ON**.
3. Open **Privacy & Security** > **Input Monitoring**.
4. Toggle **OBS** to **ON**.


On macOS (especially in newer versions like Sequoia or Sonoma), the Input Monitoring list is often empty because it is "permission on demand." This means an app won't appear there until it explicitly asks the system for that specific permission.

If OBS hasn't triggered that request yet, you can manually force it into the list. Here is how to fix it:

- Open System Settings > Privacy & Security > Input Monitoring.
- Look for a small plus (+) icon at the bottom of the (empty) list. Note: You may need to authenticate with your Touch ID or password first.
- A file browser will open. Go to your Applications folder, select OBS, and click Open.

OBS will now appear in the list. Ensure the toggle next to it is turned ON (blue). OBS will likely show a popup saying it needs to "Quit & Reopen" to apply the settings. Click Quit & Reopen.

### 3. Advanced Settings
To ensure the shortcuts always trigger, go to **Settings > Advanced** in OBS and set **Hotkey Focus Behavior** to `Never disable hotkeys`.

## OBS Screen Capture Setup for macOS

For the highest quality text rendering in Linux terminal tutorials, follow these steps:

1. **Add Source**: In the **Sources** dock, click `+` > `macOS Screen Capture`.
2. **Method**: Choose `Display Capture` to ensure all terminal popups and browser links are recorded. Select `Window Capture` for cleaner focus (if you only need to capture a single window, for example, an OnDemand session within a browser.
3. **Cursor**: Ensure `Show Cursor` is checked.
4. **Resolution Check**: 
   * If the capture is too large for the canvas, right-click the source in the preview.
   * Go to `Transform` > `Fit to Screen`.
5. **Filters (Optional)**: 
   * If text appears "shimmery," go to `Settings > Video` and set `Downscale Filter` to `Lanczos`.
