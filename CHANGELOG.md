# Changelog -- mh_Motion_Control

## 1.1.0 -- November 2026

The first public release. mh_Motion_Control turns edelkrone HeadONE and SliderONE units
into a capture rig you can measure and repeat on Windows: turntable spins and
photogrammetry, panoramas and HDRI, timelapse, stop motion, smooth real-time
video moves and focus stacks -- with every photo recorded at the position it was
actually taken.

### New -- Your gear as one rig
- Scan and connect with unit cards: tick the units you want and leave the rest
  free for the phone app.
- Link the pan head, slider and tilt head as one rig, as in the edelkrone app:
  every move of the rig starts and ends together.
- "Use as" sets a HeadONE as Turntable, Pan or Tilt -- and the TURNTABLE and
  PANORAMA tabs offer to change it when they need to. Give each unit a name of
  your own, shown in this tool only, with Restore original name. Both are
  remembered.
- Status strip with every unit's battery level; mute the units' beeps.
- RIG CONTROL (Ctrl+J): the joysticks and the stored positions in a small
  window that stays over every tab.
- Stored positions P1-P6 -- the same keyposes the edelkrone app uses: click to
  go there, SET to store, right-click to clear.
- MOVE BY / MOVE TO for exact moves, ZERO for any readout, and UNWIND to turn a
  wound-up camera cable back the way it came.
- Tilt limits taught by hand, so the lens and cable always stay clear of the
  rig -- on every tab.
- STOP and Esc halt all motion, from any tab or window.

### New -- Precision Tuning
- A short automatic routine learns how your units move with your camera and
  lens mounted, so every precise move lands where it should. Results in plain
  words, with Copy Results.

### New -- Turntable capture
- Any number of positions per turn and several photos per position, Precise or Fast.
- Rings: the tilt HeadONE and the SliderONE change the camera angle and height
  between rings, with alternate directions so cables never wind up.
- Set the first ring's tilt by value or from where the camera points; the plan
  lists every ring's tilt, and CHECK RINGS shows each ring's framing.
- RESUME after a stop, and RETURN TO START the way the turntable came.
- Camera by digiCamControl (USB) or a watch folder for any camera brand.
- An XMP sidecar per photo and a CSV log per session.

### New -- Photogrammetry
- PLAN A CAPTURE sets the turntable capture up for photogrammetry, with an
  optional backlit pass for clean masks.
- Camera positions for every photo from the turntable angle, tilt and slider.
- Export for RealityCapture / RealityScan, Agisoft Metashape and COLMAP, with
  masks, plus a spin viewer: one HTML page you can share.
- Shot RAW? COLMAP gets the full-size JPEG from each Nikon or Canon RAW file,
  or the photos you developed yourself.
- The COLMAP script also writes point clouds (.ply) for use in a professional
  modelling app, and a README explains each file.
- After an export, the mask preview shows one of the masks for checking.
- HOW IT WORKS explains the tab step by step.

### New -- Motion
- Keys are the stored positions: K1 = P1, K2 = P2 ... set from the rig with
  SET START HERE, SET END HERE and ADD KEY.
- Graph editor with Bezier ease in / out, Smooth or Linear per key; drag keys to
  retime them, with Undo (Ctrl+Z).
- Scrub the playhead and let the rig follow it, then ADD KEY for an in-between
  key.
- Real-time moves played by the units' own smooth motion, timed to the keys;
  PREVIEW MOVE learns each rig's timing, STRETCH spreads a move the gear cannot
  keep up with.
- Timelapse (step and shoot, or one continuous move), planned like an
  intervalometer: a shoot time and an interval in h:mm:ss -- three hours, a
  photo every five minutes -- or a clip length or a number of frames. The keys
  read as times into the shoot, and the photos come on a steady clock from the
  first one.
- Stop motion with a CONTINUE before every frame; PREVIEW MOVE plays the path
  first.

### New -- Panorama and HDRI
- A spherical grid from focal length, sensor, mounting and overlap, for
  rectilinear, full-frame fisheye and circular fisheye lenses.
- A map of the sphere shaded by how many frames see each spot: overlap and
  gaps at a glance.
- Rows: Auto covers what the tilt limits allow, or choose 1 to 5 rows centred
  where the camera points.
- Zenith and nadir shots that respect the tilt limits.
- 3, 5, 7 or 9 bracketed exposures per position, shutter speed only -- stepped
  by the tool or by the camera's own AEB / BKT.
- PTGui (Papywizard) and Hugin projects with every frame in place.

### New -- Focus stacking
- The slider as a macro rail: SET NEAR HERE and SET FAR HERE by hand while
  watching the live view, GO TO NEAR / FAR to check the focus at both ends.
- The step worked out from the lens (magnification, aperture, sensor and
  overlap), typed in millimetres, or set by the number of photos.
- Every step moves the same way, settles and takes a photo; photos numbered
  from near to far, each with the slider position in its XMP sidecar.
- The plan line gives the working aperture, the diffraction blur and the
  sharpest aperture, and lists the photos each aperture needs.
- RESUME A STOPPED STACK carries on after a flat camera battery or STOP, in
  the same folder, from the next photo.

### New -- Help and updates
- Help -> How do I...: short answers for every kind of shoot.
- A tooltip on every button, tick box and field.
- A log file for each day in Documents -> mh_tools -> mh_motion_control_logs
  (Help -> Open Log Folder).
- Help -> Check for Updates, and an optional check once a day at start.

Earlier versions were test builds and were not published.
