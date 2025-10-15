# RuneCollection
*A modular magic system for creative spellcasting*

## Overview

The Rune System allows players to construct spells by combining different types of runes in a structured way. Each spell begins with a **targeting rune** and can be enhanced with **effect runes** and **modifier runes** to create unique magical combinations.

## How to Build a Rune Setup

### Basic Rules

1. **Start with a targeting rune** - Every setup begins with how the spell targets (Self, Touch, Entity, or Projectile)
2. **Add effects** - Attach effect runes to define what the spell does (Area, Explosion, Enchantment, etc.)
3. **Apply modifiers** - Use modifiers to enhance both targeting and effects
4. **Stack creatively** - Effects can have multiple modifiers, and targeting can branch to multiple effects

### Structure Diagram

```
             |-------|              |-------|
             | Modi1 |              | Modi1 |
             |-------|              |-------|
                 ^                      ^
|--------|  |--------|  |--------|  |--------|  |-------|
|  Modi2 |< |Effect1 |< | Target | >|Effect2 | >| Modi2 |
|--------|  |--------|  |--------|  |--------|  |-------|  
                 v                      v
             |-------|              |-------|
             | Modi3 |              | Modi3 |
             |-------|              |-------|                 
```

![Rune System Diagram](8f25ea2b-710e-4923-8396-4813ed31c430.png)

---

## Targeting Runes

*These runes determine how spells are aimed and delivered*

### 🎯 Self
**Effect**: Centered at the caster's location

### 👋 Touch
**Effect**: Centers at a point touched by the caster's hand

**Available Modifiers**:
- **Trigger**: Effect activates when someone else interacts with the touched object/entity
- **Grand Delay**: Delays activation by 1 hour
- **Minor Delay**: Delays activation by 1 minute

### 🎪 Entity
**Effect**: Targets a single creature within range

**Available Modifiers**:
- **Targets**: +1 additional target per modifier
- **Range**: +10ft targeting range per modifier

### 🏹 Projectile
**Effect**: Launches in a direction, travels until hitting something or reaching maximum range

**Available Modifiers**:
- **Count**: +1 additional projectile per modifier
- **Range**: +10ft maximum travel distance per modifier

---

## Effect Runes

*These runes define what the spell actually does*

### 🌊 Area
**Effect**: Creates a magical area around the spell's target point

**Available Modifiers**:
- **Fire**: Area deals `{{< crc >}} d4 + 1` fire damage per turn
- **Range**: +2ft radius per modifier

### 💥 Explosion
**Effect**: Creates a blast that radiates outward from impact point

**Available Modifiers**:
- **Fire**: Adds `{{< crc >}} d6 + 2` fire damage
- **Git Push**: Knocks creatures 10ft away from center
- **Git Pull**: Pulls creatures 10ft toward center  
- **Merge Conflict**: Deals `{{< crc >}} d8` psychic damage
- **Range**: +5ft explosion radius per modifier
- **Intensity**: Increases damage dice by one step (d4→d6→d8→d10→d12)

### 🧠 Enchantment
**Effect**: Applies a magical mental effect to targets
*Base duration: 1 minute | Targets can attempt to break free each turn*

**Sub-Types**:
- **Charm**: Wisdom save or be charmed
- **Fear**: Wisdom save or be frightened  
- **Sleep**: Constitution save or fall unconscious
- **Slow**: Speed halved, only one action per turn

**Available Modifiers**:
- **Saves++**: +1 to save difficulty per modifier
- **Duration**: +20% duration (minimum +1 round) per modifier

### 🏗️ Conjuration
**Effect**: Creates temporary magical constructs or summons

**Available Modifiers**:
- **Wall**: Creates a barrier blocking movement and sight
- **Weapon**: Summons an independent attacking spectral weapon
- **Creature**: Summons a temporary ally
- **Duration**: +1 minute duration per modifier

---

## Example Spells

### 🔥 Classic Fireball

**Rune Setup**: `Projectile` → `Explosion` → `Fire` + `Range`

**How it Works**:
1. **Projectile** launches forward until impact
2. **Explosion** creates a blast at impact point  
3. **Fire** adds burning damage (`{{< crc >}} d6 + 2`)
4. **Range** increases blast radius (+5ft)

### 🔥 Fireball Variations

| Setup | Effect |
|-------|--------|
| `Projectile + Count` → `Explosion` → `Fire + Intensity` | Multiple smaller fireballs |
| `Entity` → `Explosion` → `Fire + Git Push` | Touch-range fireball with knockback |
| `Projectile` → `Area` → `Fire + Range` | Creates lingering fire zone |
| `Self` → `Area` → `Explosion + Fire + Intensity` | Kamikaze blast |

### 🧊 Other Creative Examples

| Setup | Spell Effect |
|-------|-------------|
| `Touch + Trigger` → `Enchantment` → `Fear + Duration` | Cursed object that frightens anyone who touches it |
| `Entity + Targets` → `Conjuration` → `Wall + Duration` | Summon walls around multiple enemies |
| `Projectile + Count` → `Explosion` → `Git Pull + Intensity` | Multiple gravity bombs that pull enemies together |
| `Self` → `Area` → `Fire + Range + Enchantment` → `Slow` | Fire aura that also slows nearby enemies |

---

*The beauty of this system lies in experimentation - try different combinations to discover new magical effects!*