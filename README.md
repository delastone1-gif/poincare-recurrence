# Poincaré Recurrence Theorem — Interactive Exploration

**An interactive educational website exploring the Poincaré Recurrence Theorem, statistical mechanics, and the nature of entropy.**

🌐 **Bilingual**: Full French / English support with live toggle.

![License](https://img.shields.io/badge/license-MIT-green)
![HTML5](https://img.shields.io/badge/HTML5-single%20file-orange)
![No Dependencies](https://img.shields.io/badge/dependencies-none-blue)

---

## What is this?

A single-page interactive website that explains one of the most fascinating results in physics: in a perfectly isolated system, every state will eventually recur — but the timescales involved are so absurdly large that "eventually" loses all practical meaning.

The site combines a live particle simulation with educational content covering the theorem, entropy, the historical Zermelo-Boltzmann debate, and the divergence between classical thermodynamics and statistical mechanics.

## Features

### Particle Simulation
- Particles start in an ordered grid (initial state) and receive random velocities on launch
- **Confinement phase**: particles bounce inside a circular boundary
- **Release phase**: open the box and watch entropy increase as particles disperse
- **Recall**: bring particles back into the circle to observe that order is not restored
- Real-time statistics: entropy, distance to initial state, proximity percentage, best return
- Ghost positions show where each particle started, with numbered labels (up to 30 particles)
- Flash effect when a particle passes near its initial position
- Proximity history graph tracking similarity over time

### Educational Content (7 sections)
1. **The Theorem** — Poincaré's 1890 result and its conditions
2. **Inconceivable Timescales** — From 10 particles to a vehicle with 10²⁸ atoms
3. **The Initial State Question** — Recurrence restores, it does not create
4. **Entropy: Statistical, Not Absolute** — The second law as a probability statement
5. **Two Views of Entropy** — Side-by-side comparison of classical thermodynamics vs. statistical mechanics
6. **Where Theories Diverge** — Interactive entropy timeline showing agreement and divergence across timescales
7. **The Zermelo-Boltzmann Debate** — The 1896 historical clash and its modern resolution

### Design
- Dark theme with accent colors (green/orange/purple/blue)
- Typography: Cormorant Garamond (headings), JetBrains Mono (data), DM Sans (body)
- Responsive layout
- Zero dependencies — single HTML file, pure vanilla JS + Canvas API
- Google Fonts loaded via CDN (only external resource)

## Quick Start

No build step. No dependencies. Just open the file.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/poincare-recurrence.git

# Open in browser
open index.html
```

Or deploy to any static hosting (GitHub Pages, Netlify, Vercel, etc.).

### GitHub Pages

1. Go to your repo **Settings** > **Pages**
2. Set source to `main` branch, root `/`
3. Your site will be live at `https://YOUR_USERNAME.github.io/poincare-recurrence/`

## How to Use the Simulation

| Step | Action | What happens |
|------|--------|-------------|
| 1 | Adjust the **particle slider** (5-80) | Sets the number of particles in the grid |
| 2 | Click **Start** | Particles receive random velocities, confined in the circle |
| 3 | Observe the **proximity bar** and **graph** | Watch how often particles return near their starting positions |
| 4 | Click **Open the box** | Circle wall removed — particles disperse into the full space |
| 5 | Watch **entropy** and **distance** increase | The second law in action |
| 6 | Click **Recall to circle** | Particles are pushed back in — but NOT to their original positions |
| 7 | Toggle **FR / EN** | Switch language in real time |

**Try this**: run with 5 particles confined in the circle. You'll see frequent green flashes (individual particles returning to their origin). Then try 80 particles — the flashes become extremely rare, and the proximity stays permanently low. That's the theorem in action.

## Tech Stack

- **HTML5** — Single file, no framework
- **Canvas API** — Particle simulation, proximity graph, entropy timeline
- **Vanilla JavaScript** — Physics engine, collision detection, i18n system
- **CSS3** — Responsive layout, custom properties, animations
- **Google Fonts** — Cormorant Garamond, JetBrains Mono, DM Sans

## Physics Notes

The simulation uses elastic collisions (conserving kinetic energy and momentum) in a 2D box, which satisfies the conditions for Poincaré recurrence: isolated system, finite phase space, energy-conserving dynamics. The recurrence time scales exponentially with the number of particles, which is why even going from 5 to 30 particles makes a return event essentially unobservable in a browser session.

The entropy is computed via a spatial grid binning method (Shannon entropy of the particle distribution across cells), normalized to [0, 1]. The distance metric is the average Euclidean displacement from initial positions, normalized by the initial zone diameter.

## License

MIT License. See [LICENSE](LICENSE).

## Credits

Built with Claude (Anthropic) as an exploration of physics education through interactive visualization.

Inspired by the work of Henri Poincaré (1890), Ludwig Boltzmann, and Ernst Zermelo.
