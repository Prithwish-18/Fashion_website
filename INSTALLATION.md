# Installation & Local Development

Requirements
- Any modern browser (Chrome, Firefox, Edge, Safari)
- Optional: Node.js + npm if you want to run a local static server or add build tools

Recommended local server options
- live-server (simple)
  - npm i -g live-server
  - live-server
- serve (Node)
  - npm i -g serve
  - serve . -p 5000

Steps to run locally
1. Clone the repo:
   git clone https://github.com/Prithwish-18/Fashion_website.git
   cd Fashion_website

2. Place required media
   - Add your hero video: /assets/videos/pin_man_model.mp4
   - Add your background music (optional): /assets/audio/your-fashion-track.mp3
   - Or update the HTML file paths to suit where you keep your assets.

3. Start a local server
   - live-server
   - Or open the HTML file directly in the browser (double-click the HTML file), though cross-origin requests for some modules may be blocked without a server.

4. View in browser
   - http://127.0.0.1:8080 (or the port live-server uses)
   - Open `grid_project_2.html` or `grid_project_2_Version2.html`

Development tips
- Use DevTools to throttle CPU / Network to test responsiveness and fluid canvas performance
- If modifying CSS, keep a small number of vendor prefixes and avoid forcing layout thrashing (use transform instead of top/left)
- Provide fallbacks for large video backgrounds (poster frames)

Optional: Add simple npm scripts
You can add a package.json and scripts like:
{
  "scripts": {
    "start": "live-server --open=grid_project_2.html",
    "serve": "serve ."
  }
}
