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


## Hotfix 0.7.2 (7-11-2017)

*This is a server-only hotfix that is compatible with release 0.7.0.*

### Content
- Modified the tutorial map and AI to be less overwhelming.

### Bugs
- Fixed issue where replays were available before the match had finished.
- Fixed possible issue that could cause the game to crash when receiving multiple messages from the server simultaneously.


## Hotfix 0.7.1 (5-11-2017)

*This is a server-only hotfix that is compatible with release 0.7.0.*

### Bugs
- Fixed a bug where the player could spawn on the wrong side of the map when playing the tutorial online, which made it more difficult than intended.
- Fixed a bug where colors assigned to an AI player would be permanently unavailable after the AI player was removed from the lobby.


# Release 0.7.0 (4-11-2017)

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
