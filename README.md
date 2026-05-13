/* E-ERA TECH shared design system */
:root {
  --bg: #05070d;
  --bg-soft: #090d18;
  --panel: rgba(255, 255, 255, 0.075);
  --panel-strong: rgba(255, 255, 255, 0.12);
  --text: #f5f7fb;
  --muted: #aeb8c8;
  --cyan: #24f3ff;
  --pink: #ff4fd8;
  --lime: #a8ff60;
  --line: rgba(255, 255, 255, 0.14);
  --shadow: 0 24px 70px rgba(0, 0, 0, 0.42);
  --radius: 8px;
  --max: 1180px;
  --font: "Inter", "Segoe UI", Arial, sans-serif;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: var(--font);
  background:
    radial-gradient(circle at 15% 12%, rgba(36, 243, 255, 0.14), transparent 28rem),
    radial-gradient(circle at 82% 18%, rgba(255, 79, 216, 0.12), transparent 26rem),
    linear-gradient(140deg, #03040a 0%, #07101d 46%, #05070d 100%);
  color: var(--text);
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  background-image:
    linear-gradient(rgba(255, 255, 255, 0.035) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.035) 1px, transparent 1px);
  background-size: 54px 54px;
  mask-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.75), transparent 78%);
  z-index: -1;
}

a {
  color: inherit;
  text-decoration: none;
}

img {
  max-width: 100%;
  display: block;
}

.container {
  width: min(var(--max), calc(100% - 32px));
  margin: 0 auto;
}

.site-loader {
  position: fixed;
  inset: 0;
  z-index: 1000;
  display: grid;
  place-items: center;
  background: #03040a;
  transition: opacity 0.45s ease, visibility 0.45s ease;
}

.site-loader.hidden {
  opacity: 0;
  visibility: hidden;
}

.loader-mark {
  width: 78px;
  height: 78px;
  border: 1px solid var(--line);
  border-top-color: var(--cyan);
  border-right-color: var(--pink);
  border-radius: 50%;
  animation: spin 1s linear infinite;
  box-shadow: 0 0 34px rgba(36, 243, 255, 0.25);
}

.progress {
  position: fixed;
  top: 0;
  left: 0;
  height: 3px;
  width: 0;
  z-index: 999;
  background: linear-gradient(90deg, var(--cyan), var(--pink), var(--lime));
