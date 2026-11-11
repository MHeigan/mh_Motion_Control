# mh_Motion_Control

Motion-controlled image capture built around edelkrone's compact ONE series
(HeadONE and SliderONE) on Windows -- turntable capture, photogrammetry,
keyframed Bezier moves, HDR panoramas and focus stacks, with every photo saved
at the position it was actually taken. A HeadONE or two and a SliderONE do it
all; the computer does the planning, the measuring and the logging.

**First release (v1.1.0): late November 2026.**
Web page: <https://anti-matter-3d.com/motion-control/>

> mh_Motion_Control is not made or endorsed by edelkrone, but is an example of what's possible with the edelkrone SDK.

## Features

- **Turntable capture** -- a HeadONE on the Turntable Module turns the object
  through any number of positions per turn; a tilt HeadONE and a SliderONE change
  the camera angle and height between rings. Set the first ring's tilt by
  value or from the camera, and CHECK RINGS shows each ring's framing before
  you start. Rings can alternate direction, and a stopped
  capture can be resumed.
- **Photogrammetry** -- turns a turntable capture into a project for
  RealityCapture / RealityScan, Agisoft Metashape or COLMAP, with every
  camera already placed, upright and close to real scale. An optional backlit
  pass makes clean masks that keep only the object, and a one-page HTML spin
  viewer shares the result. A Quick Start explains how it works, and PLAN A
  CAPTURE sets up the capture for you.
- **Linked rig** -- the pan head, slider and tilt head linked as one rig, as
  PAIR does in the edelkrone phone app: every move starts and ends together.
- **Motion** -- the keys are the stored positions P1-P6, as keyposes in the
  edelkrone phone app (K1 = P1, K2 = P2 ...), with Bezier ease in and out in
  a graph editor, Undo, and a playhead the rig can follow for in-between keys.
  Play as a timelapse or a continuous timelapse -- planned like an
  intervalometer, by shoot time and interval in h:mm:ss (or by clip length or
  frames), with the keys read as times into the shoot -- stop motion (waits
  for CONTINUE before each photo) or one smooth real-time move for video, with
  PREVIEW MOVE and STRETCH.
- **Panorama and HDRI** -- a spherical grid worked out from your lens
  (rectilinear or fisheye), sensor and overlap -- or just the rows you choose --
  with zenith and nadir and a map that shows overlap and gaps; 3 to 9
  bracketed exposures per position, stepped by the tool or by the camera's own
  AEB / BKT; PTGui (Papywizard XML) and Hugin projects that open with every
  frame in place.
- **Focus stacking** -- the slider as a macro rail: set the near and far
  ends by hand, and the camera steps through the subject one photo at a time,
  with the step worked out from the lens (magnification, aperture, sensor,
  overlap), typed, or set by the number of photos. The plan shows the
  diffraction cost of each aperture and the photos it needs; a stopped stack
  can be resumed. For a macro lens up to 1:1 or a close-focusing lens; ready
  for focus stacking software.
- **Tilt limits** -- set once by hand with the real lens and cable; the
  joystick, MOVE BY and the panorama rows stay inside them, and the tilt
  reads as camera pitch (+ up, - down).
- **Precision Tuning** -- a short automatic routine learns how your gear
  moves, so every move afterwards is as precise as your rig allows.
- **Manual control** -- joysticks with axis lock, live position readouts,
  MOVE BY / MOVE TO, and the six stored positions (P1-P6) shared with the
  phone app. RIG CONTROL (Ctrl+J) keeps the joysticks, P1-P6 and STOP in a
  small window over every tab.
- **Any camera** -- Nikon and Canon over USB through digiCamControl, or any
  brand through its maker's tethering software (watch folder).
- **Measured** -- an XMP sidecar per photo and a CSV log per session with the
  planned and the measured position, including the camera pitch.
- **Safe by design** -- STOP or Esc halts everything; stall, signal and
  dead-man guards on every move; tilt limits and slider ends respected;
  low-battery checks.
- **Help** -- Help -> How do I... gives each kind of shoot in a few steps; a
  tooltip on every control; a log file per day (Help -> Open Log Folder).
- **Update check** -- Help -> Check for Updates reads this repository's
  releases page.

## Distribution

The release zip holds:

| File | |
|---|---|
| `mh_Motion_Control_Win_x64_v1_1_0.exe` | the program -- unzip and double-click |
| `mh_Motion_Control_v1_1_0_User_Manual.pdf` | user manual |
| `mh_Motion_Control_v1_1_0_Quick_Start.pdf` | quick start: each workflow in a few steps |
| `License_Agreement.pdf`, `License.txt` | licence terms |
| `README.txt` | quick start |
| `THIRD_PARTY_NOTICES.txt` | open-source notices |
| `SHA256SUMS.txt`, `release_manifest.cat`, `manifest.json`, `release_info.txt` | checksums and signed catalogue |
| `_internal\` and other hidden files | runtime files -- do not modify |

No installer, Python or other software is needed.

## Quick start

1. Unzip anywhere and double-click the exe. Close the edelkrone phone app
   first (or switch the phone's Bluetooth off).
2. **CONTROL** tab: tick the units you want and press **CONNECT**. On a
   HeadONE card set *Use as* to Turntable, Pan or Tilt.
3. With a tilt head, set the **tilt limits** (SET LIMITS... in the TILT row).
4. **PRECISION TUNING** tab: **TUNE MY GEAR** (recommended, once per set-up).
5. **TURNTABLE**, **MOTION**, **PANORAMA** or **FOCUS STACK**: set up and press **START**. For
   photogrammetry, start from **PLAN A CAPTURE** on the **PHOTOGRAMMETRY** tab.

## System requirements

| Item | Requirement |
|---|---|
| Windows | 10 or 11, 64-bit |
| Bluetooth | Bluetooth LE -- built in, or a USB adapter |
| edelkrone gear | HeadONE (Turntable Module or Tilt Module) and / or SliderONE |
| Camera (optional) | Nikon / Canon over USB via digiCamControl (free), or any brand via its own tethering software |
| Screen | 1920 x 1080 or larger |

## Supported formats

Photos stay in whatever format the camera saves (JPEG, RAW, TIFF); for
photogrammetry, developed images are matched to the capture by file name.
The tool writes XMP sidecars, CSV session logs and `session.json`; for
panoramas a Papywizard XML (PTGui) and a Hugin `.pto`; for photogrammetry
RealityCapture / RealityScan sidecars and masks, a Metashape reference file,
a COLMAP known-pose model with a run script, and an HTML spin viewer.

## Licence

Free software, (C) 2026 Martin P. Heigan, licensed
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/legalcode). See [LICENSE.md](LICENSE.md).

edelkrone, HeadONE and SliderONE are trademarks of their owner. digiCamControl, RealityCapture, RealityScan, Agisoft Metashape, COLMAP, PTGui, Hugin, Papywizard, Canon, Nikon and other names are the property of their owners and are used only to describe compatibility.

## Security

Each release exe is signed with a Certum code signing certificate, RFC 3161
timestamped, and submitted to Microsoft (WDSI) and VirusTotal before release. Each release carries `SHA256SUMS.txt` and a signed catalogue
(`release_manifest.cat`).

## Keyboard shortcuts

| Key | Action |
|---|---|
| Esc | STOP -- halts all motion on every unit |
| Ctrl+J | RIG CONTROL -- joysticks, P1-P6 and STOP over every tab |
| Ctrl+Z | undo a key change on the MOTION tab |
| Shift (while dragging a joystick) | keep to the axis you started on |
| Ctrl+Q | exit |

## Safety

The tool moves real equipment. Keep the motion path clear of people and
objects, and know where STOP is before you press START.

## Help

The User Manual, the Quick Start and Help -> How do I... in the program answer
most questions, and every control has a tooltip. Help -> Check for Updates
tells you when there is a new version.

## Web page

<https://anti-matter-3d.com/motion-control/> -- the demo video, what it does, and the download.

## More tools

<https://anti-matter-3d.com/tools/>
