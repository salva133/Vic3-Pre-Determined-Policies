# Pre-Determined Policies

**A game-rule mod for Victoria 3** that decides, before the campaign even begins, which way every AI country will lean — so the political map is something you can plan around instead of something you discover the hard way.

## The idea

Victoria 3 quietly keeps track of when a nation commits to a radical ideology. The moment a country picks its path, the game plants a hidden marker on the interest group that carried it there — the Trade Unions turning communist, the Armed Forces turning fascist, and so on. Normally those markers appear on their own, deep into a campaign, and you never see them coming.

This mod hands you the pen. Add a single game rule in the lobby, choose one ideology, and every AI nation is seeded with that same marker from day one. Pick **Communism** and the workers' movements of the world are already yours to court or crush; pick **Fascism** and you know exactly where the storm is coming from. Either way, you start the game knowing who your friends and your enemies are going to be.

## Using it

Open the **Game Rules** panel when you set up a game and pick one option:

| Option | Effect |
| --- | --- |
| **Vanilla** *(default)* | Nothing is prescribed. Every country finds its own way, exactly as in the base game. |
| **Vanguardism** | Every AI country's **Trade Unions** commit to the Vanguardist path. |
| **Communism** | Every AI country's **Trade Unions** commit to the Communist path. |
| **Anarchism** | Every AI country's **Trade Unions** commit to the Anarchist path. |
| **Fascism** | Every AI country's **Armed Forces** commit to the Fascist path. |
| **Ethno-Nationalism** | Every AI country's **Armed Forces** commit to the Ethno-Nationalist path. |
| **Conservatism** | Every AI country's **Armed Forces** commit to the Conservative path. |

Your own nation is never touched — you always choose your own path. In multiplayer, every human player is left free.

## How it works

The chosen marker is applied once, right after the lobby closes, to every non-player country. Because the base game keeps these `chose_*` markers on interest groups rather than on countries, the mod seats each one where vanilla would: the left-wing paths on the **Trade Unions**, the right-wing paths on the **Armed Forces** — the two interest groups that exist in almost every nation. Any country that somehow lacks the group is simply skipped.

A marked interest group stops producing neutral leaders and holds its matching political movements together — the very levers the base game pulls when a country turns on its own. So the world drifts toward the path you chose over the years of a campaign; it does not flip overnight.

## Compatibility

- Adds one game rule, one on-action, and one scripted effect. No new events, no overwritten vanilla files.
- The default **Vanilla** setting does nothing, so the mod stays completely inert until you switch it on.
- Works alongside any mod that leaves the vanilla ideology-path mechanic in place.
- Deterministic and multiplayer-synchronized.

## Why it exists

Half the fun of a grand-strategy campaign is having someone to root for and someone to root against. Vanilla makes you wait a few decades to find out which is which. This is for players who would rather set the stage first and then go to war with it.

## Tweaking the interest groups

The left/right split above is a design choice, not a rule the base game enforces — vanilla seats the right-wing markers on whichever governing interest group already leans that way, and none exists at game start. If you would rather give each right-wing path its own power base (Fascism on the Armed Forces, Ethno-Nationalism on the Petty Bourgeoisie, Conservatism on the Landowners), it is a one-line change per option in `common/scripted_effects/pdp_scripted_effects.txt`.
