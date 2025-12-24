# VideoRecordings
Video Recordings Workflow
Author: Katia Bulekova

## Software List:

- *OBS Studio*: [https://obsproject.com/download](https://obsproject.com/download)
- *Presentify*: [https://presentifyapp.com/](https://presentifyapp.com/)

## Preparation

1. OBS Studio Setup: [obs.md](obs.md)


## Video Recording

**Pro-tips**:

- For each video create a separate drectory
- Generate a file where you keep the verbose version of what you plan to say in the recording
- Record small sections - it will be easier to re-record when/if needed.
- Name the file so they are sorted in the order they will be merged, i.e. Linux_01_Introduction, Linux_02_Terminal, etc.

To start a new recording in OBS, use the Controls dock. The step-by-step process of setting OBS for the screen recording and screen capture is described here: [recording.md](recording.md)

Once the Recording is set up and the HotKeys are set, click on the window you want to capture and use hotkeys to start (⌥ Option + ⌘ Cmd + S) ,pause (⌥ Option + ⌘ Cmd + W)  and stop (⌥ Option + ⌘ Cmd + E) recording

## Remux

If the recordings are generated in the mkv format, use the "Remux" in OBS to convert them into mp4 format: File -> Remux Recordings
