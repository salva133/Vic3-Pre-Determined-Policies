# Pre-Determined Policies

**A game-rule mod for Victoria 3** that decides, before the campaign even begins, which way every AI country will lean — so the political map is something you can plan around instead of something you discover the hard way.

## The idea

Victoria 3 quietly keeps track of when a nation commits to a radical ideology. The moment a country picks its path, the game plants a hidden marker on the interest group that carried it there — the Trade Unions turning communist, a governing faction turning fascist, and so on. Normally those markers appear on their own, deep into a campaign, and you never see them coming.

This mod hands you the pen. Add a single game rule in the lobby, choose one ideology, and every AI nation is seeded with that same marker from day one. Pick **Communism** and the workers' movements of the world will be yours to court or crush; pick **Fascism** and you know exactly where the storm is coming from. Either way, you start the game knowing who your friends and your enemies are going to be.

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
| **Historical** | Every AI country begins on the path its 1936 government took — the Axis powers Fascist, the Soviet Union Vanguardist, Kemalist Turkey Ethno-Nationalist, and everyone else on the Conservative status quo. |
| **Absolute Insanity** | Every AI country is seeded with a completely random path, drawn independently for each nation. |

Your own nation is never touched — you always choose your own path. In multiplayer, every human player is left free.

## How it works

The chosen marker is applied once to every non-player country. Because the base game keeps these markers on interest groups rather than on countries, the mod seats each one on an interest group nearly every nation has: the left-wing paths on the **Trade Unions** — exactly where vanilla puts them — and the right-wing paths on the **Armed Forces**, a dependable stand-in for the governing group vanilla would otherwise pick out for itself. Any country that somehow lacks the group is simply skipped.

A marked interest group turns away from path-neutral moderates: vanilla cuts the leader weight of every off-path stance there — the moderates included — to a tenth, so the group keeps putting forward leaders of the ideology you chose. That is the same lever the base game pulls when a country radicalizes on its own, so the world leans toward the path you picked over the years of a campaign; it does not flip overnight.

## Why it exists

Half the fun of a grand-strategy campaign is having someone to root for and someone to root against. Vanilla makes you wait a few decades to find out which is which. This is for players who would rather set the stage first and then go to war with it.
