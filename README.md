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

## Adding Captions

### Generate the Initial Transcript

Before you create the visual captions, Premiere needs to "listen" to your video.

1. Open the Text Panel: Go to Window > Text.
2. Select Transcript Tab: Click on the Transcript tab at the top of the panel.
3. Transcribe: Click the Transcribe button.

*Tip*: In the settings that pop up, you can select the specific language and choose to "Transcribe in-point to out-point" if you only want a certain section captioned.


### Review and Edit the Text


1. Search and Replace: Use the search bar in the Transcript panel to find common misspellings (e.g., if it wrote "hawk" instead of "awk").
2. Manual Correction: Double-click any word in the transcript to fix typos or punctuation.
3. Create the Caption Track: Once the transcript is perfect, you turn it into visual blocks on your timeline.
4. Click the CC Icon: At the top of the Text panel, click the CC (Create Captions) button.

**Caption Preferences**: A window will appear. For technical tutorials, use these settings:
- Maximum length in characters: 42 (keeps them easy to read).
- Minimum duration in seconds: 2.0.
- Lines: Single (this prevents the text from covering too much of your terminal screen).

**Create**: Click Create Captions. A new "Subtitle" track will appear at the very top of your timeline.

## Style Your Captions (Updated for 2025)

In the 2025 version, styling is primarily handled in the Properties panel.

- Select All Captions: Click and drag a box over all the new caption blocks on your timeline.
- Open Properties: Go to Window > Properties.
- Font: Use a clean, sans-serif font like Arial or Roboto.
- Color: White text with a Black Background (set to ~75% opacity) is the standard for high visibility.
- Position: Move the "Align" slider to ensure the text isn't blocking your code or terminal window.

**Pro Tip for Tutorials**: "Burned-In" vs. "Closed"

When you go to Export (Ctrl + M), look at the Captions tab:

- *Burn Captions into Video*: This makes the text a permanent part of the video file. This is best for tutorials shared on social media or direct file links.
- *Create Sidecar File (.srt)*: This creates a separate file that viewers can turn on or off (like on YouTube).
