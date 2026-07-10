# PUM Quick Rules: Core Loop

Welcome to the **Plot Unfolding Machine (PUM)** quick-start gameplay guide! This section provides a free, streamlined version of the core PUM rules. It is designed to help new players—especially those using **PUM Lite**—understand how to play a solo tabletop roleplaying game (RPG) using the built-in PUM mechanics.

If you enjoy this system and want to master the full rules, including advanced tables, emotional scene deviations, deep gameplay advice, and custom tracks, please support the creator by purchasing the full PDF:

<div style="text-align: center; margin: 1.5em 0;">
  <a href="https://jeansenvaars.itch.io/plot-unfolding-machine" class="md-button md-button--primary" style="font-weight: bold; font-size: 1.1em; padding: 0.6em 1.5em; border-radius: 8px;">
    🎲 Get the Official PUM PDF on Itch.io ($6)
  </a>
</div>

---

## What is a Solo RPG?

In a traditional tabletop RPG (like Dungeons & Dragons or Pathfinder), you have **Players** who control their characters, and a **Game Master (GM)** who controls the world, plays the NPCs, and decides what happens next.

In a **Solo RPG**, you play alone. You are both the Player and the Game Master:
- You control your protagonists and decide what they attempt to do.
- You use **PUM** (the app and its rules) as your virtual Game Master to introduce unexpected twists, answer questions about the world, and keep the story moving forward.

---

## The Core Gameplay Loop

Playing with PUM follows a flexible, organic cycle that lets you write freely while introducing structured twists when they matter most. 

The **Oracles** are always available at any time to answer questions and resolve uncertainty, whether you are playing freely or interpreting a major plot twist:

``` mermaid
graph TD
    A[1. Play the story and journal freely] --> B{Is it time for something relevant?}
    B -- No --> A
    B -- Yes --> C{Do you have an idea?}
    C -- No / Clueless --> D[Random prompt]
    C -- Yes --> E[Modify proposal]
    D --> F[3. Roll the Prompt and Interpret the Situation]
    E --> F
    F --> G{Was the Beat relevant after playing it?}
    G -- No --> A
    G -- Yes --> H[4. Advance the Plot Track]
    H --> I[5. Check for Plot Track section jump or completion]
    I --> A
    
    A -.->|Have a question?| O[Ask the Oracles] -->|Interpret Answer| A
    F -.->|Have a question?| O2[Ask the Oracles] -->|Interpret Answer| F
```

### 1. Play the story and journal freely
Start writing your story in the log area. Set the scene, describe what your characters are doing, and write their actions or dialogue freely. 

*   **Have a question?** At any time, if you have a question about the world or the outcome of an action, frame the question in your mind, pick a suitable oracle to answer it, and interpret the answer to keep writing. PUM never forces mechanics down your throat.

### 2. Is it time for something relevant?
As you write, ask yourself: *Is it time for a major scene, a plot twist, or a turning point in the story?* 
*   **If No:** Just keep journaling and playing freely.
*   **If Yes:** Trigger a **Plot Beat** depending on your current inspiration:
    *   **If you are clueless:** Tap **Random prompt** to let PUM surprise you with a new scene hook or situation.
    *   **If you already have an idea:** Tap **Modify proposal** to propose your scene idea and let PUM add a random twist or complication to it.

### 3. Roll the Prompt and Interpret the Situation
Roll the chosen Plot Beat and interpret the situation. Write down how your characters react to the prompt or the twist, and explore the drama.
*   **Need details?** Just like in free play, you can ask the **Oracles** to flesh out the details of the prompt (e.g., *"Is anyone else here?"*, *"What is their mood?"*).

### 4. Was the Beat relevant after playing it?
Once the scene wraps up, evaluate how it went:
*   **If No:** If the scene turned out to be a minor detour, a false alarm, or didn't significantly impact your main goals, simply go back to Step 1 and move on with your story.
*   **If Yes:** If the scene was an important milestone, a confirmed plot development, or a major turning point, **advance the Plot Track** by clicking the active box at the top of the screen.

### 5. Check for Plot Track section jump or completion
When you advance the track, check if you have jumped to a new section of your story (e.g., moving from *Exposition* to *Confrontation*) or if you have reached the final box. If the track is complete, resolve your story's main conflict and celebrate your finished game! Otherwise, return to Step 1 and repeat.

---

Next: [Plot Beats (Prompts & Proposals)](rules-plot-beats.md)
