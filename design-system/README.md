# Hum

Your own music, ready to play. Hum plays the mp3s on your iPhone. You import them from Files, make playlists, and listen with shuffle and repeat, even with the screen locked and without internet. It runs as a web app you add to the Home Screen.

## Principles

1. **Your music first.** The list is the app. Covers, titles and artists come from your own files, and you can rename them inside Hum without touching the file.
2. **Navy hero, light list.** A navy hero holds the screen title and the main actions. Songs sit below on a cool off white in white cards.
3. **Blue acts.** Electric blue is for actions, the playing song and progress. Coral only appears for removing things.
4. **Colour means something or nothing at all.** Covers without art all use one light blue placeholder, so no colour looks like it carries meaning.
5. **Same family as Stay Counter, Manna and Shuo.** The same type scale, layout rules, glass tab bar and iOS motion, with its own colour.

## Content

- Plain words, sentence case, short. No colons, semicolons or dashes in UI text. Song times are the one exception, like 3:05.
- A song without an artist says Unknown artist.
- Hum never changes the original file. Edit info says so.
- English only for now.

## Color

| Role | Tokens | Use |
| --- | --- | --- |
| Hero | `hero`, `hero-text`, `ring`, `deep` | Top of each tab, Now playing, the first open screen, behind an open sheet |
| Action | `primary`, `blue-text`, `soft` | Buttons, play, the add button, the playing row, the selected tab |
| Cover | `placeholder` | Songs and playlists without their own art |
| Ground | `bg`, `surface`, `line` | Screens, cards, dividers |
| Text | `ink`, `muted` | Titles and artists |
| Quiet | `chip`, `chip-text`, `chevron` | Round buttons, notes, the drag grip |
| Remove | `coral-text`, `coral-soft` | Remove from library, delete playlist, the minus in edit mode |

Rules
- `primary` is a fill. Blue text always uses `blue-text`.
- Text passes 4.5 to 1 wherever it sits, icons pass 3 to 1. The token notes list each pair.

## Typography

One typeface, Outfit, from Google Fonts. Six styles, two weights.

| Style | Size | Weight | For |
| --- | --- | --- | --- |
| `display` | 34 | Semibold | Screen titles in the hero, the first open headline |
| `player` | 28 | Semibold | The song on Now playing, the playlist name |
| `section` | 20 | Semibold | Section headers like All songs |
| `title` | 17 | Semibold | The playing song, buttons, sheet titles |
| `body` | 17 | Regular | Song titles in lists, fields, menu rows |
| `small` | 13 | Regular | Artists, times, counts, notes, tab labels |

Rules
- Only 400 and 600. Inside a list a title differs from the artist by size and colour, never by weight, except the playing song.
- Text inputs use 17, so iOS does not zoom.
- Large text uses minus 0.02em letter spacing. Times use tabular numbers.

## Layout

- Every screen and sheet uses a 22 side margin.
- The hero runs to the top edge under the status bar. Content starts 20 below it.
- Lists sit in one white card with a 1px `line` border and `radius-card`, rows split by hairlines. No shadows on the page.
- The app always fills the whole screen, down to the bottom edge, and lists leave room at the end so the last row clears the mini player and tab bar.
- Destructive actions always go last, as plain coral text, centered. They always ask first on a second screen.

## Navigation

- Two tabs, Songs and Playlists, in a floating glass pill at the bottom left. The round blue add button sits beside it and always means Import songs.
- The mini player floats above the tab bar while something is loaded. Tapping it opens Now playing.
- A playlist opens as a page that slides in from the right. Back is a round button top left, Edit top right.
- Settings sits behind the gear on Songs. It ends with About, where Design system opens this system inside the app.

## Sheets

- Sheets slide up and the page shrinks back and darkens behind them, like iOS.
- Top left leaves. × closes a first screen, ‹ goes back one step. Steps inside a sheet slide sideways.
- Every sheet closes with a swipe down from the top.
- The bottom holds one forward action, like Save or Done. Menus have none.

## Now playing

- A full navy sheet. Close at top left, the menu at top right, Playing from and the source in the middle.
- The big cover shrinks a little when paused.
- The progress bar is dragged or tapped to any point. Dragging to the end moves to the next song.
- Shuffle and repeat sit at the edges of the controls and turn `ring` blue on a soft pill when on. Repeat goes off, all, one.

## Lists

- Tap a song to play from that list. Hold a song for its menu, Add to playlist, Edit info, Remove from library.
- The playing song gets a `soft` row with `blue-text` and says Playing.
- In a playlist's Edit mode each row has a coral minus on the left and a grip on the right. Drag the grip to reorder. The row lifts with `shadow-lift`, the others slide aside, and the list scrolls near the edges.

## Iconography

- Line icons, round caps and joins, 24 grid, 2 line. Playback icons are filled.
- The mark is a closed smile and a music note in white on `primary`, like humming.

## Accessibility

- WCAG 2.2 AA. Targets are at least 44.
- Every icon button has a label. The drag grip says which song it moves.
- Motion stops when reduced motion is on.
