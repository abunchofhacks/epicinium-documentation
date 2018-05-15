## Hotfix 0.22.2 (15-05-2018)

*This is a server-only hotfix that is compatible with release 0.22.0.*

### Bugs
- Fixed a bug where vision was not calculated properly, which could result in invisible units or units leaving behind ghosts when disappearing in the fog of war.

### Technical
- When a user attempts to reconnect after a crash, the server might believe that they are still online. Instead of rejecting the attempt, it will now be put on hold for a few moments until the old connection has been dropped.


## Hotfix 0.22.1 (14-05-2018)

*This is a server-only hotfix that is compatible with release 0.22.0.*

### Bugs
- Fixed an issue that caused the server to freeze for several minutes when a player disconnected unexpectedly.

### Technical
- Lowered the server-side connection timeout to 2 minutes, down from 10 minutes.


# Release 0.22.0 (12-05-2018)

### Gameplay
- When a unit performs a bypass attack past an entrenched unit and an enemy unit retaliates, the entrenched unit is no longer involved in the resulting damage step.
- All players receive an announcement whenever global warming crosses a threshold, i.e. whenever another 20% of the map is covered by chaos.
- Reenabled fog of war by default, except in the tutorial.

### Content
- Improved the HungryHippo AI so it behaves symmetrically on all maps.
- Improved the RampantRhino AI so it makes better use of its units and capitalizes on an income lead by building more City tiles.

### Visuals & User Interface
- Joining a match in progress is now instantaneous.
- In the Winter growth phase, Snow also appears on tiles in the fog of war whose last known humidity is high enough.
- The chaometer has been removed in favor of a newspaper; this newspaper appears whenever global warming crosses a threshold. The last issue of the newspaper can also be brought back by clicking the date in the bottom left.
- The panels detailing unit and tile stats have been significantly simplified and now only show size, power and hitpoints.
- The hygrometer and weather markers are now placed above these panels.
- The wallet and the diamond button that reveals the player info panel have been unified.
- Added option in the lobby to create a copy of an AI player.
- In Fullscreen mode, the resolutions list in the settings menu will only contain resolutions the monitor supports (as far as we can detect).
- In Fullscreen Desktop mode, no resolution can be specified because it will be the same as the user's desktop.

### Bugs
- Fixed a bug where a Trenches tile would provide its defense bonus during the retaliation attack that takes place when a unit performs a bypass attack past an entrenched unit.
- Added a missing delay between the sound effects of unit figures dying as a result of Death.
- The UPDATE button is now properly disabled while downloading a patch.
- Fixed a bug where certain particles would only render at scale 2.
- Fixed a bug where the mouse position was incorrectly matched to its position on the screen under certain resolutions, preventing buttons from being clicked.
- Fixed a bug in Windows where in Windowed Borderless the window would be offset and the cursor position misaligned.
- Fixed a server crash that could occur when a player left the server and a lobby was disbanded at the same time.
- Fixed a bug where normal lobbies could be started on the tutorial map.

### Technical
- Improved native resolution detection.
- Added support for multiple monitors. The game will not use the primary monitor by default. The monitor can be selected in the settings menu.
- In windowed mode and borderless windowed mode, the position of the window can be changed using the settings menu.
- Fullscreen and Fullscreen Desktop now behave as intended, without any undesired stretching or clipping.
- Made sure the game window is never displayed at a resolution the monitor does not support in Fullscreen mode.


## Release 0.21.1 (02-05-2018)

*This is a Linux-only release that fixes compatibility with Ubuntu 18.04.*

### Bugs
- Fixed a compatibility issue that caused the game not to start on certain Linux distributions due to differences in libcurl.


# Release 0.21.0 (26-04-2018)

### Content
- Added the maps **small3ffa**, **small4ffa** and **small8ffa**. Unlike the old free-for-all maps whose size scaled with the number of players, these maps are roughly the same size as the *small1v1* map. The chaos thresholds now scale with the size of the map instead of with the number of players, so expect a lot of global warming on these maps.
- Removed the maps *oasis3ffa* and *beetle4ffa* from the map pool.

### Visuals & User Interface
- When an order is given to a unit or tile, the order appears below that unit or tile and floats to the order list.

### Bugs
- Fixed a bug where non-existing tile buildings could remain on the screen indefinitely after the tile had been revealed.
- Fixed a bug where question marks appeared above units that still had old orders to execute.
- Fixed a bug where no sound was played when an Industry or Barracks tile was upgraded.
- Fixed a bug where giving an order after pressing the ready button caused that order to remain in the order list when the action phase started.
- Fixed a bug where shadows from dragged players in the lobby could persist when the game was started.
- Fixed a bug in the lobby menu where changing a player's color could move them to the observers.
- Fixed a bug where a disconnected player could leave behind a ghost in the lobby.
- Fixed bug where draggable items would remain dragged if clicked with a very low framerate.
- Fixed a compatibility issue on Arch Linux.


# Release 0.20.0 (14-04-2018)

### Gameplay
- Disabled fog of war for human players. Fog of war can be reenabled per player by switching between "global vision" (no fog of war) and "normal vision" (fog of war).

### Visuals & User Interface
- Added an in-game panel that displays which player goes first each round.
- Orders can be rearranged by clicking and dragging them. (**Issue #1**)
- Added a blue button to orders in the order list. Clicking the button on a new order revokes the order. Clicking the button on an old order issues a Stop order to override the old order. (**Issue #2**)
- The in-game camera starts out with your tiles and units in view.
- Added a texture and decorative mountains to the edges of the map.
- In the lobby, players can be dragged to the observers list and back.
- The "PLAY" button on the main menu now turns into an "UPDATE" button when a patch is available to be downloaded.
- The "PLAY" button's tooltip is now more informative and appropriate to the specific situation.
- In case you forgot your password, you can now reset it from the main menu.
- The login form now displays a confirmation of a succesful registration or password reset.
- If joining the server fails due to a locked account, the login form now displays the reason.

### Bugs
- Fixed a bug where the game does not fade in from black.
- Fixed a bug where the caret did not appear when a text input was selected.
- Fixed a bug where the "PLAY" button would be enabled inappropriately.
- Fixed a bug where the server would accept clients with old version to join.

### Technical
- Login sessions are now invalidated after a manual logout.
- Login sessions that should not be remembered are now always invalidated after logout or game close.
- You will now receive an email if you are resetting your password or when your account is locked from too many failed login attempts.


# Release 0.19.0 (05-04-2018)

### Accounts
- Users can no longer join the server multiple times at once with the same account.

### Visuals & User Interface
- Added a leaderboard tab to the multiplayer menu.
- Renamed "Camera Scrolling" to "View Scrolling" in the settings menu.
- The tutorial is less rigid and will allow you to continue as long as you have given a correct order, without having to also select that unit.
- Increased the animation speed of the Farm tile's cultivate ability.
- Improved error handling when joining server: the reason for failure (currently: session expired or already joined) is displayed in a login prompt.
- Changed the wording of the rating change notification.
- Added tooltip to start button when it is grayed out.
- Added coin icon before cost in the order context menu.
- Fixed the placement of text on different scale settings.
- Added some margin to the tooltips in the multiplayer menu.

### Bugs
- Fixed a bug in the animation timing of units that are attacked from within the fog of war.
- Fixed a bug where trees and buildings from the fog of war would remain on the screen for too long after the real tile was revealed.
- Fixed an issue where the rating change notification would sometimes not appear after a lobby was disbanded.
- Prevent crash when quickly starting new threads through repeated reconnection, login or registration.
- Fixed a bug where the players were too spaced out in the lobby after joining a replay lobby.
- Fixed a bug where sprites would show the wrong frame once every couple of draw steps in 32-bit Windows versions of the game.


## Hotfix 0.18.1 (26-03-2018)

*This is a server-only hotfix that is compatible with release 0.18.0.*

### Gameplay
- First player advantage is now properly randomized.

### Content
- Lowered the aggressiveness of the Easy RampantRhino, and increased the aggressiveness of the Hard RampantRhino.
- Improved the RampantRhino AI to prevent its units from blocking each other.


# Release 0.18.0 (21-03-2018)

### Accounts
- The game now requires an Epicinium account with username, email and password. This allows you to log in with the same account on different computers. (**Issue #33**)
- Usernames are now restricted to alphanumeric ASCII characters and the characters '_', '-', '.' and '~'. Support for usernames with non-ASCII characters (such as Cyrillic or Chinese) will be added in the future.
- Some players had issues with files not being saved correctly and were forced to create multiple accounts with slightly different usernames. We will manually merge the ranks of these accounts into a new Epicinium account.

### Gameplay
- Decreased the hitpoints of City, Town and Farm tiles to 2, down from 3.
- Decreased the cost of the City tile to 20, down from 30.
- Decreased the cost of upgrading a Town tile to a City tile to 15, down from 30.
- Industry and Barracks tiles can be upgraded to increase their size, for a cost of 30. At night, each Industry or Barracks tile gains power if the total power of surrounding City tiles is greater than its current power, but this does not automatically create a new building.
- Frostbite only appears on Grass, Dirt, Desert and Rubble tiles.
- Frostbite no longer lowers hitpoints, and instead deals 2 shots of 1 damage to ground units in the Decay phase.
- Dirt tiles without humidity transform to Desert tiles if at least 40% of the map is covered by chaos, up from 20%.

### Content
- Reworked the *toad1v1*, *spruce1v1* and *oceanside1v1* maps to make expansion areas more interactive.
- Updated the Medium and Hard TutorialTurtle to be more difficult to beat, and to allow them to use Sappers.
- Added the RampantRhino AI, an aggressive variant of the TutorialTurtle.

### Visuals & User Interface
- Reworked the main menu and added login and registration functionality.
- The "Waiting for response from server..." notice time is changed from 5 to 10 seconds after sending ping.
- New notice "Connection to server resumed" added after receiving pong after the aforementioned 10 seconds.
- Added "Authenticating..." notice to multiplayer menu while waiting for confirmation from server.

### Technical
- A warning now appears in the main menu if the game detects that it cannot properly save configuration files on the system.
- Communication with the server now uses our new domain name, server.epicinium.nl, instead of using the IP address directly.
- Login and registration uses login.epicinium.nl.
- Login now works with sessions: a session token (with temporary validity) is issued while logging in, which is validated when joining the server.
- Account files are now used to (optionally) remember sessions.


## Hotfix 0.17.1 (12-03-2018)

*This is a server-only hotfix that is compatible with release 0.17.0.*

### Bugs
- Fixed an issue where replays from version 0.17.0 could not be viewed due to missing data.
- Fixed an issue where missing data while viewing a replay caused the lobby to crash.
- Fixed an issue where a single lobby crash caused the server to crash.


# Release 0.17.0 (01-03-2018)

*Due to a bug in the patcher, Windows users may need to update manually.*

### Gameplay
- Snow, Frostbite, Firestorm, Bonedrought and Death also update at the end of every Night phase.
- Death is placed on one random tile per player per Weather or Night phase, instead of two random tiles per player per Weather phase.

### Content
- Altered the bottom of the *spruce1v1* map slightly.

### Visuals & User Interface
- Added UI elements that show the hitpoints, movement speed, vision radius, attack damage, ability volleys, ability range and income of units and tiles under the cursor.
- At night, clouds of Gas appear transparent instead of invisible.
- Before a unit fires, its figures show a short aim animation.
- When a unit is triggered to fire because of a Focus Attack of another unit or because of an Attack of Opportunity, an exclamation mark pops up above each of its figures.
- When a moving unit is part of an Attack of Opportunity, it briefly stops moving.
- Units without orders have a question mark pop up until they are selected.
- Target guides now blink to help differentiate them from order guides.
- The color of humid grass is now consistent within each map, but varies between maps.
- Adjusted the colorization of dry grass to be more readable across all maps.
- The pause icon that appears in the tutorial can now be clicked to unpause the game.
- In the multiplayer menu's playerlist and lobby, the player's own username is now colored dark red to distinguish it from other usernames.

### Audio
- Added titlescreen music. (**Issue #11**)
- Increased overall loudness of the game.
- Decreased relative loudness of explosions and collapses.

### Bugs
- Fixed some bugs where the main menu would give incorrect or misleading information regarding the connection status.
- Fixed a bug where the settings would not be saved if settings.json was missing.

### Technical
- Added a notification for when the server takes more than 5 seconds to respond so the player knows what is going on.
- The game will now attempt to reconnect after the server has not responded for 33 seconds, instead of 66 seconds.
- The game will now always attempt to reconnect when the connection closes unexpectedly, instead of only in the case where the server seems up but does not respond to ping.
- The game will now keep attempting to reconnect after losing connection.
- Improved behavior and information when the server is shutting down for maintenance.
- Made the audio mixer more efficient to prevent audio playback issues on slow machines.
- Fixed a bug that prevented patches from being installed correctly under Windows.


# Release 0.16.1 (16-02-2018)

### Visuals & User Interface
- Added a settings menu. (**Issue #3**)

### Technical
- Removed unused rulesets from the *rulesets* folder.
- Reduced RAM usage by about 75%.


# Release 0.16.0 (09-02-2018)

### Gameplay
- Mountain tiles now cause nearby spaces to start with 4 humidity.
- Water tiles no longer cause nearby spaces to start with more than 3 humidity.
- Snow also occurs in Spring, Summer and Autumn on spaces with 4 humidity.
- Aridification also lowers the humidity of surrounding tiles.
- Firestorm occurs in Summer at random on 24% of the map for every 40% of the map that is covered by chaos, instead of 8% for every 20%.
- Bonedrought occurs on Desert tiles if at least 60% of the map is covered by chaos, up from 40%.
- Bonedrought also occurs on City, Town, Farm, Barracks, Industry, Airfield and Rubble tiles if at least 80% of the map is covered by chaos.
- Death is placed on two random City, Town, Farm, Barracks, Industry or Airfield tiles for every player, up from one per player.
- If a tile or unit is affected by multiple hitpoint modifiers, such as Frostbite and Bonedrought, its hitpoints can be lowered by more than 1, but not below 1.

### Visuals & User Interface
- Swapped the positions of the chaometer and the weather marker gauge.
- Added an in-game panel that displays which player is playing as what color. Access this panel by clicking on the diamond button in the top left of the screen. For observers, a similar panel can be accessed by clicking the coin button; this panel also shows how much money each player has.
- The "start game" button is disabled when there are not enough players to start a game.
- Added text to main menu that displays when you have been disconnected from the server and tells you to press 'PLAY' to rejoin.

### Audio
- Added a delay between building destruction sounds to reduce the loudness of Upgrade and Death animations.

### Bugs
- Fixed GPU memory leak that could cause the game to crash. (**Issue #32**)
- Fixed bug where the chaometer indicated values slightly lower then intended.
- Fixed bug where the chaometer could grow beyond its container.
- Fixed bug where Dirt turns to Desert before 20% of the map is covered by chaos.
- Fixed bug where AI difficulty was not synchronized correctly when a player joined a lobby.
- Fixed bug where orders would sometimes not be sent at the end of the planning phase if a player did not press the ready button.

### Technical
- If the game was installed via the Itch.io desktop application or via the GameJolt desktop application, the game no longer patches itself to prevent extraneous patching.


## Hotfix 0.15.1 (02-02-2018)

*This is a server-only hotfix that is compatible with release 0.15.0.*

### Bugs
- ~~Fixed bug where Dirt turns to Desert before 20% of the map is covered by chaos.~~

### Technical
- When all players are disconnected from a non-tutorial game in progress, the lobby is not disbanded immediately but remains alive for ten minutes.


# Release 0.15.0 (27-01-2018)

### Gameplay
- Removed temperature from the game.
- Humidity ranges from 0 to 4, instead of from 0 to 100. Water and Mountain tiles cause nearby spaces to start with more than 2 humidity. Desert tiles can cause nearby spaces to start with only 1 humidity.
- Each space can have up to 1 chaos counter. Chaos counters no longer influence the weather on the spaces they are on; only the total number of chaos counters matters. When a chaos counter would be placed on a space that already has a chaos counter, it is placed on a random other space instead.
- Aridification occurs at random on 8% of the map for every 20% of the map that is covered by chaos.
- Aridification lowers humidity by 1, instead of by 5 percent point.
- Aridification no longer lowers the humidity of surrounding tiles.
- Industry tiles lower humidity of surrounding tiles by 1, instead of by 10 percent point. This only occurs in Autumn.
- Gas lowers humidity by 1, instead of by 10 percent point.
- Degradation occurs when a Grass tile has no humidity.
- Desertification occurs when a Dirt tile has no humidity and at least 20% of the map is covered by chaos.
- Snow occurs in Winter on all spaces with at least 1 humidity.
- Frostbite occurs in Winter on spaces without buildings or trees on them if at least 20% of the map is covered by chaos, on spaces with 1 building or tree on them if at least 40% of the map is covered, etcetera.
- Firestorm occurs in Summer at random on 8% of the map for every 20% of the map that is covered by chaos. Firestorm avoids City, Town, Farm, Barracks, Industry and Airfield tiles if possible.
- Bonedrought occurs on Desert tiles if at least 40% of the map is covered by chaos.
- Once 100% of the map is covered by chaos, Death is placed at random on one random City, Town, Farm, Barracks, Industry or Airfield for every player every Growth phase. Once placed, Death never disappears.
- Reduced chaos emission of Industry tiles to 5, down from 25.
- Reduced chaos emission of City tiles to 2, down from 5.
- Reduced chaos emission of Town, Farm, Barracks, Airfield and Rubble tiles to 1, down from 2.

### Content
- Altered the *spruce1v1* map slightly to make the top area less restrictive.
- Cropped the *oasis3ffa* map and expanded the *beetle4ffa* map so they have the correct number of tiles for the new chaos system.

### Audio
- Unit spawn sounds are no longer played during a rejoin.
- Foot soldier spawn is now three footsteps instead of one.
- Separate volumes for gameplay and music.
- Made volume behave exponentially.
- Made panning behave in accordance to a constant-power rule.

### Visuals & User Interface
- Removed the thermometer.
- The hygrometer now has four segments to indicate how many humidity a space has.
- A new "chaometer" shows a known lower bound and possible upper bound of the total number of chaos counters, based on your current vision of the map.
- The camera no longer pans to show enemy cities gaining power.
- The chat window expands to cover most of the screen, and only shows a small preview when collapsed.

### Bugs
- Fixed a bug where buildings and trees could be improperly placed.


# Release 0.14.0 (20-01-2018)

### Gameplay
- The City tile now generates income.
- The Industry tile generates three income per powered stack, instead of just one per powered stack.
- Increased the cost of the City tile to 30, up from 20.
- Increased the cost of the Industry tile to 3, up from 0.
- Increased the cost of the Barracks tile to 3, up from 2.
- Increased the cost of the Rifleman unit to 10, up from 3.
- Increased the cost of the Gunner unit to 10, up from 6.
- Increased the cost of the Sapper unit to 10, up from 8.
- Increased the cost of the Tank unit to 15, up from 5.
- Increased the starting income to 20, up from 10.

### Content
- Improved phrasing of certain prompts in the in-game tutorial, and added new prompts about building and using Barracks.

### Audio
- Improved the timing of the the tank engine sound.

### Visuals & User Interface
- Unit figures are positioned more towards the center of the tile.
- Guides that appear when a Capture, Shape, Settle, Upgrade or Produce order is given are now blue instead of orange.

### Bugs
- Fixed an issue where joining a replay in progress would skip through the entire recording at once.
- Made the audio code thread-safe, preventing some rare crashes.
- Fixed issue where after playing the tutorial, the tutorial map would be listed in the map picker.
- Fixed a bug where clicking on unpathable tiles would generate invalid move orders.

### Technical
- When a player reconnects to the server after being disconnected from a game against human opponents, the player automatically rejoins the game.
- Framerate and audio volume can now be adjusted by editing *settings.json*.
- The client and the server now ping each other more often to keep the TCP connection alive.


## Hotfix 0.13.0 (12-01-2018)

*Due to a bug in the patcher, updating from v0.11.0 or earlier to v0.12.0 would result in a broken version of the game. This hotfix should allow players to first patch to v0.12.1 and then to v0.13.0.*

### Bugs
- Fixed an issue where the patcher could not install the audio folder.

### Technical
- The game is now able to patch the patcher before the patcher patches the game.


# Release 0.12.0 (11-01-2018)

### Gameplay
- Decreased the maximum size of the Rifleman unit to 3, down from 5.
- Decreased the cost of the Farm tile to 2, down from 5, and increased its maximum size to 2, up from 1. The Farm tile can now produce Rifleman units.
- Settling a Farm tile now immediately cultivates surrounding tiles into Soil tiles. Once built, a Farm tile can still be given a cultivate order to repair any destroyed Soil tiles.
- Decreased the cost of the Town tile to 5, down from 10.
- Decreased the cost of the Industry tile to 0, down from 2.
- Decreased the cost of the Tank unit to 5, down from 10.
- Decreased the starting income to 10, down from 20.
- Crops tiles are now considered natural (like Water tiles) when evaluating if a City, Town of Farm tile gains power.
- Aridification (the humidity loss that occurs in cells with extreme heat) also lowers the humidity of all surrounding cells, but decreased the humidity loss for humid cells to 5, down from 10.
- Ground pollution (the humidity loss caused by Industry tiles) now occurs in all seasons, not just in Autumn.

### Content
- Players no longer start with a Town tile but instead have an extra Rifleman unit of size 1, and City tiles start with 1 power instead of 2.
- The in-game tutorial now has prompts to guide the player and takes place on a new map with a new AI. (**Issue #7**)
- Updated QuickQuack to do farming because gameplay changes made it necessary to do economy.
- Updated HungryHippo to produce and control tanks.

### Visuals & User Interface
- Added auto-pathing assistance; when issuing a Move order to a ground unit, it will now attempt to find a way around any unpathable terrain.
- A message now appears for all players and observers whenever a player is defeated.
- Added tooltips for the players' in-game and in-lobby icons in the multiplayer menu.

### Audio
- Added sound effects during gameplay. (**Issue #12**)
- Added cue for beginning of planning phase. (**Issue #16**)

### Bugs
- Fixed a bug where replays from version 0.10.0 and older did not work.
- Fixed a rare bug where valid orders were discarded for no reason.
- Fixed an issue in free-for-all games where the server would wait for defeated players to ready up.
- Fixed a bug where players could still control their units locally after being defeated.
- Fixed a bug where players could not send messages with quotes in them.
- Fixed a bug where the camera would fly past a tile being captured instead of stopping and showing it.


# Release 0.11.0 (23-12-2017)

### Content
- Added the map **oasis1v1**.
- Added the free-for-all maps **oasis3ffa** and **beetle4ffa**.

### Visuals & User Interface
- Reworked Rifleman and Gunner unit sprites.
- Reworked surface textures and added blending between surfaces.
- Increased the speed at which the diamond icons appeared.

### Bugs
- Fixed a bug where unit figures would keep moving instead of dying when taking lethal damage.
- Fixed a bug where players were able to generate broken orders by clicking on unpathable tiles, which were then discarded by the server. (**Issue #30**)
- Fixed a bug where a starting a game while a chat message was being typed would cause that message to be sent once that player started typing again. The message is now discarded. (**Issue #29**)
- Fixed a bug where observers watching a replay that ends in the planning phase, would not see the "game over" message.
- Fixed a bug where HungryHippo would issue invalid Focus orders.

### Technical
- Reduced the size of the data sent to observers by about 80 percent.


## Hotfix 0.10.1 (18-12-2017)

*This is a server-only hotfix that is compatible with release 0.10.0.*

### Bugs
- Fixed issue where the tutorial opponent would be QuickQuack instead of DemoDuck.


# Release 0.10.0 (15-12-2017)

### Gameplay
- When a player leaves a game in progress, they resign. Once resigned, a player can rejoin the lobby as an observer but can no longer win.

### Content
- Reworked the maps *toad1v1*, *spruce1v1*, *small1v1* and *oceanside1v1* to be all have the same number of starting City tiles, Town tiles and Rifleman units.
- In a lobby, it is now possible to change the AI and difficulty after adding an AI opponent.
- Updated both AIs slightly, mostly to respond to difficulty setting.

### Visuals & User Interface
- After a match has ended, a diamond icon pops up over each tile that is worth points.

### Bugs
- Fixed a bug where the camera would not always pan when Crops tiles generated income at night.
- Fixed bug where player ratings in the multiplayer menu would not always update.

### Technical
- Improved server responsiveness when a player joins a game in-progress.
- Reduced the size of the data sent by the server at the start of a game by about 40 percent.
- The game ceases drawing if its window is hidden or minimized. (**Issue #28**)


# Release 0.9.1 (07-12-2017)

### Gameplay
- After the game ends, the entire map is revealed to all players.

### Visuals & User Interface
- Added an extra bar with icons for each of the weather effects. These icons light up when that weather effect is active and show a tooltip explaining their effects when hovered.
- Made thermometer (temperature gauge) and hygrometer (humidity gauge) larger.
- Added tooltips to the various markings on the thermometer and hygrometer.
- The in-game chat box can now be clicked to activate it.
- Increased the visual difference between 1 stack of Gas and 2 stacks of Gas.
- Tweaked the colors of the Gunner's machine gun.

### Bugs
- Fixed a bug where the camera would not scroll down when the cursor was at the bottom of the screen on certain resolutions. (**Issue #24**)
- Fixed a bug where the cursor displayed a waiting animation at the end of a game.
- Fixed a bug where Industry tiles could lower the humidity of surrounding tiles below 35 percent.


# Release 0.9.0 (04-12-2017)

### Gameplay
- The **Town** tile replaces the Settlement tile. The Town tile can have up to 5 buildings, generates income and can produce Settler units, but cannot produce Rifleman units.
- Added the **Farm** tile. The Farm tile can produce Settler units and can turn all tiles around it into **Soil** tiles. In the growth phase, a Soil tile transforms into a **Crops** tile if the temperature and humidity support plant growth. The Crops tile is consumed in the night phase, generating 1 income for its owner and turning back into a Soil tile. Soil tiles and Crops tiles leave Dirt behind when destroyed.
- The Settler unit no longer builds Settlement tiles. Instead, it can settle either a Town tile, a City tile or a Farm tile.
- The City tile no longer generates income.
- Barracks and Industry tiles require nearby City tiles to grow, and thus no longer benefit from nearby Settlement/Town tiles.
- City tiles and other structure tiles now start with 1 power when they are created, instead of 0.
- Increased the cost of City tiles to 20, up from 10.
- Decreased the cost of Barracks and Industry tiles to 2, down from 5.
- Decreased the starting income to 20, down from 50.
- City tiles and other structure tiles now leave **Rubble** behind when destroyed, instead of Stone. Rubble cannot be built upon.
- Desert can no longer be built upon.
- Added **Ridge** tiles. Ridge tiles function the same as Mountain tiles except they are not as cold by default.
- In the spring growth phase, Grass no longer regrows from Dirt.
- Increased the maximum temperature at which trees and crops will grow to 39 degrees, up from 29 degrees.
- Reduced randomness in the starting values of temperature and humidity so they are more reliable.
- A Rifleman unit now always succeeds when capturing a tile, regardless of its size.
- When a tile produces a non-Settler unit, the tile now loses all of its power, not just 1.

### Content
- Reworked the maps *toad1v1*, *spruce1v1* and *small1v1* to be less cold and less humid by replacing some Water and Mountain tiles with Ridge tiles.
- Removed the maps *peaktorn1v1* and *snowcut1v1* from the map pool.
- Added the map **oceanside1v1**.
- Updated the AIs for new gameplay changes and wrote new one that farms (HungryHippo).

### Visuals & User Interface
- Added impact shake to various attacks and damage abilities.
- Added camera shake on various attacks and abilities.
- Improved timing of the Shell ability of Tank units with less than three tanks.
- Differences in grass color (caused by temperature or humidity differences) are now more distinct, which should improve their readability.
- Tweaked the colors of Dirt, Desert and Mountain tiles.
- When displaying simultaneous effects such as the hearts and coins at night, if not all effects fit on the screen at once, the camera will pan multiple times.

### Bugs
- Fixed bug where a player could appear to remain online indefinitely after their game crashed. (**Issue #25**)
- Fixed bug where the planning phase would last its entire duration even though both players were ready. (**Issue #27**)
- Properly fixed a bug where a figure could disappear before its death animation had finished.
- Fixed bug where Tank death animation would not play if the tank had just finished moving.
- Fixed bug where user's rating would not update in the UI after a game was over.
- Fixed bug where the multiplayer menu would be in an invalid state after returning to main menu and going back.
- Fixed minor bug where the chat indicatator would keep saying NAME after renaming lobby.


# Release 0.8.0 (23-11-2017)

### Accounts
- The game will ask you for a username the first time you log in with version 0.8.0 and automatically log you in with that username afterwards. To log in with that username on a different computer, you need to copy the *.acc* file from the *accounts* folder. To log in as a different user, you need to override the username in the settings.
- The server now tracks **rating points** for each player. All players start with 0 rating points. Every game you play causes you to gain rating points if the score you obtain at the end is higher than your rating, and lose points if your score is lower.

### Gameplay
- Tank units now deal trample damage to tiles when they move onto them, turning Grass to Dirt and destroying trees. A Tank unit with three tanks can even bring down buildings.
- Lowered default humidity from 65 percent to 55 percent.
- Lowered the maximum temperature at which grass and trees will grow from 39 degrees to 29 degrees.
- Stone tiles now cause residual global warming.

### Content
- Reworked the maps *toad1v1*, *peaktorn1v1*, *snowcut1v1*, *spruce1v1*, *small1v1* and the tutorial map, making them more compact and fixing the total number of Grass and Forest tiles on each map to be exactly 100.
- It is now possible to see and send 'All' chat in game as well.

### Visuals & User Interface
- Added title logo to the main menu.
- Added connection icon to the top right of the main menu that indicates whether the game is connected to the server and whether a patch is available for download.
- Added icons to indicate whether a user is in a lobby or in a game.
- Added an icon to indicate whether a lobby is private.
- Added tooltips to the phase icons and the order icons. (**Issue #22**)
- Tweaked how colors look at night.

### Bugs
- ~~Fixed a bug where a figure could disappear before its death animation had finished.~~
- Fixed a bug where night phase mood indicators (e.g. pink hearts) were not displayed in observer mode and replay mode.
- Fixed a bug where disconnected observers could not rejoin the lobby if it was private.

### Technical
- The game is now able to patch itself. If a patch is available, the connection icon in the top right of the main menu will show an exclamation mark. Clicking this icon will cause the game to download the necessary files. Once the download is complete, clicking the icon again installs the patch and restarts the game.
- In AI vs AI games and replays, the server now waits between action phases until all observers have finished animating.
- Improved the responsiveness of rejoining a match in progress.
- Improved the stability and responsiveness of replay mode.
- Improved resolution detection when resolution is not specified in the settings. (**Issue #23**)

### Other
- We now have a Discord bot that posts when users go online or offline.


## Hotfix 0.7.2 (07-11-2017)

*This is a server-only hotfix that is compatible with release 0.7.0.*

### Content
- Modified the tutorial map and AI to be less overwhelming.

### Bugs
- Fixed issue where replays were available before the match had finished.
- Fixed possible issue that could cause the game to crash when receiving multiple messages from the server simultaneously.


## Hotfix 0.7.1 (05-11-2017)

*This is a server-only hotfix that is compatible with release 0.7.0.*

### Bugs
- Fixed a bug where the player could spawn on the wrong side of the map when playing the tutorial online, which made it more difficult than intended.
- Fixed a bug where colors assigned to an AI player would be permanently unavailable after the AI player was removed from the lobby.


# Release 0.7.0 (04-11-2017)

### Content
- Removed singleplayer modes from the main menu.
- Tutorial mode can be accessed by clicking the "start tutorial" button once connected to the server.
- Added AI opponents. Once inside a lobby, add an AI player by clicking the blue plus and selecting "Add AI player". To remove them, click the blue dots and select "Remove AI player".
- Added observer mode. To turn a player into an observer, click the blue dots and select "Move to observers". To move them back, click the blue dots again and select "Move to players". Users that join a lobby after a match has already begun automatically become observers.
- Added replay mode. Click the "watch replay" button to create a Replay lobby.
- Added lobby privacy. Private lobbies cannot be joined by other users.
- New lobbies are now automatically assigned a name by the server, but can be renamed with the "rename" button.
- Separated "Lobby" chat from "All" chat. During matches "All" chat is disabled.
- Renamed *tiny1v1* map to *small1v1*.

### Visuals & User Interface
- Revamped the lobby screen.
- Added dropdown boxes for selecting map, planning time and player colors.
- Tweaked the style and colors of various interface elements.

### Bugs
- The game now no longer continues after a player has been declared victorious.
- Fixed visual issues when rejoining a match in progress.
- Fixed issue where tiles destroyed during combat would rebuild themselves at night.
- Fixed issue where new trees popped up either with a very large delay or with no delay at all.
- Fixed issue where clicking an interface element also caused units and interface elements behind it to be clicked.
- Fixed issue where the text of an interface element was drawn over an interface element in front of it.


# Release 0.6.0 (20-10-2017)

### Gameplay
- A Tank unit executing a Shell order now fires an additional volley after the first.
- Simplified the final score: each Grass and Forest tile is worth 1 point.
- Dirt, Desert and Mountain tiles are no longer considered natural when evaluating if the City tile gains power.
- Tile buildings can now be destroyed when taking lethal damage in a targeted damage step.
- Gas no longer hits tiles or lowers the hitpoints of tiles.
- Gas causes the humidity to drop by 10 percent after it spreads, but not below 39 percent.
- A ground unit that moves through snow has its movement speed slowed *by* 1, instead of *to* 1.
- A ground unit that moves *out of* a Trenches tile no longer has its movement speed slowed.
- A ground unit that moves *onto* a Trenches tile stops moving and becomes entrenched if able. If the moving unit is a Tank or would be bypassing a friendly unit, it can continue moving without being slowed.
- A ground unit that is attacked while moving out of a Trenches tile no longer benefits from the protection of the Trenches.
- A ground unit that is being attacked after performing a bypass attack from a Trenches tile does not benefit from the protection of the Trenches.

### Content
- Forest tiles now start with fewer trees.
- Added new map: **toad1v1**.
- Removed *twolakes1v1* from the map pool.

### Visuals & User Interface
- Improved animations when tiles are transformed or destroyed.
- Move guides now show how much the unit is predicted to be slowed by colorizing that many move guides blue instead of gray.
- It should now be more apparent when an order cannot be issued because the order limit has been reached.
- The mouse cursor is now always visible when hovering above a UI element.
- The camera can no longer fly too far beyond the edges of the map. (**Issue #6**)
- Fullscreen mode now forces native desktop resolution. (**Issue #19**)
- Chat text now wraps instead of extending past its container.
- Added a blinking caret to text input fields whose position is controlled by the left/right arrow keys.
- Added automatic horizontal scrolling to text input fields when the text gets longer than its container.

### Bugs
- Properly fixed issue where the camera would not pan when a zeppelin dropped gas.
- Fixed issue where the Quit popup was unresponsive if the chat window was open.

### Technical
- Added multithreading to prevent unresponsiveness while connecting to the server.

### Other
- Usernames are now required to be between 3 and 36 characters in length.


# Release 0.5.0 (16-10-2017)

### Content
- Made the tutorial AI produce weaker riflemen.
- Screen edge camera scrolling is now on by default.
- Camera scrolling options can be overridden in the settings.

### Bugs
- Fixed issue preventing 32-bit and OS X from connecting to the server. (**Issue #18**)
- Fixed errors preventing startup on OS X. (**Issue #17**)
- ~~Fixed issue where the camera would not pan when a zeppelin dropped gas.~~
- Fixed issue where figure footprint (selection circle) lingered after death.
- Fixed issue where the multiplayer menu was in a wrong state after the player left a match.

### Other
- Added these release notes.


# Release 0.4.4 (12-10-2017)

### Content
- Added a simple AI opponent for singleplayer. (**Issue #9**)
- Added a simple AI opponent for the tutorial.
- Added credits.

### Visuals & User Interface
- Changed the ready button checkbox.
- Changed font to Munro, which has a more permissive license.

### Bugs
- Changed all references from Aftermath (working title) to Epicinium.

### Other
- Hardcoded font into the binary.


# Release 0.4.2 (09-10-2017)
*First beta version.*
