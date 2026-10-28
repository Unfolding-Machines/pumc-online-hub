# AI Assistant

> **Premium Extra**  
> The AI Assistant is an optional premium extra for PUM Companion. You can unlock it via the in-app store or as a DLC on your preferred platform.

PUM Companion includes powerful AI assistant designed to enhance your solo RPG experience. From generating characters and locations to expanding your narrative notes and visualizing your world, the AI acts as a creative partner that helps you overcome writer's block and adds depth to your stories.

---

## Getting Started with AI

To use the AI features in PUM Companion, you need to provide your own API keys from supported providers. This ensures that you only pay for what you use and have full control over your data.

### Supported Providers (Standard Mode)

For most users, we recommend starting with one of these two providers:

*   **Google Gemini:** Offers a generous free tier and excellent performance.
    *   [Get a Google AI Studio API Key](https://aistudio.google.com/app/apikey)
*   **OpenAI (ChatGPT):** The industry standard for high-quality text generation.
    *   [Get an OpenAI API Key](https://platform.openai.com/api-keys)

*Note: Advanced users can also configure local models via Ollama or other OpenAI-compatible services in the Advanced AI section.*

---

## Activation and Consent

Before you can use AI features, you must activate them in the application settings and provide your consent.

1.  Open **Settings** from the Main Menu or the Game Interface.
2.  Navigate to the **AI Settings** tab.
3.  **Read and Accept the Consent:** PUM Companion prioritizes your privacy. The AI features only send the data necessary to fulfill your requests (like your current plot notes or character descriptions) to the provider you choose.
4.  **Enter your API Key:** Paste your key into the corresponding field (e.g., Gemini API Key).
5.  **Select your Provider:** In the "Text Generation" section, choose your preferred provider and model.

![ai-settings-activation](assets/screenshots/ai-settings-activation.png)

---

## Configuring Your Game AI

Each game can have its own AI personality. You can configure these settings by clicking the **AI Settings (Robot Icon)** in the Game Interface or during the New Game Wizard.

### Preferences

*   **Game System & Universe:** Define the genre, setting, and system of your current game (e.g., "A cyberpunk d20 detective story set in a rainy Neo-Tokyo").
*   **Writing Style Preferences:** Describe your preferred writing style (e.g., "Dark and gritty, focused on internal monologue" or "High-fantasy, epic and descriptive").
*   **Image Style Preferences:** Set the visual aesthetic for generated images (e.g., "Oil painting, moody lighting" or "Digital art, vibrant colors").
*   **Narrator Style / Voice ID:** Shown when a voice provider is set up, to direct how the narrator sounds.

**Tip:** You can use the **Magic Wand** icons next to these fields to have the AI generate a suggestion for you based on your existing game data!

Below the preferences, shortcuts open your **Plot Scope** (your game's premise, setting and priorities) and your **System Rules** (the mechanics the AI should know). Both help the AI a lot.

### Output

These settings balance what you get against what you spend.

*   **Output depth:** How long and detailed AI answers are.
*   **Visual consistency:** Lets the AI take your portraits and covers into account, so texts and images match how your characters and places look.
    *   **Disabled (lower cost):** Portraits and covers are not used.
    *   **Approximate (medium cost):** The AI looks at each portrait and cover once and remembers what it saw, so characters and places keep their features. This is the default.
    *   **Faithful (higher cost):** Generated images also see the portraits and covers of who and what is in the scene, so the same character looks like the same person. This adds a small cost to every image. It needs an image model that accepts reference images (most OpenRouter image models, Google Gemini image models, OpenAI GPT Image, or ComfyUI with a [Reference Workflow](ai-providers.md#6-comfyui-advanced)). With other image models the option is unavailable and images are drawn from descriptions.
*   **Generate images in entities / plot nodes:** Whether the AI also creates images when it creates characters, locations, documents, the gamemaster, or plot nodes.

### Oracles & Creativity

*   **AI Oracle Leverage:** How much the AI relies on PUM's oracles for its ideas: *Disabled* (AI only), *Simple* (the best single oracle), or *Advanced* (multiple oracles).
*   **Creativity bias:** Lower leans towards logic and following instructions, higher towards unpredictable and creative ideas.
*   **Show AI oracle rolls:** Displays the oracle rolls the AI makes in the cinematic overlay.

---

## AI Feature Overview

PUM Companion uses specialized "AI Chains" to handle different tasks:

### ✍️ Writing Assistant
Found in most text editors within the app, the Writing Assistant can:

*   **Repair:** Spell-check and fix grammar issues in your writing.
*   **Enhance:** Improve the style and flow of your text.
*   **Elaborate:** Write and expand brief notes into detailed descriptions.
*   **Condense:** Summarize long passages into concise overviews.
*   **Instruct:** Follow specific commands to modify your text (e.g., "Make this more suspenseful").

### 👤 Entity Generation
When creating a new Character, Location, or Compendium, you can provide just a brief concept and let the AI fill in the details. It will generate a description, personality traits, and even a visual appearance that fits your world.

### 🎭 Plot Node Generation
Enhance your Plot Unfolding Machine with World Building and Obstacles for your story. The AI can suggest new plot nodes based on your game's genre and current narrative, helping to keep the story dynamic and engaging.

### 🎲 Build Narrative
Interpret the results of Oracles, Random Tables, and Dice Rolls within the context of your story. The AI helps you weave these random elements into a cohesive narrative beat, making sense of the "chaos" of the dice.

### 💬 Answer Directly
Ask the AI a direct question about your world or current situation. It uses the underlying Oracle systems to determine the outcome and then provides a narrative answer that fits your story's context.

### 🗣️ Discuss
A dedicated AI Chat feature for brainstorming. You can talk to the AI to bounce ideas, ask for suggestions on world-building, or get creative input on where your story could go next.

### 📝 Draft Game
Found in the New Game Wizard, this feature allows you to create a complete game proposal in seconds. The AI will fill in your plot scope, suggest key characters and locations, and even draft initial plot nodes to get your adventure started immediately.

### 🖼️ Image Generation
Either indirectly through creating Entities and Plot Nodes, or directly within a character or a location, you can generate images that match your specified style and description. The AI will create visuals that bring your world to life. With **Visual consistency** on, your existing portraits and covers keep characters and places looking like themselves across new images.

---

## Privacy and Data
PUM Companion is designed with a "Privacy First" approach. Your API keys are stored locally on your device. Data is only sent to the AI provider when you explicitly click an AI-related button. No story data is ever sold or used for training by Unfolding Machines.
