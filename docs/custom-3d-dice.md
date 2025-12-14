# Custom 3D Dice Pack Developer Guide

## JSON Structure Overview

Your dice pack consists of:
- **{PackName}.json** - Main configuration file
- **{PackName}/** - Folder containing all assets (models, textures, icons, sounds)

### [Download Example ZIP for Custom Dice](assets/black-dice-example.zip)

## Core Concepts

### Dice Positions 0-6 (Core Dice Set)

Positions **0-6** are reserved for the standard polyhedral dice:

| Position | Die Type | Required |
|----------|----------|----------|
| 0 | d4 | Yes |
| 1 | d6 | Yes |
| 2 | d8 | Yes |
| 3 | d10 | Yes |
| 4 | d12 | Yes |
| 5 | d20 | Yes |
| 6 | d10x10 (percentile tens) | Yes |

**To override core dice with custom visuals:**
```json
{
  "position": 1,
  "model": "Models/d6_custom.glb",
  "map": ["MyPack/custom_d6_texture.png"],
  "faces": [
    { "normal": [1.0, 0.0, 0.0], "number": 6 },
    ...
  ]
}
```

### Variant Dice (Position 7+)

Add custom dice variants by **omitting position** or using **position >= 7**:

```json
{
  "id": "weather_storm",
  "displayName": "Storm Die",
  "baseType": "d6",
  "position": 7,
  "model": "Models/d6_low.glb",  // Reuse existing model
  "map": ["MyPack/storm_texture.png"],  // Custom texture
  "icon": "icons/storm_icon.png",
  "faces": [
    { "normal": [1.0, 0.0, 0.0], "number": 1, "label": "Thunder" },
    { "normal": [0.0, 1.0, 0.0], "number": 2, "label": "Rain" },
    ...
  ]
}
```

## Face Labels vs Numbers

Each face supports both numeric values and text labels:

```json
{
  "faces": [
    { "normal": [...], "number": 5 },  // Shows "5"
    { "normal": [...], "number": 1, "label": "Critical!" },  // Shows "Critical!"
    { "normal": [...], "label": "Banana" }  // Shows "Banana" (number defaults to 0)
  ]
}
```

**Display Priority:**
- If `label` exists → display label
- If no label → display `number`
- If neither provided → `number` defaults to 0

**Example: Story Dice**
```json
{
  "id": "story_die",
  "displayName": "Story Die",
  "baseType": "d6",
  "faces": [
    { "normal": [1.0, 0.0, 0.0], "label": "🍌 Banana" },
    { "normal": [0.0, 1.0, 0.0], "label": "🦆 Duck" },
    { "normal": [-1.0, 0.0, 0.0], "label": "🌟 Star" },
    { "normal": [0.0, -1.0, 0.0], "label": "🏰 Castle" },
    { "normal": [0.0, 0.0, 1.0], "label": "🐱 Cat" },
    { "normal": [0.0, 0.0, -1.0], "label": "🌈 Rainbow" }
  ]
}
```

## Variant-Only Packs

If your pack **only contains variants** (no core dice set):

```json
{
  "displayName": "Weather Dice Collection",
  "variantOnly": true,
  "dice": [
    {
      "id": "storm",
      "displayName": "Storm Die",
      "baseType": "d6",
      "model": "Models/d6_low.glb",
      "map": ["Weather/storm.png"],
      "faces": [...]
    },
    {
      "id": "sunny",
      "displayName": "Sunny Die",
      "baseType": "d8",
      "model": "Models/d8_low.glb",
      "map": ["Weather/sunny.png"],
      "faces": [...]
    }
  ]
}
```

**Note:** With `"variantOnly": true`, users can only load your pack as **additional dice** on top of another complete dice set.

## Reserved System IDs

**Do not use these IDs for custom dice** (they're hardcoded for specific game systems):

### FATE Dice
- **`dF`** - FATE die (d6 with -1, 0, +1 results)

### Genesys/Star Wars Narrative Dice
- **`nDa`** - Ability die (d8)
- **`nDb`** - Boost die (d6)
- **`nDc`** - Challenge die (d12)
- **`nDd`** - Difficulty die (d8)
- **`nDs`** - Setback die (d6)
- **`nDp`** - Proficiency die (d12)

**If you create custom versions of these dice**, use the same IDs so the system recognizes them:

```json
{
  "id": "dF",  // System will recognize this as FATE dice
  "displayName": "Fate Die (Custom)",
  "baseType": "d6",
  "faces": [
    { "normal": [...], "number": 1 },   // +
    { "normal": [...], "number": 0 },   // blank
    { "normal": [...], "number": -1 }   // -
  ]
}
```

## Display Names

- **Pack-level `displayName`**: Shown in dice pack selection UI
- **Die-level `displayName`**: Shown in tooltips and roll results

```json
{
  "displayName": "Mystical Runes (by YourName)",  // Pack name
  "dice": [
    {
      "position": 1,
      "displayName": "Runic d6",  // Die name (optional, defaults to "d6")
      ...
    },
    {
      "id": "oracle_die",
      "displayName": "Oracle's Vision",  // Important for variant dice
      ...
    }
  ]
}
```

**For d10x10 (percentile):** The UI automatically displays it as "d100" to users.

## Quick Examples

### Full Pack (Reskinned Core + Variants)
```json
{
  "displayName": "Dragon Scales",
  "dice": [
    { "position": 0, "model": "Models/d4_low.glb", "map": ["Dragon/d4.png"], ... },
    { "position": 1, "model": "Models/d6_low.glb", "map": ["Dragon/d6.png"], ... },
    ...
    { "position": 6, "model": "Models/d10_low.glb", "map": ["Dragon/d100.png"], ... },
    { "id": "dragon_breath", "displayName": "Dragon's Breath", "position": 7, ... }
  ]
}
```

### Variant-Only Pack
```json
{
  "displayName": "Elemental Symbols",
  "variantOnly": true,
  "dice": [
    { "id": "fire", "displayName": "Fire", "baseType": "d6", ... },
    { "id": "water", "displayName": "Water", "baseType": "d6", ... },
    { "id": "earth", "displayName": "Earth", "baseType": "d8", ... },
    { "id": "air", "displayName": "Air", "baseType": "d8", ... }
  ]
}
```

### Story Dice with Labels
```json
{
  "displayName": "Adventure Dice",
  "variantOnly": true,
  "dice": [
    {
      "id": "quest_die",
      "displayName": "Quest Die",
      "baseType": "d6",
      "model": "Models/d6_low.glb",
      "map": ["Quest/symbols.png"],
      "faces": [
        { "normal": [1.0, 0.0, 0.0], "label": "Treasure" },
        { "normal": [0.0, 1.0, 0.0], "label": "Monster" },
        { "normal": [-1.0, 0.0, 0.0], "label": "Trap" },
        { "normal": [0.0, -1.0, 0.0], "label": "Ally" },
        { "normal": [0.0, 0.0, 1.0], "label": "Magic" },
        { "normal": [0.0, 0.0, -1.0], "label": "Rest" }
      ]
    }
  ]
}
```

## Tips

1. **Reuse models**: Point to existing models like `"Models/d6_low.glb"` and just change textures
2. **Test with simple packs first**: Start with one variant die before creating a full set
3. **Icon paths**: Provide custom icons for better UI: `"icon": "icons/my_die.png"`
4. **Additive packs work together**: Users can enable multiple variant packs simultaneously
