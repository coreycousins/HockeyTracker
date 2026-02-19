# Hockey Tracker v1.7

A mobile-optimized puck possession and shot tracking app for youth hockey teams. Track individual player possession times, shots on goal, and goals during live games with detailed touch-by-touch analysis and video reference timestamps.

## Features

- **Real-time Possession Tracking**: Tap players to track possession during live games
- **Shot & Goal Tracking**: Long-press to record shots, double-tap to record goals
- **Defense Line Quick Selector**: Fast access to active defense pairs
- **Period Management**: Track across all 3 periods with per-period breakdowns
- **Game History**: Save and review past games with persistent storage
- **Video Reference Timestamps**: Correlate possession, shot, and goal data with game video
- **Roster Swap**: Tap-to-select-and-swap players between lines, positions, or within the same line in Edit Roster
- **In-Game Line Editing**: Adjust lines mid-game without ending the game — tap "Edit Lines" to swap players between lines, then "Done Editing" to resume tracking
- **Persistent Roster**: Roster changes made in Edit Roster (names, numbers, line/position swaps) auto-save to localStorage and persist across sessions. In-game line edits do not affect the saved roster
- **Overall Stats**: View aggregate possession, shots, and goals across all saved games with per-game averages and CSV export
- **Delete Confirmation**: Confirmation dialog before deleting historical game reports
- **CSV Export/Import**: Export detailed reports including shot/goal events for analysis
- **Mobile Optimized**: Designed for iPhone use during games

## Quick Start - GitHub Pages Deployment

1. **Create a new repository on GitHub**
   - Go to https://github.com/new
   - Name it `hockey-tracker` (or any name you prefer)
   - Set to **Public**
   - **DO NOT** initialize with README, .gitignore, or license
   - Click "Create repository"

2. **Upload the files**
   - On your new repository page, click "uploading an existing file"
   - Drag and drop `index.html` and this `README.md`
   - Scroll down and click "Commit changes"

3. **Enable GitHub Pages**
   - Go to your repository Settings (gear icon at top)
   - Click "Pages" in the left sidebar
   - Under "Source", select "main" branch
   - Click "Save"
   - Wait 1-2 minutes for deployment

4. **Access your app**
   - Your app will be live at: `https://YOUR-USERNAME.github.io/hockey-tracker/`
   - Bookmark this on your iPhone home screen for easy access

## Development with Claude Code

Once your repository is set up:

```bash
# Clone your repository
git clone https://github.com/YOUR-USERNAME/hockey-tracker.git
cd hockey-tracker

# Open with Claude Code
claude-code .
```

Then you can:
- Ask Claude Code to make changes
- Test locally by opening index.html in a browser
- Push changes to GitHub (they'll auto-deploy to your live site)

## Usage

### Editing the Roster
1. From the home screen, tap "Edit Roster"
2. Edit player names and numbers directly in the input fields
3. To move players between lines/positions: tap a player to select them (highlighted in cyan), then tap another player to swap their positions
4. Players can swap across lines, across positions, or within the same line (e.g., swap two forwards on the same line to reorder them)
5. Tap "Done" when finished

### Starting a Game
1. Enter opponent name
2. Click "Start Game"
3. Select active defense line using quick selectors
4. Tap player buttons to track possession

### During Game
- **Single tap**: Start tracking possession for that player
- **Tap again**: End possession (creates a "touch")
- **Different player tap**: Switches possession
- **Long-press (~500ms)**: Record a shot on goal (yellow flash)
- **Double-tap (<300ms)**: Record a goal (amber flash, also counts as a shot)
- Active player shows in green with live timer
- Shot/goal counts displayed on player buttons (S:# G:#)
- **Edit Lines**: Tap "Edit Lines" to enter swap mode — tap a player (cyan highlight), then tap another to swap their lines. Tap "Done Editing" to resume possession tracking. Possession timer pauses automatically while editing.
- Use "Next Period" button between periods
- Use "End Game" when finished

### After Game
- Review possession statistics sorted by total time
- View shots, goals, and shooting percentage per player
- Expand players to see timestamped shot/goal events and possession touches per period
- Add video reference time (HH:MM:SS format)
- Export CSV for detailed analysis
- CSV includes shot/goal details and video timestamps when reference time is set

### Game History
- View all saved games
- Click any game to review stats
- Delete old games with confirmation prompt
- Import CSV files from other devices

### Overall Stats
- From History, tap "Overall Stats" to view aggregate data across all games
- Team summary shows total and average possession, shots, goals, and shooting %
- Per-player stats separated by forwards and defence, sorted by possession
- Shows games played, totals, and per-game averages for each player
- Export overall stats to CSV

## Data Storage

Game data and roster changes are stored in your browser's localStorage:
- Data persists between sessions
- Tied to the specific browser/device
- Not synced across devices
- Export CSV to back up or share data

## Browser Compatibility

- iOS Safari: ✅ Full support
- iOS Chrome: ✅ Full support
- Desktop browsers: ✅ Works but optimized for mobile

## Future Development Ideas

- Multiple team rosters
- Line combination analysis
- Real-time game clock
- Plus/minus tracking

## License

MIT - Feel free to modify and use for your team!
