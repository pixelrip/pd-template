# Playdate Development Guidelines

This document outlines helpful tips for developing for the Playdate with the Playdate SDK.

## General Tips
- Always review the [Playdate SDK](https://sdk.play.date/2.7.6/Inside%20Playdate.html#_animation) docs to understand best practices with the SDK
- Playdate games run at 30 frames per second (fps)
- Project must contain a `main.lua` file within a `source/` directory. For organization, use `images/` and `sounds/` subfolders within `source/` for assets.

## Object-Oriented Programming (OOP)
- Use `CoreLibs/object` to construct objects instead of Lua's more common metatable approach
- Use `playdate.graphics.sprite` as entity constructor for most visal entities in the game


## Hardware Constraints
- Screen resolution is 400 × 240 pixels, at 173 pixels per inch
- Screen has a 3mm black bezel allowing for graphics all the way to the edge.
- Physically center an onscreen element on the actual device at 228 on the x axis

## Sprites
- Pre-transform graphics in an editor app. Rotating or scaling images is CPU-intensive and Playdate has no GPU.
- [Image tables](https://sdk.play.date/#C-graphics.imagetable) can be used to conveniently access multiple transformations of the same image


## On Screen Text
- Dialog text should be at least 12 pixels tall, preferably 14 pixels tall. 
- HUD text (score, health, level name) can be slightly smaller, down to 10 pixels tall


