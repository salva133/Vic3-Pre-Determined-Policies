# Pre-Determined Policies

**A game-rule mod for Victoria 3** that lets you decide, before the campaign begins, which ideological path every AI country will follow — turning the political map into something you can plan around.

## Overview

Victoria 3 already tracks when a country commits to a radical ideology: the game plants a hidden `chose_*` marker on the interest group that has picked its path (the Trade Unions turning communist, the Armed Forces turning fascist, and so on). Normally these markers appear organically, mid-campaign, and you never know in advance where the world is heading.

This mod adds a single game rule — **Pre-Determined Policies** — that seeds those same markers on every AI country from the very first day. Pick one ideology in the lobby and the whole AI world is nudged down that road, so you start the game already knowing who your natural friends and enemies will be.

## The game rule

Set it in the **Game Rules** panel when you create a game. One option is active at a time.

| Option | What it does |
| --- | --- |
| **Vanilla** *(default)* | Nothing is prescribed. Interest groups choose their own path exactly as in the base game. |
| **Vanguardism** | Every AI country's **Trade Unions** are locked onto the Vanguardist path. |
| **Communism** | Every AI country's **Trade Unions** are locked onto the Communist path. |
| **Anarchism** | Every AI country's **Trade Unions** are locked onto the Anarchist path. |
| **Fascism** | Every AI country's **Armed Forces** are locked onto the Fascist path. |
| **Ethno-Nationalism** | Every AI country's **Armed Forces** are locked onto the Ethno-Nationalist path. |
| **Conservatism** | Every AI country's **Armed Forces** are locked onto the Conservative path. |

Only **non-player** countries are affected — your own nation always chooses its own path. In multiplayer every human player is left free.

## How it works

The chosen marker is applied once, from the vanilla `on_game_started_after_lobby` hook, to every non-player country. Each `chose_*` variable is interest-group scoped in the base game, so the mod seats it on the interest group vanilla itself associates with that path:

- **Left-wing paths** (Vanguardism, Communism, Anarchism) → the **Trade Unions**.
- **Right-wing paths** (Fascism, Ethno-Nationalism, Conservatism) → the **Armed Forces**.

Both interest groups exist in practically every country, so the rule reaches nearly the whole world; any country that happens to lack the interest group is simply skipped. Marking an interest group suppresses its neutral leaders and keeps its matching political movements from disbanding — the same levers vanilla uses when a country picks a path on its own — so the affected nations drift toward the prescribed ideology over the course of the campaign rather than flipping overnight.

## Compatibility

- Adds one game rule, one on-action and one scripted effect; adds no events and overrides no vanilla files.
- The default **Vanilla** option changes nothing, so the mod is inert until you deliberately switch it on.
- Compatible with any mod that does not remove the vanilla `chose_*` ideology-path mechanic.
- Multiplayer-synchronized and deterministic.

## Note on which interest group

The left/right split above is a design choice, not a hard vanilla rule: the base game seats the right-wing markers on whichever government interest group already leans that way, which does not exist yet at game start. If you would rather spread the right-wing paths across distinct power bases (Fascism on the Armed Forces, Ethno-Nationalism on the Petty Bourgeoisie, Conservatism on the Landowners), it is a one-line change per option in `common/scripted_effects/pdp_scripted_effects.txt`.
