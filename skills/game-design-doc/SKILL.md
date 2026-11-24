---
name: game-design-doc
description: Turn a game idea into a one-page design doc and a minimum playable build checklist for Roblox (Luau) or a small single-player browser game. Use before writing any game code or when a game idea needs scoping.
---

# One-page game design doc

## 1. The doc (before any code)
Fill one page. Ask only for missing essentials (genre, platform).
- One-line concept, genre, platform (Roblox / browser / Godot)
- Core loop: 3 actions that repeat within 30 seconds (e.g. explore → collect → upgrade)
- Win/lose conditions, length of one round
- Controls: keyboard / touch / gamepad
- Scope: in the first build / later / never
- 2–3 reference games and one thing to take from each

## 2. Tech
- Roblox: Luau. Split server (ServerScriptService) and client (StarterPlayerScripts), talk only via RemoteEvents, validate client input on the server.
- Browser: Phaser 3 or plain Canvas, one folder + Vite. Suggest Godot if physics/scene management gets big.

## 3. Minimum playable checklist
1. The player moves
2. One core loop runs
3. Win/lose is detected
4. You can restart
Stop here, play it, confirm it's fun — only then add art, sound and features.

## 4. QA
Browser: run it in Playwright — zero console errors, ~60fps, touch works on mobile. Roblox: check server/client output in Play mode. Report: works / doesn't / next.
