## 0.9.292

This release covers everything since b208. It is a large update: most of the world, the props and the creatures are now the host's, and every other player sees them as the host does.

- **Everyone in a lobby needs the same build, so update together.** A lobby admits only players on the same build number. Lobbies of other builds still show in the browser but refuse the join. Players who all stay on b208 can keep playing among themselves.

**Joining and lobbies**

- Lobbies are signed: a host proves its key to the master server, a lobby no longer vanishes when a master forgets it, and a refused or stopped announce no longer leaves a ghost lobby.
- The browser and the join check compare the game build each side runs and name a mismatch in a popup; the update check answers per game version.
- A join waits until the host's world has settled, so a joiner no longer captures a half-built world.
- A joiner holds back what it cannot place yet (props, drives, containers, Kerfus) until the thing it belongs to exists, instead of losing it.
- A joining player is told about everything that changed after the host's save was cut: nametags, hooks, plants, the vent crawl, the daily task and the host's weather.
- A join or host click names its refusal by code, and an install that cannot index the game ends the join by name.
- The pause menu lets a player leave during an event, and the last player to leave no longer scrambles the host's session reset.
- Flooding a host with requests ends that client, and a source that floods is refused for ten minutes.

**The world**

- The host's bad sun, the earth teleport's sounds, the harvest sound, the alien noise and a faucet's click reach every player; a joiner in the middle of an alien noise gets it.
- Plants are the host's: planting, growth, berries, damage and the growth lamp's glow are one state for everyone.
- Deer, trees, dirt holes and beehives are the host's, and one set of them is shown to every player.
- The vent crawl is shared: its sounds, the breaking vent and the swing are seen by everyone, and a player who joins mid-crawl sees it as it stands.
- A spilled liquid is the host's: decal, splash and pour look the same for everyone.
- The cargo lift, the woodchipper (fuel and switch) and the shared balance are the host's on every machine.
- The host's save is announced to every player, including a save that failed.
- A client no longer rolls the night's creatures or the host's events itself.
- Launchers such as the salt rocket: a client's shot and its explosion are sent to the host, which judges them and spawns the blast for everyone.
- Explosions are the host's: a blast that flings props drives those props on every machine.
- The ATV's fuel, modules, controls and horn are the host's, and a client's ATV acts are asked of the host first.

**The signal desk and its devices**

- The refiner's cap label shows the same level on every player's screen, and a loaded desk repaints its label.
- The desk's signal view settings, the dish's slew sounds and a pinging player's progress are shown to everyone; a player who dies or is knocked down mid-ping frees the desk.
- The base computer's short circuit is the host's, and a client's press of it is carried out on the host.
- A client's laptop module purchases are paid and bought by the host.
- The coordinate towers, the fuse towers and the radio tower are the host's and share their claims; a refused claim is answered.
- A disc full of server data crosses between players, and a disc the host ejects arrives with its files.
- The drone's leave timer is shared, and a client's drone copy plays back on the host's timing.
- The notebook, its torn pages and the open page are shared; whoever holds the claim writes, anyone writes while it is free.
- The coffee machine and its cups are shared, and a client's press is a request the host performs.
- Cords and their sockets are shared: the player who plugs a cord in claims the link.

**Props, trash and tools**

- The host judges takes, uses and puts of a prop: a client asks first and is told the answer, and two players can no longer hold one keyed prop.
- Containers are the host's: a client's take, put or throw is judged by the host and a thrown container keeps its contents.
- Food has one author: the host, or the hand that holds it. Bites, opened cans, snacks, MREs and first aid kits a client uses are performed on the host, and a food's poison reaches everyone.
- Props a client throws or swings stay in sync until they rest; the host takes a thrown prop back if the thrower falls silent.
- Doors you drag by the mouse are shared, including their rest pose for a joiner.
- Nametags on props are the host's and every player sees them, a joiner included.
- The remover tool, the properties tool and the toolgun's freeze, unfreeze and make-static are requests the host judges and shows to all.
- A hook taken back by a client goes through the host, and a joiner gets the hooks taken before it was ready.
- Sleeping bags and mattresses (unrolling, taking one off a bunk bed) are shared.
- A snack's wrapper and the shop's drive and reel-case changes reach every player.
- Trash piles hold still on a joiner until their bind arrives, and a pile that gives up lands what it held.

**Creatures**

- The walking mannequin is one creature, the host's, for every player: it hunts one player and keeps it, freezes only on its target's gaze, and its hit lands on the right machine.
- The Octa (and the geometric Octa) decide on the host and every client replays the host's decisions; a joiner mid-attack gets the attack.
- A client's creature copies never think for themselves, and a client's hit on a creature is judged by the host.
- A deer, a hound and a tree show the host's pose and size.
- A client's cremator copy spits no fireballs of its own.

**Players**

- The crematorium is an admin action: a host can send a player to the crematorium, and the lever run is shown to everyone. A cremated player no longer earns the host an achievement.
- A trip to the backrooms belongs to the player who clips out: the others see that player's copy hidden, the backrooms are dark with the world's sky above, and the host can close the backrooms for everyone.
- A nightmare is one player's, a client included, and a client's rest ends with the game's own wakeup.
- A revived player wakes beside the base bed instead of at the gate, and a revive puts the fire out and clears every black screen.
- An empty battery switches the flashlight off for every player, and a remote player's body no longer shadows its own flashlight.
- A remote player's death is announced, and a peer's copy takes no damage or fire of this machine.

**Commands, moderation and settings**

- Hosts get a permissions system with groups and an in-game editor, and chat lines starting with / run as commands on the host (/help, /set, /reset, /kick, /ban, /tphere, /cremate).
- The F1 Administration panel gains a Server settings pane; changes reach every player live, and the voice range is a session setting.
- Bans are checked at the identity proof, and an Offline list shows recorded players.
- The in-game bug report writes a redacted zip.
- The mod's own text can be translated: the interface, the browser, chat lines and the feed follow the player's language, and a Chinese pack ships.

**Graphics and input**

- The overlay now works on Vulkan as well as DirectX.
- The game window is hooked from boot, the overlay hotkeys open only once the overlay is up, and a larger game window is followed.

**Stability**

- A player who minimizes the game or has it behind another window while joining now finishes the join properly; before, the session stayed half-joined.
- Closing a menu while the HUD is hidden no longer leaves text input or push-to-talk stuck.
- Classes that were still loading when a spawn arrived are asked again instead of dropping the spawn.
- The mod keeps an index of every live prop and finds a prop by key instead of walking the world.
- A world-ready flood, a repeated join and a repeated save request are refused without taking the session down.
- A build that cannot hook the game's script loop starts no session.

Known limitations:

- A blast a client sets off some other way -- breaking an object, a microwave, a MOAB, a PC -- can still be seen on that client only. A client's own rocket, sticky bomb, grenade, pipe bomb, burning and driven ATV all go through the host.
- A client's copy of a flying rocket shows no fuse or thrust, and a player who joins does not see an explosion that went off before their world was ready.
- After loading a save, the refiner's cap label may show the old level until the desk is used.
- In testing, the host's game closed by itself once during a very early backrooms trip; a likely cause was fixed and it did not happen again, but it is not proven gone.

This is a development prerelease. Please report what breaks:
https://github.com/VOTV-MP/Multivoid/issues

## 0.9.208

- **Update together.** A lobby admits only players on the same build: lobbies of other builds
  still show in the browser but refuse the join. Players who stay on b150 can play among themselves.

**Joining and lobbies**

- Two master servers, in the USA and in the EU: the browser has a tab for each, and a host
  announces its lobby to the one it picks.
- A lobby's row shows its real player count (it used to read "1/4") and how its players reach
  the host: direct, LAN or relay.
- Joining through the relay keeps working after the first two minutes: the host's relay
  credential is renewed with every heartbeat.
- The join screen shows the host's world downloading, a join waits on the step that is working
  instead of one fixed timeout, and a failed join names the step it failed at.
- A large world downloads without choking the connection: sending is paced to what the link
  actually delivers.
- A joiner loads in the host's game mode, keeps its own inventory, health and spot, and a join
  during an event gets the live world.
- A join started from inside a world of your own leaves it for the menu and loads the host's.
- The relay policy and the listen port you set apply to every session, and a relay setting a
  session cannot honour is refused by name.
- Hosting a save from another game version warns first.
- The main menu shows a thanks list.

**The world**

- A coop session plays by the save's world rules (fall damage, for one) and starts on the save's
  day; it used to run on the defaults.
- The clock is the host's: a client's time of day and its midnight follow the host's.
- Weather and world events come from the host: lightning, the red sky, the sky eye, jellyfish.
- Power is the host's: the power panel, the generators, their repair puzzles, upgrades and wear;
  a client's upgrade the host refuses is handed back.
- Doors, keypads, light switches, light groups, the garage door, lockers, lids and appliances are
  shared as they are used; a client's door press, hit and pry run on the host, doors close by
  themselves again, and a client's keypad works after a blackout and a repair.
- Doors, lights, light groups and containers are named the same way on every machine, so a
  client's presses reach them.
- An oven repaired by one player is repaired for everyone.
- A container take is judged by the player's reach to it, and a container's view closes when you
  walk away from it.
- Shop upgrades are the host's, and so is the bill; a client earns into the shared balance.

**The signal desk and its devices**

- The desk runs on the host: downloading, pinging, the scan needle, the dish's calibration and
  precision, the hash codes, the coordinate towers, decoding on the refiner, saving a signal (its
  photo too) and the signal database; a client's press is carried out on the host's desk.
- The drive slots, the drive rack, the drive box, the eraser, the laptop's disc slot and the
  server boxes (breaking, repairing, upgrades) are the host's.
- A player who joins in the middle of a download or a decode gets it as it stands.
- A device no longer takes a drive or a module another player is carrying out of their hands.
- A disc keeps its contents when it is handed over or ejected, and a disc put into a signal
  server stays there for everyone, a joining player included.

**Props, trash and tools**

- Props keep one identity across players, so a prop moved, frozen or freed by one player does the
  same for everyone: a wall-mounted fire extinguisher, a sign or a torch holder pried off its wall.
- A prop a client spawns from the spawn menu reaches everyone.
- A client no longer deletes props the host still holds.
- Trash piles, clumps and the broom are the host's; a client's sweeping, bagging and carrying
  reach everyone.
- Cleaning grime and windows, and the wall fixer's repairs, reach everyone.
- A deployed hook, and what it drags, is visible to everyone.

**Creatures**

- The plain kerfur thinks on the host; a Kerfus a client turns on follows that client, and a
  thrown Kerfus no longer vanishes for the other players.
- The drone rests where the host's does, and a client's press of the drone console runs on the
  host.

**Stability**

- One cause of the "Fatal Error!" crash at game start is removed: the mod's hook install no longer
  races the game's embedded browser.
- The mod keeps an index of the game's objects instead of rescanning them every frame.
- The host's log no longer fills with false alarms while somebody joins.

Known limitations:

- The desk's back panels and the drone's sack are not shared yet.
- When one player carries a device and another a prop that fits it, neither of their worlds takes
  the prop.

## 0.9.150

- **INSTALL CHANGE — if you are on b133, uninstall it before installing this.** Multivoid
  is now a normal UE4SS mod (`Mods/Multivoid/`), so it installs through r2modman or
  Thunderstore Mod Manager, or by hand into the game's `Mods` folder. The old standalone
  loader is gone, and this build **refuses to start** if a leftover `multivoid-*.dll` or
  `votv-coop.dll` is still sitting next to the game executable — it will tell you so in a
  dialog rather than failing quietly. Steps: `docs/install.md`.
- **Four scientist skins ship with the mod.** They are in the package; no separate download.
  The F1 skin picker now only lists skins the game can actually put on you, and picking one
  that briefly fails to load no longer wipes the skin you had chosen.
- **The in-game server browser is now the game's own UI, not an overlay.** It opens from the
  main menu, uses VOTV's colours and sounds, and supports hovering, selecting, scrolling,
  Connect, Host, Refresh and Back. The old F1 browser is still there as a fallback if you
  turn it on in `multivoid.ini`.
- **You are only let into a lobby after proving who you are.** Every install now has a durable
  keypair, and both sides prove themselves to each other before a seat is spent — the host
  proves itself first. Your saved data is keyed to that identity instead of to a name anyone
  could type.
- **Lobby passwords are enforced.** "Locked" used to be a label on a lobby that anyone could
  still walk into. A password now actually gates admission, and it is bound to the host's key
  so it cannot be replayed at a different host.
- **Nobody can take over your lobby's name on the matchmaking server.** Registrations are
  signed now, and the client refuses to talk to a relay that does not challenge it.
- **Death no longer ends the session.** You hear the death, the screen goes black, and then
  you are revived where you were, instead of the game unloading the world and throwing
  everyone to the main menu. The red damage overlay no longer stays on your screen afterwards,
  and a dead player can open the pause menu again.
- **Shopping and coins are real transactions now.** Laptop shop orders are priced by the host
  from its own table instead of by the buyer, the coin gun's sales are performed by the host,
  and a client can finally pick up coins the host dropped.
- **The ATV is drivable together.** A peer that is not driving no longer freezes its copy of
  the ATV; it simulates and is steered onto the driver's pose. Tyre wear, dirt and damage now
  travel with it, so both players see the same vehicle condition.
- **Light switches and the lamps they drive agree across peers.** Previously only the switch's
  own click travelled and the lights themselves were left to each player's world.
- **The F1 overlay works with RTSS, MSI Afterburner and OBS.** It used to be invisible while
  RTSS was running, and OBS's default game capture did not record it at all. Both are fixed on
  DirectX 11 and DirectX 12.
- **Hosting can be done more than once per session.** The second time you hosted a New Game it
  failed on a duplicate save name and dumped you back to the browser with no reason shown.
  Server names are also editable on the session settings screen now.
- **A host who quit to the menu and hosted a different map could send the joining player an
  empty world** — two ATVs, every door disagreeing. The host now refuses to send a world that
  describes nothing.
- **Rejoining a session no longer crashes the game.**
- Chat, names and non-English text carry over from b133 unchanged, and every text field the
  game owns keeps its keys — the mod does not steal them.

Known limitation: if the host refuses a coin-gun sale, the item is still consumed. Refusals
should be rare now that the underlying cause is fixed, but the sale is not yet atomic.

This is a development prerelease. Please report what breaks:
https://github.com/VOTV-MP/Multivoid/issues

## 0.9.133

- **Chat now has history.** Press `T` and the last messages fade back in above the
  input bar; `PgUp`/`PgDn` page through them, and the fade-out clock stops while you
  are reading so nothing expires under you. A player who joins mid-session is seeded
  with the lobby's chat record instead of arriving to an empty feed.
- **The player list (tilde) answers the same question on every row.** It now lists
  everyone — the host, other clients, and yourself — with an ID column, and shows how
  each player reaches the session plus their ping. Your own row is no longer blank.
- **Names are unique and the host decides them.** If two players ask for the same
  name the host hands out `Name2`, `Name3`, and the assignment is written back to
  `multivoid.ini`, so you keep it next session. Names that merely *look* identical
  (Latin `A` vs Cyrillic `А`) still count as taken.
- **Non-English names and chat actually render.** Cyrillic, Greek, Hebrew, Thai,
  Arabic, Tamil, Dhivehi and Latin-Extended text now draw instead of falling back to
  boxes — 4,700+ characters that were previously unrenderable, plus emoji. Combining
  marks are included, so scripts written entirely with them (Dhivehi) are writable at
  all. Case-insensitive name matching now covers Greek, Armenian, Georgian and
  Latin-Extended, which it silently did not before.
- **The mouse cursor is visible again in the multiplayer menus.** At any UI scale
  below 1.0 the software cursor was being drawn at zero size — present, tracking, and
  completely invisible.
- **The mod no longer steals keys the game is typing.** You can type at the in-game
  SAT server console, the notepad, save-slot names and the settings search without
  `T` opening chat or `V` opening the voice panel. Function keys still reach the mod,
  so `F1` works even inside a game interface. (GitHub issue #5.)
- **Nameplates:** the name and ping are centred on the health bar as one label, and a
  client now sees the host's ping instead of a blank.
- **A message you just sent no longer flickers** out of the chat feed and back in.
- The overlay renders correctly under DirectX 12, including a fix for a rare crash in
  its texture-release path.
- Chat text arriving from other players is now validated as UTF-8 at the receive
  boundary and refused if malformed.

## 0.9.128

- The in-game overlay (F1 menu, chat, nameplates, dialogs) now renders under
  DirectX 12 — it was DX11-only before. If you launch VotV with `-dx12`, the
  mod's UI now draws instead of logging a warning.
- The F1 menu shows which graphics API the game is running on ("Graphics API:
  DX11/DX12").
- The "Tidy up" button in the boot-time SETTINGS CHECK notice now actually
  works: it reformats `multivoid.ini` and comments out unknown or invalid
  lines. It was a dead button before.
- New install guide: [docs/install.md](https://github.com/VOTV-MP/Multivoid/blob/main/docs/install.md)
  — release pages now carry install steps and this changelog section.
- README gained a Credits section (prior art: MTA:SA, RE-UE4SS, MinHook,
  VoidTogether) and a living playbook for porting the mod to future VotV
  versions (`docs/versioning.md`).

## 0.9.127

- `multivoid.ini.example` is now generated next to `multivoid.ini` on every
  boot: a catalog of every setting the mod reads, each with a description.
  `multivoid.ini` itself is never overwritten.
- Internal config-system hardening (typed settings registry; a CI gate keeps
  the settings catalog and the code in lockstep).
- `BUILDING.md`: the mod can now be built from source via GitHub Actions alone,
  no local toolchain needed.

## 0.9.126

- First public development build.
- The whole co-op layer as of July 2026: shared world and props, host-scheduled
  events and NPCs, the signal desk, proximity voice and text chat, server
  browser and direct connect, skins.
- Settings live in one file next to the game executable (`multivoid.ini`); on
  boot the mod checks it and shows a SETTINGS CHECK notice if something is off.
