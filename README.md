5o5o Noise Meter 1.7 — Release Notes and User Guide
Version: 1.7
Documentation date: October 24, 2026

5o5o Noise Meter is an Android application for observing sound frequencies, recording changes in noise, and documenting on-site conditions. Its real-time spectrum, frequency history, screenshots, audio recording, and video recording help users compare noise at different times and locations.
1. What Changed Between Versions 1.5 and 1.7?
The following summary covers development and fixes made between versions 1.5 and 1.7, including cumulative improvements from intermediate releases. Not every feature listed was first introduced in version 1.7.
1.1 A Home Screen That Makes Observation Easier
- Added the Special Edition interface, bringing the real-time dB(A) reading, dominant frequency, real-time spectrum, and frequency history together, with easier access to common controls.
- Renamed the color themes: “Iron Gray Metallic Observation” is now “Special Edition,” “Classic” is now “Professional Edition,” and “Classic Green” is now “Fluorescent Professional Edition.”
- Updated the Fluorescent Professional Edition so that the spectrogram and spectrum curve use coordinated colors.
- Added pinch-to-zoom to the home-screen spectrogram for closer inspection of frequency history.
- Simplified the text below the Special Edition reading while retaining the “A-weighted estimate” label.
1.2 More Consistent Sound Level and Dominant Frequency Calculations
- The Special Edition home screen uses A-weighting for sound level estimation. Video mode uses the same A-weighting algorithm and calibration offset.
- Video mode and the home screen now use the same full-spectrum dominant frequency selection rules, reducing differences caused by inconsistent calculation methods.
- The “dB+” and “dB−” controls in video mode now increase or decrease the calibration offset by 2 dB per tap. This offset is shared with the home screen.
- Existing calibration settings are preserved. After installing version 1.7, readings will still change with the environment. Having calibrated the app to 36 dB(A) in one environment does not mean it should display 36 everywhere.
1.3 More Complete Video Recording
- Opening the video screen now starts a preview. Recording begins only after tapping “Start,” allowing you to adjust the framing first.
- You can choose whether to display the sound level, low-frequency spectrum, and date and time. Selected overlays are included in the exported MP4.
- Adjusted video orientation and rendering to address rotation, mirroring, and overlapping overlays.
- Moved “Flip” and “Flash” to either side of the Start button and fixed controls appearing too close to, or beyond, the edges of narrow screens.
- Removed the aspect-ratio switch. All video recordings now use a portrait resolution of 720 × 1280 pixels in MP4 format.
- Improved finalization and saving after recording stops to reduce waiting. Actual processing time still depends on the phone, recording length, and storage conditions.
1.4 App Watermarks on Screenshots and Videos
- Added a “5o5o Noise Meter” watermark to the video preview and exported recordings.
- Added a “5o5o Noise Meter” watermark to the lower-left corner of exported screenshots to help identify their source.
1.5 Fixes for Issues That Could Affect Recording
- Fixed resource conflicts when starting or stopping microphone capture, switching screens, and returning from the background, reducing the risk of crashes or capture errors.
- Fixed an issue where rapidly starting and stopping audio recording could start a new recording before the previous file had finished saving.
- Fixed issues affecting temporary-file saving when navigating back during video recording. Pressing Back again while saving now prompts you to wait.
- Fixed an issue where different audio and video encoder startup times could cause the first samples or frames to be lost, improving the completeness of video beginnings.
- Fixed issues involving the Stop button, timer, and camera state after switching cameras during recording.
- Added handling for extremely short videos, file-write failures, and insufficient memory during screenshot capture, preventing incomplete clips from being exported as normal videos.
- Updated the About screen to consistently display the actual installed version number: 1.7.
2. Getting Started
1. Open the app and grant microphone permission. Grant camera permission when you first open the video screen. On older Android versions, grant storage permission if requested so files can be saved.
2. Place the phone at the location you want to observe without blocking its microphone openings. Minimize interference from handling noise, speech, and wind blowing across the phone.
3. Wait a few seconds, then observe the reading, spectrum, and frequency history.
4. Tap “Screenshot,” “Record Audio,” or “Video” as needed to save a record.
Opening the app does not automatically start saving an audio recording. Opening the video screen does not automatically start video recording either.
3. Understanding the Numbers and Charts
Item	Meaning
Large dB(A) reading	An estimated sound level calculated using A-weighting and the calibration offset, useful for observing overall changes.
Dominant frequency in Hz	A frequency currently standing out in the spectrum. Hz indicates frequency, not loudness, direction, or distance.
Real-time spectrum	Shows the relative strength of different frequencies. The horizontal axis represents frequency; the vertical axis shows dBFS.
Frequency history / spectrogram	Shows how frequency content changes over time, making it easier to identify persistent sounds or repeated starts and stops.


The dBFS values in the spectrum and the dB(A) reading above it represent different quantities and do not need to match. A-weighting reduces the contribution of low frequencies to the overall reading. When investigating low-frequency noise, also examine the spectrum and save audio recordings.

The home screen and video mode use the same calculation methods, but they sample at different times. Environmental changes can therefore still produce different instantaneous readings. The small low-frequency chart in video mode displays only 0–1 kHz. Because the full-spectrum dominant frequency may exceed 1 kHz, its label may fall outside the range shown in that chart.
4. Taking Screenshots and Recording Audio or Video
Screenshots
Wait for the display to stabilize, then tap “Screenshot” to save the current screen as a PNG image. For closer inspection, tap “Pause” first, take the screenshot, and then tap “Resume.”
Audio Recording
Tap “Record Audio” on the home screen to begin. Tap “Stop” when finished and wait for saving to complete. Audio recordings are saved as WAV files. Wait until the controls become available again before starting another recording.

“Pause” freezes the display; it does not replace the recording’s “Stop” control. Keep the app in the foreground when continuous audio recording is required. Opening another screen or moving the app to the background may end and save the current recording.
Video Recording
1. Tap “Video” on the home screen and check the framing and orientation.
2. Select the sound level, low-frequency spectrum, and date and time overlays as needed.
3. Tap the red “Start” button. Once the recording indicator appears, keep the phone steady.
4. Tap the circular button again to stop. Wait for saving to complete and return to the home screen.
“Flip” switches between the front and rear cameras. Switching cameras during recording saves the current clip and starts a new one, so you may get multiple video files. “Flash” requires the currently selected camera to support a recording light.

Pressing Back during recording ends and saves the recording. Wait while saving is in progress, and do not force-close the app. If the phone has already been calibrated, avoid changing “dB+” or “dB−” unnecessarily, because these controls also affect the home-screen reading.
5. Where Are Saved Files Stored?
Open the system gallery or file manager and look in the phone’s internal storage:
File type	Folder	Format
Screenshots	Pictures/5o5o噪音计	PNG
Audio recordings	Music/5o5o噪音计	WAV
On-site videos	Movies/5o5o噪音计	MP4


The folder names above are shown exactly as they appear on the device.

File names usually begin with 5o5o_. If you cannot find a file, search for this prefix in the file manager. Use the system gallery or file manager to share, rename, and organize files. Recordings captured by the app are stored locally on the phone and are not automatically uploaded to a server.
6. Things to Know Before and After Upgrading from Version 1.5
- Back up important screenshots, audio recordings, and videos first. Install the update over the existing version whenever possible. Do not uninstall the app or clear its data simply to upgrade.
- Installing over an existing version requires the same package name and signing identity. If Android reports “App not installed” or a signature conflict, do not immediately uninstall the old version. First confirm the installation package’s source and the appropriate upgrade method.
- After upgrading, check microphone and camera permissions, along with your existing theme and calibration settings. Recheck calibration when changing phones; do not assume the old phone’s settings are equally accurate on another device.
- Phone microphones and audio processing vary. This app is intended for observing, recording, and comparing changes. It does not replace a calibrated professional sound level meter, and frequency and dB(A) readings alone cannot determine a sound source’s location or distance.
- Testing for this release covered the main workflows on one HONOR phone running Android 16. Other devices and operating systems may still have compatibility differences.
7. Frequently Asked Questions
Why is the reading not changing?
First check whether the display is paused and whether microphone permission has been granted. Close other apps using the microphone, then reopen the relevant screen.

Why is the video preview black, or why does Flash do nothing?
Check camera permission and whether another app is using the camera. Some front-facing cameras do not have a recording light. Save your current recording, then reopen the video screen and try again.

Why do I need to wait after stopping?
The app must finalize the audio and video streams and save the file. The waiting time depends on the recording length and the phone’s condition. Wait until saving is complete before starting another operation.

What should I do if saving fails?
Check available storage and permissions, and keep a record of the error message. Do not immediately uninstall the app or clear its data, as this may delete files still temporarily stored within the app.
License
This application is free of charge and is distributed under a “Free Use with Attribution Required” license. See LICENSE.txt for details.

Free installation and use for personal purposes are permitted, provided that attribution to “雨花石子记” (Yuhua Shizi Ji) is retained. Commercial use, repackaging after removing copyright notices, reverse engineering, and cracking are prohibited.

All data is stored locally on the device and is not uploaded to any server.
