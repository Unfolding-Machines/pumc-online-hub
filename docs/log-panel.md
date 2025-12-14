# Log Panel

The Log Panel is your adventure’s living journal. Write your descriptions and dialogue. Play results, oracle answers, dice rolls, add images and audio notes, and draw cards all land here in a scrollable timeline so you can replay, edit, or react to anything that happened during your session.

![log-panel](assets/screenshots/log-panel.png)

## Log File Manager
- Tap the header badge (the receipt icon + log name) to open the log selector dialog. Pick any log, rename it, delete an unused one, or add a fresh log so different scenes or campaigns stay organized.
- The dialog lists every log file, highlights the Main Log, and lets you rename, remove, or create logs without losing existing entries. Empty log slots show up immediately after creation.

![log-panel-files](assets/screenshots/log-panel-files.png)

To create a new log file, write a New log name and press "add". To switch to a different log file, just tap its name in the list.
To edit a log's name, tap the pencil icon beside it, change the name, and press "edit".

Considerations:

- Each game has one Main Log that can’t be deleted.
- Logs that contain plot beat advancements can’t be deleted to avoid losing story progress (you may undo the advancements first if needed).
- Organize the logs under your own naming scheme (e.g., by session date, scene name, or chapter, important event, world building, etc.).

## Playing Plot Beats (Random Prompts and Modified Proposals)
The app is conveniently setup to play Plot Unfolding Machine with ease, and the log panel has built-in buttons to help you generate story prompts and modified proposals on the fly.

![plot-beats](assets/screenshots/plot-beats.png)

Modified proposals invoke alterations to the current plot beat based on your input, while random prompts invoke a fresh prompt for you to draw inspiration from. Random prompts invoke Plot Nodes which you manage in the Plot Nodes panel (go to: [Plot Nodes](plot-nodes.md) to learn more).

Generated Plot Beats are added to the log as entries with a special highlight and an "Advance" button. When you confirm that a plot beat has occurred in your story, tap "Advance" to promote it to the active plot track. This helps keep your story organized and ensures that your plot progresses smoothly (go to: [Plot Tracks](plot-tracks.md) to learn more).

## Log area and log entries
- The scrollable timeline is built with the same entries you see in-game: text, answers, card art, shared images, oracle results, dice rolls, and snapshots of NPC portraits.
- Each entry can be tapped to open a simple viewer or the richer Visual Mode overlay, which stitches text, answers, and images into an animated highlight.
- Images and card art stay clickable; you can pin them to the board (Pin Cards), send cards to characters, or download attachments and audio clips directly from the entry’s context menu.
- Entries that represent candidate plot beats can be promoted so they join the active plot track, or rolled back if the plot changes.

## Entry Composer
- Tap or drag the portrait to the left of the composer to choose who is speaking; the same menu lets you pick a character from the cast or type a new “spontaneous speaker” name.
- Long-press the portrait to jump into that character’s detail view.
- The typing surface grows and shrinks as you drag the handle above it—expanded mode shows a formatting toolbar with bold, italic, headers, bullet/numbered lists, code blocks, and quick dice placeholders so you can style entries in Markdown-like notation.
- When the composer is compact, the send arrow button appears to the right; when the composer is tall, the send button sits beside the text field for more comfortable editing.
- The primary send button logs whatever text is in the field along with the selected speaker. Auto-formatting keeps numbered and bulleted lists going when you press Enter.
- Audio recording buttons are part of the composer: start recording to capture voice notes, stop to automatically attach the resulting audio file to a new log entry, and restart if you want to re-record.
- A drag handle above the composer lets you resize the input area so you can shrink it for more history or expand it when you want to write longer passages.

## Entry Actions (desktop context menu / long press)
- View opens the entry in Visual Mode or Image Viewer so you can re-read the text and examine attached art without leaving the timeline.
- Pin Cards keeps an image or card stack pinned to the board as an overlay for reference.
- Send Cards shares the card art from the entry to another character’s image gallery and opens their detail tab.
- Insert adds a new blank entry right after the selected one and begins editing automatically, so you can jot follow-up notes in position.
- Promote marks a user text entry as a confirmed plot beat (useful when you want to record something that drives the plot forward).
- Copy copies the entry’s speaker, title, text, and answer so you can paste it elsewhere.
- Edit/Describe switches the composer into edit mode for that entry; a warning dialog protects any text you already have in the composer from being overwritten.
- Reroll fires up the original oracle or dice roll so you can try again; Download lets you save attached audio or image files to disk.
- Rollback undoes a confirmed plot entry if the plot track hasn’t advanced yet, and Delete removes an entry entirely (audio files tied to it are also cleaned up).

## Dice Roller
- Enable the Dice Roller under Settings → Log Area to show a familiar roller widget under the timeline. Dice results get logged automatically with optional roll-detail counts if that setting is active.

## Log Area Settings
Adjust these toggles via Settings → Log Area to tailor the panel:
1. **Show Word Count** – Displays live word counts for the composer.
2. **Show GM Portrait** – Displays the GM avatar alongside game-master entries.
3. **Show Character Portraits** – Shows character portraits by each entry when available.
4. **Show Timestamps** – Adds timestamps to each entry in the timeline.
5. **Use 24h Timestamp** – Switches timestamps between 12h and 24h format.
6. **Show Section Titles** – Displays section headings when the plot track inserts them.
7. **Confirmed Plot Beats** – Shows/hides the “Advance” cue that promotes relevant entries.
8. **Show Dice Roller** – Toggles the roller widget below the timeline.
9. **Include Roll Details** – Appends formulas and dice details to each dice-roll entry when enabled.

## Tips
- Use the log to track both story beats and mechanical outcomes (dice rolls, oracle answers, cards dragged in from quests).
- Regularly review the timeline in focus mode to see which plot beats are still waiting for confirmation and which have already advanced.
- The panel auto-saves and keeps your audio/image attachments safe, but you can download or pin anything you need for later reference.
