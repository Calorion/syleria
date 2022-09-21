---
{"dg-publish":true,"permalink":"/garden/obsidian-daily-note-readme/","dgHomeLink":false,"dgPassFrontmatter":false}
---


[Obsidian Daily Note](https://routinehub.co/shortcut/12864/) Readme
======

Obsidian Daily Note by Jim Syler
@Calion

View this readme online: <https://syleria.netlify.app/garden/obsidian-daily-note-readme/>

This shortcut creates a new daily note with metadata in Obsidian.

The reason a shortcut is necessary is that Obsidian currently has [no way to import GPS data](https://forum.obsidian.md/t/mobile-can-obsidian-api-provide-current-geo-location-gps-on-android-ios/21638).

Features
---------
- Creates a daily note in Obsidian with location and date/time information in the frontmatter. If invoked again the same day, will open the same note, adding a timestamp. If dated note is renamed, will create a new note
- Automatically folds the frontmatter if the [Advanced URI plugin](https://vinzent03.github.io/obsidian-advanced-uri/actions/commands) is installed
- If the [Obsidian Leaflet](https://obsidian.md/plugins?id=obsidian-leaflet-plugin) plugin is installed, creates a Note info callout with metadata and a map
- Creates a map of all your journal entries if you have Leaflet installed

### Hidden preferences
Note: Any changes to hidden preferences must be reset after every update.
- If you would like more accurate but slower location data, including the addition of altitude data to your notes, set “Precise location" in the Dictionary above to True.
- If you want to receive beta versions of this shortcut, change the value for “Beta versions” in the Dictionary above to True. You will have to do this for every new non-beta version. Note that at this time, changing it back to False will *not* cause it to revert to the last stable version.
- RoutineHub has been having server issues, so checking for updates has occasionally been very slow. If you wish to disable version checking, set "Version check" in the Dictionary above to False.

Info
----
- There is an update mechanism included. Updating is always optional; you will be asked whether you want to update or not. The update mechanism is harmless, and cannot damage your system; it checks to see if there is an update available, and then optionally prompts you to download it from Apple’s Shortcuts Gallery. For more info, visit the [UpdateKit home page](https://www.mikebeas.com/updatekit-api/). If for any reason you are uncomfortable with the included update mechanism, simply delete the action titled “If Current IP Address has any value,” and respond with “Delete Actions” in the subsequent dialog. You can then Favorite the shortcut at [RoutineHub](https://routinehub.co/shortcut/12864/) to get notifications of new versions.

- Latest version always available at <https://routinehub.co/shortcut/12864/>

- If this has been helpful to you, feel free to [buy me a coffee!](https://www.buymeacoffee.com/calion)

- Please report any bugs in a comment on [RoutineHub](https://routinehub.co/shortcut/12864/) or on [Twitter](https://twitter.com/intent/tweet?text=@calion%20Re%20%20Obsidian%20%20Journal%20%20Entry%3A).

### Known bugs
- [ ] Insertion point does not appear at bottom, ready to create entry (possibly fixable with Templater. Perhaps I should split the input between the shortcut and a template. I could even have the shortcut create the template on first run)
- [ ] When you change the title of a note, the link in the Note info callout doesn’t change. This is an issue with Leaflet, which I cannot fix.

~~There are no immediate plans to fix these bugs, so if any of them are bothering you, let me know via the links above!~~

### Proposed features
- [ ] Various options for how you want your entries formatted
- [ ] Use Dataview to keep tags in frontmatter but display in Note info callout
- [ ] Allow user to select a custom note title at runtime (probably not going to do this given the Daily Notes format. Indeed, perhaps I should rename the shortcut)
- [ ] Prompts user to buy the developer a coffee after every 10 launches
- [ ] Put insertion point at end of file on creation ("Journal/log workflow" does this)
- [ ] Location data in timestamps? Maybe city/State?
- [ ] Persistent preferences using a JSON file in the Shortcuts folder. Looks like I can set my own first-run prefs this way using menus and such. If you do this, maybe set a true/false pref in Import Questions to make it easy to reset them.
- [x] Don’t check location if simply adding to a Daily Note. This unnecessarily slows down the shortcut (unless we want to add location metadata to the entries? Maybe just *disable* the location checking, instead of moving the whole thing above it, if the file already exists, to make future customization easier)
- [ ] Before "1.0" release (should have made these "0." releases):
	- [ ] Fix insertion point issue (maybe just invoking the keyboard would be sufficient?)
	- [ ] Improve timestamp format (right now it’s not a header or anything. Investigate Daily Notes formats)
	- [ ] Implement nagware function
- [ ] Full Daily Note functionality. Integrate with Obsidian Daily Notes function. How:
	- [x] Rename Shortcut "Daily Note"
	- [ ] Auto-create "Daily Note" template in Obsidian/Templates (what if it collides with an existing note?), and have shortcut open it in Obsidian, if it doesn’t exist
	- [ ] Populate template with `[Create new daily note](shortcuts://run-shortcut?name=[Daily Note])` and instructions (in a Markdown comment?) for how to turn on the Daily Note core plugin, set this as a Daily Note template, and delete these instructions (in the template!). Mention to leave the Date field blank.
	- [ ] Change Shortcut to auto-delete (or replace) a file with the same name it wants to use (i.e. today’s date) and "[Create new daily note](shortcuts://run-shortcut?name=[Daily Note])" plus a blank line.
- [ ] If I ever go to asking the user for a title, if there’s a collision, ask whether to append or rename
- [ ] Make and release a fork of Linter that will put the title after the Note Info
- [ ] Suggest users use [Frontmatter Tag Suggest](https://obsidian.md/plugins?id=obsidian-frontmatter-tag-suggest) since tag entry is now in frontmatter

If any of these features appeal to you, let me know via the links above!

### Similar products
- [Journal/log workflow – Drafts-like “just start writing” for your daily notes (iOS)](https://forum.obsidian.md/t/journal-log-workflow-drafts-like-just-start-writing-for-your-daily-notes-ios/18382)

Let me know if you’re aware of other products that should go here.

### Credits
- Contains actions from [UpdateKit API Example](https://www.mikebeas.com/updatekit-api/v1)
- Contains actions from [Save and retrieve API Key](https://www.reddit.com/r/shortcuts/comments/ajdq6d/data_storage_part_1_storing_simple_values/)

## Version History

### 2.0.0b (2022-09-03)
#### New features
- Changed to permanent local storage for preferences, enabling much more customization going forward [in progress]
- Implemented nagware function (hey, I worked hard on this!) [in progress]
- Improved timestamp format [in progress]
- Changed name from “Journal Entry” to "Daily Note”

#### Bug fixes
- Fixed insertion point issue; note is now instantly ready to type on [in progress]
- Moved tags to frontmatter where they belong

### 1.3.1 (2022-09-03)
#### Bug Fixes
- Eliminated unnecessary slowness when adding timestamps to daily notes
- Vastly sped up note creation by checking location faster but less accurately, and with no altitude data (added a hidden preference to go back to the old, slow way with altitude)

### 1.3.0 (2022-09-02)
#### New Features
- Centers link to overall map
- Allows custom journal folder
- Note name is now date only; if invoked on the same day, will add timestamp. If note title has been changed, will create new note with date as title

### 1.2.0 (2022-09-01)
#### New Features
- Auto-creates map of all notes in Journal folder on startup, and checks for it every time
- Adds link to overall map to every note

### 1.1.2 (2022-08-31)
#### Bug Fixes
- Hotfix for missing import question

### 1.1.1 (2022-08-30)
#### Bug Fixes
- Hotfix for version number error

### 1.1.0 (2022-08-30)
#### Bug Fixes
- Opens Obsidian earlier in the process, so the note will open more reliably
- Added a “Version check?” toggle to turn off version checking, as a hack around the fact that Routinehub is so slow.
- Fixed the first tag not registering as a tag (added a space before the hashtag)

#### New Features
- Changed icon
- Creates note with Note Info but no map if Leaflet is not installed
- Automatically fold the frontmatter if the [Advanced URI plugin](https://vinzent03.github.io/obsidian-advanced-uri/actions/commands) is installed

### 1.0.0 (2022-08-23)
- Initial release, inspired by <https://forum.obsidian.md/t/mobile-can-obsidian-api-provide-current-geo-location-gps-on-android-ios/21638>

#### New Features
- Creates a new journal entry in Obsidian with location and date/time information in the frontmatter.
- If the [Obsidian Leaflet](https://obsidian.md/plugins?id=obsidian-leaflet-plugin) plugin is installed, creates a Note info callout with metadata and a map

updated: 2022-09-21T12:23:20-05:00
