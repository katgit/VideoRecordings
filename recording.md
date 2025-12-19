# Recording a Screen Capture Video in the OBS Studio

To start a new recording in OBS, you use the **Controls** dock. Here is the step-by-step process to ensure you start correctly:

### 1. The "Start Recording" Button
In the main OBS window, look at the bottom-right corner. You will see a panel labeled *Controls*.

- Click the *Start Recording* button.
- Once clicked, the button text will change to *Stop Recording*, and a small *Pause* icon will appear next to it.

### 2. Verify it is actually recording
Before you start your actual video recording, check the *Status Bar* at the very bottom of the OBS window:

- **REC**: You should see a red dot and a timer showing how long you have been recording (e.g., 00:00:05).
- **Dropped Frames**: This should stay at 0 (0.0%). If this number starts climbing, your computer is struggling to keep up with the video quality.
- **CPU**: This shows how much power OBS is using.

### 3. Using the Pause Feature (Highly Recommended)
Since you are doing a tutorial, you might need to look up a command.

Click the *Pause* icon (two vertical bars) next to the "Stop Recording" button. This allows you to stop the clock without creating a new file. 
When you unpause, it continues in the same video file, saving you a lot of time in Adobe Premiere later.

### 4. The "Remux" Step

By default, we set your OBS to record in .mkv (the safest format). However, Adobe Premiere Pro cannot open .mkv files. You must convert it to .mp4 before you can edit.

**How to Remux**:

1. Once you finish your recording and click Stop Recording.
2. In OBS, go to the top menu: File > Remux Recordings.
3. Click the three dots (...) under "OBS Recording" to select your file.
4. Click Remux.
5. OBS will instantly create an .mp4 version of your video in the same folder. This is the file you will drag into Adobe Premiere.
