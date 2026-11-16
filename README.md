# LOOM — Stories, woven in motion
An original editorial Video.js v10 skin by Laiba Ilyas. HTML custom elements, CSS, and Vite. No backend or accounts required.

## Run
Node.js 22.12+ or 24 LTS.

```
npm ci
npm run dev
npm run build
```

Deploy the generated `dist` folder on Netlify, Vercel or another static host. The build includes the demo film so it does not rely on a third-party video URL.

## Player
The `video-player` / `media-container` subtree in index.html is the skin; all Video.js registrations are in src/main.js; styling is in src/style.css. `@videojs/html` 10.4.0 is pinned by package-lock.json. Copy the player subtree, imports, styles and needed assets into your HTML application. The UI uses real v10 playback, seek, volume, fullscreen and rate components, not v8 or a decorative facade.

Player CSS variables: --media-accent-color, --media-border-radius, --surface, --ink, --line. Set data-finish on .loom-skin to ivory, ink or clay. The layout uses container queries, so controls adapt to embedded player widths, not just the browser viewport. Volume slider hides on narrow players; mute remains available. On mobile devices that disallow programmatic volume, use physical volume controls. Keyboard controls: Tab, Space, M, F, arrow keys; sliders use their native arrow key behavior.

Replace video src and poster in index.html to use your own film. Update the three editorial bookmark times and labels in index.html and main.js, and the timeline marker percentages in CSS to match the new film. Native iOS fullscreen may show system controls rather than a custom skin.

## Submission copy
LOOM turns the video player into a small piece of editorial craft. Inspired by bookbinding and woven cloth, its timeline is a thread and its playhead a shuttle, connecting moments in a story. Warm paper surfaces, cobalt accents, and three considered finishes give it character, while familiar controls, container-responsive layouts, visible keyboard focus, and reduced-motion support keep the experience approachable. Built with Video.js v10.

## Submission checklist
Use the public live demo URL. Include a screenshot of the player. Accept the challenge guidelines personally in Contra and submit there before the deadline. Do not claim the Mux bonus: this demo self-hosts a licensed trailer and has no user-owned Mux asset. Only claim the live-site bonus after integrating the skin into an actual portfolio/project site that qualifies under the rules.

## License
Original code: Apache-2.0, see LICENSE. Third-party film, stills, font and dependencies retain their respective licenses; see NOTICE. This project does not claim ownership of Sintel.
