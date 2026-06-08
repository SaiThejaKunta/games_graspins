# 🎮 Graspins Games Portal

A premium, curated collection of serverless, self-contained word puzzles, party games, local two-player board games, and utility tools. All games run entirely inside the web browser with zero backend requirements or framework overhead.

---

## 🕹️ Games & Tools Catalog

### 🧠 Semantix (Solo)
* **Goal**: Guess the secret target word based on its semantic meaning.
* **Features**:
  * Calculates semantic similarity scores (using local cosine similarity vectors).
  * Auto-sorts history by proximity and tracks daily stats.
  * **Dynamic Knowledge Graph**: A custom HTML5 Canvas force-directed graph physics simulation showcasing how your guesses bridge together semantically towards the target word.
  * **Smart Selector**: Dynamically limits target words to the top 700 everyday daily-use terms and prevents repetition using client-side history tracking.

### 🔴 Connect Four (2 Player)
* **Goal**: Drop chips into a 6x7 grid to align four of your matching colors (Red vs. Yellow).
* **Features**:
  * Physics-based gravity dropping animation with a terminal bounce.
  * Interactive column selectors and neon hovering previews.
  * Web Audio API synthesized chip drop sounds and celebratory victory chime.
  * Full scoreboard tracking and win highlights.

### ❌ Tic-Tac-Toe / x0x (2 Player)
* **Goal**: Align three marks (❌ or ⭕) horizontally, vertically, or diagonally.
* **Features**:
  * Elegant glowing neon theme.
  * Animated SVG path drawings when placing marks.
  * Victory strike overlay drawing a line directly across matching markers.
  * Custom player name configurations and scoreboards.

### 🕵️ Codenames (Co-op / Party)
* **Goal**: Spymasters give one-word clues pointing to multiple words on a shared board. Teams collaborate to discover all of their agents before the assassin is revealed.

### 🕶️ Spy — Who is the Spy? (Party)
* **Goal**: A social deduction game where players ask questions to deduce who doesn't know the secret location (the spy). The spy must blend in and guess the location.

### ☝️ Just One (Co-op)
* **Goal**: A cooperative word game where players write single-word clues to help a teammate guess a secret word. Duplicated clues are discarded, rewarding creativity.

### 🪙 Coin Toss (Tool)
* **Goal**: Flip a coin to settle disputes or decide game order.
* **Features**:
  * Full 3D spinning physics coin animation rotating on multiple axes.
  * Switchable coin styles: Gold Bitcoin, Silver Ethereum, or Bronze Graspins.
  * Synthesized metallic ringing and table bounce audio.
  * Tracks tails/heads statistics and consecutive streaks.

### 🎛️ Mixer (Tool)
* **Goal**: A player management tool to randomize teams, generate group pairings, and distribute players for activities.

---

## 🛠️ The Tech Stack (Simplicity by Design)

This portal showcases how simply and cleanly fully-featured web games can be built without heavy framework chains. 

* **Vanilla Foundation**: Core structure is built on raw **HTML5** and **ES6 JavaScript**. This guarantees instant loading, zero compilation delays, and offline-readiness.
* **CSS3 Preserved-3D Physics**: Advanced styling is done using Vanilla CSS. Animations like the Coin Toss 3D flip and the Connect Four drop are executed using CSS Keyframes and `transform-style: preserve-3d` for hardware-accelerated 3D graphics in the browser.
* **Serverless Local Storage**: All scoreboards, custom player names, played word history, daily streak stats, and active game progress are persisted client-side via the browser's `localStorage` API. No login, databases, or accounts needed.
* **Web Audio API Sound Synthesis**: Instead of downloading heavy audio assets (like MP3 or WAV files), all game noises (chips dropping, coin ringing, wins, draws, clicks) are dynamically synthesized on-the-fly using oscillators, custom envelopes, and lowpass biquad filters.
