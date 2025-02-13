Fire comment
2 comment 2
3 comment 3
4 comment 4
5 5ccc
hrhfdfgdfgfghfghfg
5544
55555555555
gdfgdfgdfgdrgdf
dsfsdfsdf sdf sd fsd 
6667

2222
fgdhfghfgh fgh fghfgh

- [x] Extract Preloader component (get from public/index.html)
- [x] Remove dynamic layout
- [x] Create script for generating media queries for game page
      Search: Does media query include scrollbar? Actually, the whole point is to avoid a scrollbar
- [x] Design game UI screens (new game, pausing)
- [x] Add user list to GamePanel
- [x] Design new game state (with Flow types)
  - [x] Put `curUser` in Redux state
  - [x] Derive playing state from `users(status=playing).len`
- [x] Add missing screens for multiplayer flows
- [x] PIVOT: Turn collaborative Flatris (2-8 players) into competitive 1vs1 Flatris
  - [x] Redesign state and actions
    - [x] Make MOVE, ROTATE, ENABLE_ACCELERATION, DISABLE_ACCELERATION userId based
    - [x] Cancel ADVANCE loop on unmount
    - [x] Disable acceleration on line drop
    - [x] ADVANCE action for current user
    - [x] Remove START/STOP actions
  - [x] Clear onboarding screens (postpone UI this time until game mechanics are confirmed)
  - [x] Update fixtures and tests
  - [x] Add 2nd player
    - [x] Start game when both players are ready
    - [x] Render other player's grid in the background
- [x] Create server MVP database
  - [x] Split client logic between starting or joining a game
- [x] Rename state.game to state.curGame
- [x] Add blocks to other player when clearing lines
- [x] Bring back "falling" block transition when lines are cleared
- [x] Transitions when clearing lines
  - [x] Cleared lines should go down (not instantly disappear)
  - [x] Lines from enemy should come up (not instantly appear)
  - [x] getNextCellId(gameState) abstraction
- [x] Fix concomitant line clearing between players
  - [x] Fix multiplayer test case: Clearing lines that aren't bottom ones
- [x] Expand memory db to multi games
- [x] Green/red wall flash when clearing lines (own vs enemy)
- [x] Earthquake effect when clearing lines
- [x] Make enemy grid visible on Firefox
- [x] Add hidden keyboard shortcut for stopping game
- [x] Clean up server scripts (Keep server with client together in prod, separate in dev)
- [x] [WORKING PROTOTYPE]
- [x] Handle wrong game ID with 404
- [x] Create server-side user sessions
- [x] Read game (Redux) state from server side in Page.getInitialProps
- [x] Use HTTP request instead of socket event to create game
- [x] Load entire game state on load
- [x] Don't join game if 2 players are already in
- [x] Create join/:id route
- [x] Turn sessionId, userId & gameId numbers into hashes
- [x] Grayscale loading state until JS is loaded
- [x] Subscribe to game events on game page, once JS is loaded
- [x] Continue game after hard refresh
- [x] Add fixtures for all components
- [x] Add disabled state to buttons (get rid of early exists in handlers)
- [x] Create "Invite or play" screen
- [x] Create "Game full" screen
- [x] Create "Join game" screen
- [x] Create "Get ready" screen
- [x] Create "Waiting for other" screen
- [x] Create "Game over" screen
  - [x] Allow players to restart once game is over
- [x] Different layouts per device type/orientation
  - [x] No controls on desktop
- [x] Drop Tetromino on SPACE key
- [x] Style "Auth" screen
  - [x] When joining
  - [x] When creating
  - [x] Restrict name length
- [x] Reuse old public assets
  - [x] Add meta tags from old index.html
- [x] Style GamePanel
  - [x] Show both players' score in game panel
  - [x] Show player READY state
  - [x] New Flatris logo
  - [x] Humanize numbers over 1K
  - [x] Show lines instead of "wins" for single player
  - [x] Make "2P insert coin" clickable
- [x] Add global score (how many games each player won)
- [x] Add ability to PING other player
- [x] Allow users to just watch
- [x] Onboarding screen
  - [x] Left, right, up, down & space keys for desktop
  - [x] Point to controls
  - [x] Explain Flatris invention: line transferring
- [x] [ALPHA TESTING] feedback
  - [x] Disable in-game auth after entering 1st time
  - [x] Fade in game screens
  - [x] Generate new Tetromino random sequence per game turn
  - [x] Improve ending UI: Add WON green badge under player name
    - [x] Regression: Change "WON" badge to not block user score
- [x] Encourage players to play "best x out of y"
- [x] Disable controls when user isn't playing
- [x] Side controls on landscape mobile
  - [x] Extract portrait controls out of FlatrisGame
- [x] Don't request user auth when game is full (allow guests to watch)
- [x] Add copy to clipboard btn to "Invite or play" screen
  - [x] Show share button when clicking on "2P insert coin"
- [x] [BEAUTIFUL MVP]
- [x] Ensure action consistency
  - [x] Create action backfill if user has old state and new actions
    - [x] Create action.id, action.prevId and game.player.lastActionId
    - [x] Store actions on the server
    - [x] Create backfill operation
- [x] UX: Disable Auth buttons while performing IO
- [x] UX: Disable buttons while JS is loading
  - [x] 2P Insert Coin in GamePanel
  - [x] screens/Auth name field
  - [x] screens/GameFull Watch
  - [x] screens/GameOver Again
  - [x] screens/GetReady Ready
  - [x] screens/JoinGame Watch and Join
  - [x] screens/NewGame Play and Copy
  - [x] screens/WaitingForOther Ping
- [x] Add pause & end game state for solo players with invite screen
- [x] Index page
  - [x] Create reduxState.games
  - [x] List all games
  - [x] Beautiful grid
  - [x] Animating games
  - [x] Strip game effects when going back to index page
  - [x] Push new games to dashboard
  - [x] Remove inactive games
    - [x] Mark inactive after 30 seconds
    - [x] Remove expired after 15 minutes
    - [x] Redirect to dashboard from expired game page
  - [x] Style
    - [x] Style NEW GAME button
    - [x] Add Flatris header
    - [x] Show blank state when no active games exist
    - [x] Fade in fade out transition game previews
    - [x] Highlight already joined games
- [x] BUG: Broadcast new game to `global` (without requiring an action)
- [x] BUG: Reset losses when 2nd player joins
- [x] Minimize network communication: Don't send noop actions
- [x] Throttle key down events
- [x] Profile browser performance (detect unnecessary renders)
- [x] Redesign onboarding
  - [x] Screen 1: Game intro
  - [x] Screen 2: Multiplayer game
  - [x] Screen 3: Line transferring
  - [x] Screen 4: Controls
- [x] Custom 404 page
- [x] Error page (via componentDidCatch)
- [x] Add empty game shell to Dashboard blank state
- [x] Link to Github
- [x] Game footer
- [x] Disable active Tetromino movement when game over (via mobile buttons)
- [x] [1.0]
  - [x] Merge to master
  - [x] Rollbar server
  - [x] Rollbar client
  - [x] https://flatris.space
- [x] Embed Teko font in JS bundle
- [x] Record stats
  - [x] Store in Firebase (users, games)
  - [x] Count Turns and lines
  - [x] Count actions (left, right, accelerate, rotate)
  - [x] Count time
- [x] BUG: Gracefully invalidate session after re-deploy
- [x] Sync game after player disconnect
- [x] Real time stats page
- [x] [2.0]
  - [x] Share on HN, PH, Reddit, etc
- [ ] Fix: Polyfill Set/Map https://reactjs.org/docs/javascript-environment-requirements.html
- [ ] Increase speed logarithmically (game currently ends too abruptly)
- [ ] "Paused" state for solo players (useful in dashboard to see if person paused or disappeared)
  - [ ] How about "idle" state?
- [ ] Ask for permission to join game
  - [ ] "Waiting for permission..." screen
  - [ ] "Allow player to join?" screen
  - [ ] "Denied" screen
- [ ] End of game screen

BACKLOG

- [ ] Back/home button in end game screen
- [ ] Allow watcher to select current player
  - [ ] Show current player visually
- [ ] Don't show onboarding after every deploy
- [ ] Freeze game on player disconnect
- [ ] Create drop shadow from active Tetromino
- [ ] Draw game status
- [ ] Zoom in animation when opening game from dashboard
- [ ] Algorithm for dispatching bundled actions at time interval
- [ ] Sounds

PERF

- [ ] Separate client from server (and run multiple instances of client)
- [ ] Minimize state footprint
- [ ] Batch dashboard actions

CHORES

- [x] Upgrade to Babel7
- [ ] Extract ReduxActions Cosmos proxy

UX

- [ ] Reconnect when focusing idle tab (https://github.com/socketio/socket.io-client/issues/1067)
