# AoEView

An Ashita v4 plugin that shows the area of effect of abilities and spells directly on the ground. Additionally, it shows aggro ranges for aggressive mobs.

##Notes:
This plugin is still very much in beta and may be buggy - use at your own risk.
This plugin does **not** send any packets.

## What it shows

**AoE ranges.** When a player or monster starts an area-of-effect spell, ability.

| Color | Meaning |
|-------|---------|
| Blue | Player buff / heal |
| Red-purple | Player attack |
| Green | Monster buff / heal |
| Red | Monster attack |

**Aggro zones.** Around nearby aggressive monsters that are idle and unclaimed, AoEView draws where they will notice you:

|Aggro Type| Description|
|-------|----------------|
| Sight | Yellow cone in the direction that the mob is facing |
| Sound | Orange circle |
| Magic | Cyan circle |
| Blood | Dark red circle |

A mob can have more than one. Aggro zones are only drawn on mobs within a 45yalm radius of the player.

## Installing and loading

1. Copy `AoEView.dll` into your Ashita `plugins` folder.
2. In game, type `/load AoEView`.
3. To load it automatically, add `/load AoEView` to your Ashita startup script.

## Commands

All commands start with `/aoe`.

| Command | What it does |
|---------|--------------|
| `/aoe aggro` | Turn aggro zones on or off (on by default) |
| `/aoe packets` | Turn AoE display on or off (on by default) |
| `/aoe filter all` | Show actions from both players and monsters (default) |
| `/aoe filter players` | Only show actions started by players |
| `/aoe filter mobs` | Only show actions started by monsters |
| `/aoe scope party` | Show actions involving you, your party or your alliance (default) |
| `/aoe scope solo` | Only show actions started by you or aimed at you |

## Good to know

- Aggro zones only appear for monsters the monster database lists as aggressive. They show *where* a monster can notice you, not whether it will.
- Ranges come from LandSandBoat server data and may not be 100% retail / specific private server accurate.
- If shapes stop showing, `/unload AoEView` then `/load AoEView` resets the plugin.
