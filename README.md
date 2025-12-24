# VideoRecordings
Video Recordings Workflow
Author: Katia Bulekova

## Software List:

- *OBS Studio*: [https://obsproject.com/download](https://obsproject.com/download)
- *Presentify*: [https://presentifyapp.com/](https://presentifyapp.com/)
- *Adobe Premiere Pro*

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

## Importing into Premiere Pro

Once you have your files in .mp4 or .mov format, here is what you do first:

1. **Create a New Project**: Open Premiere, click "New Project," and name it (e.g., Merged_Data_Videos).
2. **Importing**: Double-click in the Project Panel (bottom left) or press Ctrl+I (Cmd+I on Mac) and select all your converted files.
3. **Create a Sequence**: Drag your first clip onto the Timeline panel. This automatically creates a "Sequence" that matches your video's resolution and frame rate.
4. **Arrange and Merge**: Drag the rest of your clips onto the timeline, snapping them end-to-end in the order you want them to appear.

## Cutting/Removing sections

If you have a section in the middle of a clip (like a mistake in a terminal command) that you want to remove:

1. **Select the Razor Tool**: Press the 'C' key on your keyboard (or click the razor icon in the toolbar).
2. **Make your cuts**: Click on the clip at the exact frame where the unwanted section starts, then click again where it ends.
3. **Delete the section**: Switch back to the Selection Tool (press 'V'), click the middle segment you just created, and hit Backspace or Delete.
4. **Close the gap**: Right-click the empty space (the "gap") and select Ripple Delete. This slides all following clips over so there’s no black screen.

