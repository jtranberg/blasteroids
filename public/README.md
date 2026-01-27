# Blaasteroids 🚀☄️

A fast, minimalist **Phaser 3** arcade game: pilot a space plane, **thrust + rotate**, and **shoot incoming asteroids**.  
Asteroids spawn from the **edges of the screen** and drift inward. Every **10 asteroids destroyed**, the game speeds up.

---

## 🎮 How to Play

### Controls
- **Turn Left / Right:** `A` / `D`
- **Thrust (forward):** `W` or `↑`
- **Shoot:** `Space`
- **Restart:** `R`

### What’s happening on screen
- Your ship starts in the **center**.
- Asteroids **spawn just outside the screen** (left/right/top/bottom edges) and fly inward.
- Bullets fire from your ship in the direction it’s facing.
- If an asteroid touches your ship → **game over**.

---

## ☄️ Where are the asteroids?

Asteroids spawn **off-screen**, then move into the play area.

In code, this happens in `spawnAsteroid()`:

- Left edge: `x = -40`
- Right edge: `x = W + 40`
- Top edge: `y = -40`
- Bottom edge: `y = H + 40`

So you won’t see them until they drift onto the screen (usually within a second).

---

## 📈 Difficulty Scaling

- Each asteroid destroyed: **+10 score**
- Every **10 kills**:
  - **Level increases**
  - Asteroids spawn faster (spawn delay decreases)
  - Asteroids move faster (speed increases)

---

## 🧰 Run Locally

Because this is a single-file Phaser game, you can run it with any simple static server.

### Option A: VS Code Live Server
1. Open the folder in VS Code
2. Right click `index.html`
3. **Open with Live Server**

### Option B: Node (http-server)
```bash
npm i -g http-server
http-server
