+++
title = "Targeting Runes"
+++

# Targeting Runes

**Summary**

Targeting runes determine who or what a rune setup affects. They set the origin point, the number of targets, and interact directly with range and count modifiers.

How targeting works

- The targeting rune resolves first and establishes the point(s) or creature(s) affected.
- The effect rune then applies its effect to those targets.
- Modifiers on either rune may alter range, number of targets, or other targeting properties.

## Self

**Self** — Origin is the caster.

Mechanics:
- The caster occupies the origin point; effects are centered on the caster.

Example

Casting an Area rune with Targeting:Self places the area around the caster.

## Touch

**Touch** — Requires physical contact with the target.

Mechanics:
- The caster must touch the target with a free hand.
- The spell triggers on touch; use Trigger modifiers to delay activation.

Modifiers

- Trigger: The rune is set on the touched object and activates when the trigger condition is met.
- Grand delay / Minor delay: Introduce long or short delays before activation (campaign-specific timing).

Example

A Trap rune applied to a door that detonates when opened.

## Entity

**Entity** — Targets a single creature or object within range.

Mechanics:
- Choose a creature or object within the rune's range.
- Apply effects to the selected entity (or multiple if Targets modifier is present).

Modifiers

- Targets: Increase the number of targets by 1 per step.
- Range: Increase targeting range by 10 ft per step.

Example

Entity → Enchantment:Charm to be placed on one guard; with Targets+1 it may affect two guards.

## Projectile

**Projectile** — Creates a moving object that travels until it hits or reaches its maximum range.

Mechanics:
- The caster chooses a direction and target point.
- The projectile travels and resolves on impact or at max range.

Modifiers

- Count: Launch multiple projectiles.
- Range: Increase projectile maximum travel distance by 10 ft per step.

Example

Projectile → Explosion produces flaming orbs that detonate on impact.

Notes

- Targeting interacts heavily with battlefield geometry; always determine line of effect and cover before resolving.
