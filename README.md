* {
  box-sizing: border-box;
}

:root {
  --bg: #091521;
  --bg-soft: #102235;
  --card: rgba(14, 31, 45, 0.88);
  --panel: rgba(17, 38, 56, 0.9);
  --accent: #44d0d2;
  --accent-strong: #21b5dc;
  --accent-soft: rgba(68, 208, 210, 0.15);
  --text: #edf6ff;
  --muted: #9ec0d7;
  --border: rgba(158, 192, 215, 0.18);
  --shadow: 0 20px 40px rgba(6, 16, 25, 0.48);
}

html, body, #root {
  margin: 0;
  min-height: 100%;
  min-width: 100%;
  font-family: 'Inter', sans-serif;
  background:
    radial-gradient(circle at top, rgba(52, 112, 160, 0.2), transparent 35%),
    linear-gradient(160deg, #06131d 0%, #0e1c2c 32%, #08151f 100%);
  color: var(--text);
}

body {
  min-height: 100vh;
}

button,
input {
  font: inherit;
}

.app-shell {
  width: min(1200px, calc(100% - 32px));
  margin: 32px auto;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.topbar {
  display: flex;
  justify-content: space-between;
  align-items: end;
  gap: 16px;
}

.eyebrow,
.panel-label {
  margin: 0;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 11px;
  color: var(--accent);
  font-weight: 700;
}

h1, h2, h3, p {
  margin: 0;
}

h1 {
  font-size: clamp(2.1rem, 4vw, 3.5rem);
  margin-top: 10px;
}

.topbar__badge {
  padding: 10px 14px;
  border-radius: 999px;
  background: rgba(68, 208, 210, 0.12);
  border: 1px solid var(--border);
  color: var(--accent);
  font-weight: 700;
}

.content-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.6fr) minmax(280px, 0.8fr);
  gap: 24px;
}

.card {
  background: rgba(10, 23, 33, 0.8);
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  backdrop-filter: blur(10px);
  border-radius: 24px;
}

.map-panel {
  padding: 20px 20px 16px;
}

.map-toolbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  margin-bottom: 16px;
}

.map-toolbar h2 {
  margin-top: 8px;
  font-size: clamp(1.3rem, 2vw, 2rem);
}

.map-toolbar input {
  width: min(220px, 100%);
  border-radius: 12px;
  border: 1px solid var(--border);
  background: rgba(255, 255, 255, 0.02);
  color: var(--text);
  padding: 12px 14px;
  outline: none;
}

.map-toolbar input::placeholder {
  color: var(--muted);
}

.map-container {
  border-radius: 18px;
  background: linear-gradient(180deg, rgba(11, 27, 39, 0.9), rgba(13, 21, 31, 0.8));
  border: 1px solid rgba(158, 192, 215, 0.12);
  padding: 10px;
}

.iraq-map {
  width: 100%;
  height: auto;
  display: block;
}

.iraq-outline {
  fill: rgba(61, 92, 121, 0.18);
  stroke: rgba(90, 199, 214, 0.95);
  stroke-width: 4;
  stroke-linejoin: round;
}

.province-group {
  cursor: pointer;
}

.province {
  fill: rgba(52, 146, 175, 0.42);
  stroke: rgba(148, 226, 255, 0.8);
  stroke-width: 2;
  transition: all 0.18s ease;
}

.province:hover,
.province.selected {
  fill: rgba(68, 208, 210, 0.7);
  stroke: #92eff3;
  stroke-width: 3;
  filter: drop-shadow(0 0 10px rgba(68, 208, 210, 0.25));
}

.province-label {
  fill: #f4fbff;
  font-size: 10px;
  font-weight: 700;
  text-anchor: middle;
  pointer-events: none;
  letter-spacing: 0.06em;
}

.sidebar {
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.sidebar__header h3 {
  font-size: 2rem;
  margin-top: 8px;
}

.info-card {
  background: rgba(68, 208, 210, 0.06);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 14px;
  display: grid;
  gap: 12px;
}

.info-card__row {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  color: var(--muted);
}

.info-card__row strong {
  color: var(--text);
  font-weight: 700;
}

.description {
  color: var(--muted);
  line-height: 1.65;
}

.mini-stats {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 12px;
}

.mini-stats div {
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 12px 14px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.mini-stats span {
  color: var(--muted);
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.list-panel {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 12px;
  padding: 18px;
}

.province-item {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 4px;
  padding: 14px 16px;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: rgba(255, 255, 255, 0.02);
  color: var(--text);
  text-align: left;
  transition: all 0.18s ease;
}

.province-item span {
  font-weight: 700;
}

.province-item small {
  color: var(--muted);
}

.province-item:hover,
.province-item.active {
  background: rgba(68, 208, 210, 0.1);
  border-color: rgba(68, 208, 210, 0.35);
  transform: translateY(-1px);
}

.empty-state {
  color: var(--muted);
  padding: 12px 0;
}

@media (max-width: 860px) {
  .content-grid {
    grid-template-columns: 1fr;
  }

  .map-toolbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .map-toolbar input {
    width: 100%;
  }
}

@media (max-width: 560px) {
  .app-shell {
    width: min(100% - 18px, 1200px);
    margin: 18px auto 28px;
  }

  .card,
  .map-panel,
  .sidebar,
  .list-panel {
    border-radius: 18px;
  }

  .sidebar__header h3 {
    font-size: 1.5rem;
  }
}
