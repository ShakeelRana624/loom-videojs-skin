# LOOM validation

Build: Vite production build succeeds with @videojs/html 10.4.0.

Browser checks in Chromium:
- Real local trailer metadata loads: duration 52 seconds.
- Play/pause: confirmed time advances and state changes.
- Seek: ArrowRight and Home update the timeline/time.
- Mute: control switches to Unmute.
- Volume: ArrowLeft changes value from 100 to 95.
- Playback speed: cycles from 1 to 1.25.
- Chapter jump: second bookmark seeks to 18 seconds and plays.
- Keyboard guide: opens as a modal dialog and Escape closes it.
- Responsive: visually inspected at 375px and 320px iframe widths; essentials remain visible, without horizontal clipping.
- Visible focus styling is implemented, including sliders and theme controls.
- Reduced motion and forced-colors styles are included.

Verification limits:
- The remote test browser rejected native fullscreen with `TypeError: not granted`. The button is the official Video.js v10 fullscreen component. Please verify enter/exit fullscreen in a normal desktop browser before submitting.
- No physical iOS/Android device or screen-reader run was available. Native fullscreen on iOS may use system controls.
- Error, buffering and ended states are implemented; not all were deliberately induced in browser QA.
- Theme controls and reduced motion were reviewed in implementation; full assistive-technology testing is still recommended.
