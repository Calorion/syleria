---
{"dg-publish":true,"permalink":"/garden/obsidian-clipper-readme/","dgHomeLink":false,"dgPassFrontmatter":false}
---

[Obsidian Clipper](https://routinehub.co/shortcut/11156/) Readme
======

Obsidian Clipper by Jim Syler
@Calion

This shortcut takes input from the share sheet and imports it into the Obsidian app.

In principle, it will accept any input. In practice, some formats will work better than others. If you run into formats it handles poorly, leave a comment on the RoutineHub page linked below.

Features
---------
- Saves entire web pages, not just URLs
- Optionally appends input to existing note (especially useful for images!)
- Embeds YouTube videos
- Handles rich text
- Imports Evernote notes

### Hidden preferences
Note: Any changes to hidden preferences must be reset after every update.

- If you want to receive beta versions of this shortcut, change the value for “Beta versions” in the Dictionary above to True. You will have to do this for every new non-beta version. Note that at this time, changing it back to False will *not* cause it to revert to the last stable version
- If you wish to disable version checking, set “Version check" in the Dictionary above to False

Info
----
There is an update mechanism included. Updating is always optional; you will be asked whether you want to update or not. The update mechanism is harmless, and cannot damage your system; it checks to see if there is an update available, and then optionally prompts you to download it from Apple’s Shortcuts Gallery. For more info, visit the [UpdateKit home page](https://www.mikebeas.com/updatekit-api/). If for any reason you are uncomfortable with the included update mechanism, simply delete the action titled “If Version check is Yes” and respond with “Delete Actions” in the subsequent dialog. You can then Favorite the shortcut at [RoutineHub](https://routinehub.co/shortcut/11156/) to get notifications of new versions.

Latest version always available at <https://routinehub.co/shortcut/11156/>

 If this has been helpful to you, feel free to [buy me a coffee!](https://www.buymeacoffee.com/calion)

 Please report any bugs in a comment on [RoutineHub](https://routinehub.co/shortcut/11156/) or on [Twitter](https://twitter.com/intent/tweet?text=@calion%20Re%20Obsidian%20Clipper%3A%20).

### Known bugs and limitations
- [ ] Text containing links to YouTube videos will not import as text, but as a YouTube video
- [ ] Webpage images behind relative links do not show up
- [ ] Shows up for—but does not successfully import—iPadOS screenshots
- [ ] Web article headings show webpage title, not the heading seen in Reader. This is a bug in Shortcuts; [reported](https://openradar.appspot.com/radar?id=5627250862981120)
- [ ] Cannot support `blob:` URLs
- [ ] Evernote notes imported from Evernote’s “Export note” function do not include links to the original Evernote note
- [ ] Evernote formatting is not as good as it could be. The current method should be redone using XML parsing

There are no immediate plans to fix these bugs, so if any of them are bothering you, let me know via the links above!

### Proposed features
- [ ] Add “archive article” option (or its own shortcut), which will take the Reader view of a Web article and import it to Obsidian, with *saved* images (hopefully missing ads), and the link to the original on top, to have a publishable archive of linked articles. Perhaps this should be the default saved webpage option. Alternately, support Web Archives, and write a plugin to get Obsidian to [recognize them](https://forum.obsidian.md/t/render-webarchive/17833) (for 3.0 release)
- [ ] Sticky preferences: Beta versions, do not open Obsidian (for 3.0 release)
- [ ] Support “File” filetype, e.g. Pages files
- [ ] Create button for user to open result in Obsidian, or not
- [ ] Prompt user to buy the developer a coffee after every 10 launches, with “not right now” and “never ask me again” options (for 3.0 release, but disable in beta)
- [x] Open Obsidian early to ensure notes open properly
- [x] Ask every time what folder to put it in (for 3.0 release)
- [ ] Ask for new note or append earlier, so user can ignore until it’s done (for 3.0 release)
- [ ] You can get the selected text from the Get Details of Safari Web Page action! I gotta use that somehow
- [ ] Pop up a multiple-choice menu asking for clipping options: Append, tags, notes, show result in Obsidian, etc. Then have successive screens depending on the options chosen (for 3.0 release)
- [x] Change documentation format to Markdown and reformat per my Daily Notes shortcut. Also remove periods at the end of bullets
- [ ] Advertise my other shortcuts in the readme (for 3.0 release)
- [ ] Advertise in the forums listed in Similar Products
- [ ] Upload shortcut to other services (and then largely ignore, trusting the update mechanism)
- [ ] Add option in beta versions to revert to last stable version (link will have to be manually input for every new stable), along with an explanation that it’s a beta, and you’re expected to test and report bugs (for 3.0 release)
- [ ] Go over whole Shortcut (for 3.0 release)
- [ ] Add “Link only” to Web and YouTube (and, hell, Evernote) options. Yes, the Obsidian share sheet extension can already do this better, but why have to switch between? (for 3.0 release)
- [ ] Add support for Evernote tasks
- [ ] The ability to import Evernote files from the app instead of from ENEX files may go away at some point, as I don’t want to have to support two different methods, and this way is largely inferior (the only reason this function exists at all is that I had already written it before I discovered that exporting ENEX files was possible on mobile).
- [ ] Separate prefs and info dicts, as in Daily Notes (for 3.0 release)
- [x] Switch bugs and features in the readme
- [x] Move readme online entirely, just keeping basic info that won’t change in the Shortcut?
- [ ] Show full documentation on first run (and how to find it again)
	- Nice example documentation in the BART shortcut
- [ ] Have a way to permanently exclude folders from the list that appears when you choose New File. 
- [ ] Consider including the Evernote link for Evernote notes. This will be involved and kind of hacky, as it’s got to search for the note name in Evernote. Luckily I already created the mechanism to do so, but it’s kind of cumbersome for the user. I’ve also considered writing a separate shortcut for this purpose

### Similar products
- [MarkDownload](https://forum.obsidian.md/t/markdownload-markdown-web-clipper/173)
- [Obsidian Web Clipper](https://forum.obsidian.md/t/obsidian-web-clipper-bookmarklet-with-full-markdown-support-for-images-headings-and-code-blocks/22068)
- [Built-in Share Sheet extension](https://discord.com/channels/686053708261228577/694235607810965636/983742187869188146)
- Other options are discussed at [How do I get content from websites into my notes?](https://forum.obsidian.md/t/how-do-i-get-content-from-websites-into-my-notes/1738)

Let me know if you're aware of other products that should go here.

### Credits
Contains actions from:
- [UpdateKit API Example](https://www.mikebeas.com/updatekit-api/v1).
- [Translated Data Types](https://www.reddit.com/r/shortcuts/comments/c1eg61/)
- [Saveit](https://talk.automators.fm/t/help-with-shortcut-to-save-webpage-as-your-chose-of-webloc-webarchive-or-pdf/7180/2)
- [XML to JSON Converter](https://routinehub.co/shortcut/678/)
- [Dictionary all values example](https://www.reddit.com/r/shortcuts/comments/cx5xjc/working_with_dictionaries/)
- [Dictionary keys and values example](https://www.reddit.com/r/shortcuts/comments/cx5xjc/working_with_dictionaries/)
- [Remove JSON value by key](https://www.reddit.com/r/shortcuts/comments/akn3k0/data_storage_part_3_removing_stored_values/)

## Version History

### 3.0.0-b.1 (2022-04-21)
#### New Features
- Imports images from webpages, creating a permanent archive. This is the default behavior, though there is a preference to turn it off. [In progress]
- Adds Evernote support
- Adds runtime options to import Web pages as Markdown, HTML, or PDF
- Adds frontmatter indicating the origin of the clip, date created, and possibly other info [In progress]
- Adds image support
- When New File is chosen, images and photos will be imported into a new Note, not merely placed in the Attachments folder
- Changed name from “Save to Obsidian” to “Obsidian Clipper”
- Asks what folder to save new clips in
- Full readme file moved to https://syleria.netlify.app/garden/obsidian-clipper-readme/, leaving a stub in the Shortcut

#### Bug Fixes
- Removed slashes from filenames, which caused files to be created in subfolders [in progress (or not)]
- Fixed issues caused by inputs having multiple data types. User will now be asked to choose which to use
- Errors out on `blob:` URLs rather than failing silently
- Improved handling of Internet connection check
- Fixed an issue where clips with the same name as an existing file would be appended to the existing file
- Opens Obsidian earlier to help ensure notes open correctly

### 2.1.0 (2022-03-30)
#### New Features
- Saves web pages as Reader articles
- Added ability to opt in to beta versions

#### Bug Fixes
- Now works in any language
- Accepts unsupported file types
- Opens correct file if appended to a nested file

### 2.0.1 (2022-03-29)
#### Bug Fixes
- Fixed shortcut name and beta status

### 2.0.0 (2022-03-28)
#### New Features
- Option to append to existing note (especially useful for images!)

#### Bug Fixes
- Doesn’t fail if there’s no Internet connection

### 1.5.2
#### Bug Fixes
- Fixed version checking error

### 1.5.1
#### Bug Fixes
- Can handle filenames with periods (I’m a little concerned that this will cause other files not to automatically open in Obsidian—I had left the extension off the link for a reason—, but it works in my testing so far)

### 1.5.0
#### New Features
- Built-in update checking with [UpdateKit API](https://www.mikebeas.com/updatekit-api/v1)

#### Bug Fixes
- Fixed error in duplicate handling mechanism (Shortcuts doesn’t need the period when it looks for file extensions; doh!)
- Now can handle Markdown files! (doh again!)
[These bugs were fixed in 1.5, but not included in the release notes on Routinehub until 1.5.1, because I wanted to test the new update mechanism. And then I found another bug anyway ¯\_(ツ)_/¯]

### 1.4.2
#### Bug Fixes
- Treats images from Web browsers as images, not Web pages

### 1.4.1
#### Bug Fixes
- Treats text not from YouTube app as text, not URL

### 1.4.0
#### New Features
- Embeds YouTube videos

#### Bug Fixes
- No longer fails when trying to save with the same filename as an existing file

### 1.3.0
#### New Features
- Handles rich text

### 1.2.0
#### New Features
- Handles Web pages from URL
- Launches resulting file in Obsidian

### 1.1.1
#### Bug Fixes
- Fixed lack of input options

### 1.1.0
#### New Features
- Adds photo support

### 1.0.0
- Initial release, inspired by <https://forum.obsidian.md/t/feature-ios-share-sheet-extension/14873/>
