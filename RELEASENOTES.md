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
- Fixed issue where the camera would not pan when a zeppelin dropped gas.
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
