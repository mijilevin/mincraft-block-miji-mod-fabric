# Miji Mod

Miji adds a craftable block and server mini-games to Minecraft Java Edition.

The block's name is available in English and Hebrew. Choose Hebrew in Minecraft's language settings to see it as `מיג׳י`.

## Modded head compatibility

The Miji recipe accepts vanilla player and mob heads. It also accepts heads added by other mods when those mods include their head items in Minecraft's `minecraft:skulls` item tag.

## Mini-games

Any player can start or stop one timed mini-game at a time. All players can compete; the first player to finish wins a Miji block. Each round lasts two minutes.
Every Miji and teleport command is available to any player, including players who are not OP.

- `/miji game start mining` — break 20 blocks.
- `/miji game start ores` — mine 3 ore blocks.
- `/miji game start heads` — break 1 mob or player head.
- `/miji game status` — see the active round and time remaining.
- `/miji game stop` — stop the round.

## Teleport requests

- `/tpa <player>` — ask to teleport to a player.
- `/tpaccept [player]` — accept the latest request, or choose a player.
- `/tpdeny [player]` — deny the latest request, or choose a player.

Requests expire after 60 seconds. These commands work for non-OP players too.

The ore and head games use Fabric's shared `c:ores` and `c:skulls` block tags, so they include modded ores and heads added to those tags.

## More Fabric mods

These optional third-party mods are separate downloads for players or servers running Fabric. They are not required to join a Miji server. Check each project page for dependencies and install requirements.

- [MinigamesMod](https://modrinth.com/mod/minigamesmod) — client-side games such as Snake, Tetris, Minesweeper, and Solitaire.
- [Minimega](https://modrinth.com/mod/minimega) — multiplayer mini-games inspired by Minecraft Legacy Console Edition.
- [Lockout Bingo](https://modrinth.com/mod/lockout-bingo) — a multiplayer bingo challenge.
- [Bogey!](https://modrinth.com/mod/bogey) — a golf mini-game.
- [Beach Games](https://modrinth.com/mod/beach-games) — beach ball and frisbee activities.
- [Sodium](https://modrinth.com/mod/sodium) — improves client rendering performance.

This is a curated starter list, not a bundle of 999 mods. Mod availability and compatibility change, so use each project's Minecraft 26.2 files and read its server/client requirements before installing it.

## Collecting the block

Mine Miji with any tool or by hand to make it drop itself.

## Requirements

- Minecraft Java Edition 26.2
- Fabric Loader 0.19.5 or newer on the server
- Fabric API for Minecraft 26.2 on the server
- Java 25 or newer for the server

Only the Fabric server needs `miji.jar` and Fabric API. Polymer is bundled inside `miji.jar`. Players can join with an unmodded Minecraft Java 26.2 client; they do not need Fabric or the Miji mod installed. Polymer shows the custom block and item to vanilla clients.

Polymer hosts and sends the Miji resource pack automatically after auto-host is enabled. Start the server once, set `enabled` to `true` in `config/polymer/auto-host.json`, then restart. Players need to accept the server resource pack to see the Miji texture correctly.

## Vanilla players

Vanilla clients can join the Fabric server without installing Miji, Fabric, or Fabric API. The server itself must run Fabric and have Fabric API installed.

## Install on a Fabric server

1. Set up a Fabric server for Minecraft 26.2 using the [Fabric installation guide](https://docs.fabricmc.net/players/installing-fabric/).
2. Put `miji.jar` and the Fabric API jar for Minecraft 26.2 in the server's `mods` folder.
3. In a separately installed server's `eula.txt`, set `eula=true` only after accepting Minecraft's EULA. This project's Gradle `runServer` task keeps its development file at `run/eula.txt` set to `eula=true`.
4. Start the server. In `config/polymer/auto-host.json`, set `enabled` to `true`, then restart the server.
5. Players join using Minecraft Java Edition 26.2 and accept the server resource pack prompt. They do not install Miji or Fabric on their computers.

See Minecraft's [server setup guide](https://help.minecraft.net/hc/en-us/articles/360058525452) and Fabric's [server installation guide](https://docs.fabricmc.net/players/installing-fabric/) for details. Download Fabric API for Minecraft 26.2 from [Modrinth](https://modrinth.com/mod/fabric-api).

## License

This project is available under the CC0 license.

Miji has a 3D stepped-relief model: its image is mapped onto raised block-sized tiles with shaded sides. The block item also uses this 3D model.
