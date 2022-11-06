---
{"dg-publish":true,"dg-home-link":false,"dg-show-inline-title":false,"title":"Obsidian Clipper Readme","url":"https://syleria.netlify.app/garden/obsidian-clipper-readme/","created":"2022-09-21T11:01:39-05:00","updated":"2022-10-18T21:21:24-05:00","aliases":[],"tags":[null],"permalink":"/garden/obsidian-clipper-readme/","dgHomeLink":false,"dgShowInlineTitle":false,"dgPassFrontmatter":true}
---

[Obsidian Clipper](https://routinehub.co/shortcut/11156/) Readme
======

Obsidian Clipper (formerly Save to Obsidian) by Jim Syler  
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
There is an update mechanism included. Updating is always optional; you will be asked whether you want to update or not. The update mechanism is harmless, and cannot damage your system; it checks to see if there is an update available, and then optionally prompts you to download it from Apple’s Shortcuts Gallery. For more info, visit the [UpdateKit API home page](https://www.mikebeas.com/updatekit-api/). If for any reason you are uncomfortable with the included update mechanism, simply delete the action titled “If Version check is Yes” and respond with “Delete Actions” in the subsequent dialog. You can then Favorite the shortcut at [RoutineHub](https://routinehub.co/shortcut/11156/) to get notifications of new versions.

Latest version always available at <https://routinehub.co/shortcut/11156/>

If this has been helpful to you, feel free to [buy me a coffee!](https://www.buymeacoffee.com/calion)

Please report any bugs in a comment on [RoutineHub](https://routinehub.co/shortcut/11156/) or on [Twitter](https://twitter.com/messages/compose?text=Obsidian%20Clipper%20issue%3A%20&recipient_id=7663632).



### Known bugs and limitations
- [ ] Text containing links to YouTube videos will not import as text, but as a YouTube video
- [ ] Webpage images behind relative links do not show up
- [ ] Shows up for—but does not successfully import—iPadOS screenshots
- [ ] Web article headings show webpage title, not the heading seen in Reader. This is a bug in Shortcuts; [reported](https://openradar.appspot.com/radar?id=5627250862981120)
- [ ] Cannot support `blob:` URLs
- [ ] Evernote notes imported from Evernote’s “Export note” function do not include links to the original Evernote note
- [ ] Evernote formatting is not as good as it could be. The current method should be redone using XML parsing
- [ ] Clips cannot be saved to nested folders
	- There's a workaround: You can choose “\*New Folder\*” and enter whatever path you want, whether it already exists or not, and the file will be saved there. Cumbersome, but effective
- [ ] Will leave colons in titles in `title:` field in frontmatter, which causes YAML errors
	- [ ] Fix by putting single quotes around titles
- [x] YAML multiline tags have two spaces before the hyphen, whereas this Shortcut uses only one.
	- [ ] Unfixed this one, for compatibility with Frontmatter Tag Suggest
		- [ ] On that note, recommend useful plugins, like that one, to use with this shortcut?
- [ ] If you leave a comment on a clip, and the Shortcut subsequently fails for some reason, the comment is lost.
	- The easiest way to fix this is to move the Get Contents action to before this step, but that contradicts my wish to have the input happen before the time-consuming parts of the shortcut. I wonder if I could fix this by saving the comment to disk, deleting it if the Shortcut completes, and reloading it if they try the same site (or whatever) again
- [ ] Probably fails on non-tweet Twitter links

There are no immediate plans to fix these bugs, so if any of them are bothering you, let me know via the links above!

### Proposed features
- [ ] Add “archive article” option (or its own shortcut), which will take the Reader view of a Web article and import it to Obsidian, with *saved* images (hopefully missing ads), and the link to the original on top, to have a publishable archive of linked articles. Perhaps this should be the default saved webpage option. Alternately, support Web Archives, and write a plugin to get Obsidian to [recognize them](https://forum.obsidian.md/t/render-webarchive/17833) (for 3.0 release)
- [ ] Sticky preferences: Beta versions, do not open Obsidian (for 3.0 release)
	- BART has these, as an example
- [ ] Support “File” filetype, e.g. Pages files
- [x] Create button for user to open result in Obsidian, or not
- [ ] Prompt user to buy the developer a coffee after every 10 launches, with “not right now” and “never ask me again” options (for 3.0 release, but disable in beta)
- [x] Open Obsidian early to ensure notes open properly
	- [ ] Undid this
- [x] Ask every time what folder to put it in (for 3.0 release)
- [x] Ask for new note or append earlier, so user can ignore until it’s done (for 3.0 release)
- [x] You can get the selected text from the Get Details of Safari Web Page action! I gotta use that somehow
- [x] Pop up a multiple-choice menu asking for clipping options: Append, tags, notes, show result in Obsidian, etc. Then have successive screens depending on the options chosen (for 3.0 release)
- [x] Change documentation format to Markdown and reformat per my Daily Notes shortcut. Also remove periods at the end of bullets
- [ ] Advertise my other shortcuts in the readme (for 3.0 release)
- [ ] Advertise in the forums listed in Similar Products
- [ ] Upload shortcut to other services (and then largely ignore, trusting the update mechanism)
- [ ] Add option in beta versions to revert to last stable version (link will have to be manually input for every new stable), along with an explanation that it’s a beta, and you’re expected to test and report bugs (for 3.0 release)
- [ ] Go over whole Shortcut (for 3.0 release)
- [ ] Add “Link only” to ~~Web~~ and YouTube (and, hell, Evernote and Reddit) options. Yes, the Obsidian share sheet extension can already do this better, but why have to switch between? (for 3.0 release)
- [ ] Add support for Evernote tasks
- [ ] The ability to import Evernote files from the app instead of from ENEX files may go away at some point, as I don’t want to have to support two different methods, and this way is largely inferior (the only reason this function exists at all is that I had already written it before I discovered that exporting ENEX files was possible on mobile).
- [ ] Separate prefs and info dicts, as in Daily Notes (for 3.0 release)
- [x] Switch bugs and features in the readme
- [x] Move readme online entirely, just keeping basic info that won’t change in the Shortcut?
- [ ] Show full documentation on first run (and how to find it again)
	- Nice example documentation in the BART shortcut
- [ ] Have a way to permanently exclude folders from the list that appears when you choose New File.
- [ ] Consider including the Evernote link for Evernote notes. This will be involved and kind of hacky, as it’s got to search for the note name in Evernote. Luckily I already created the mechanism to do so, but it’s kind of cumbersome for the user. I’ve also considered writing a separate shortcut for this purpose
- [ ] Format latitude and longitude data (from Evernote specifically) to be compatible with [Leaflet](https://github.com/valentine195/obsidian-leaflet-plugin)
- [ ] Use (*not* copy) R downloader to download YouTube video
- [x] Consider having a Metadata section header as Matter does
	- [x] If you do that, probably also have Comment and Article headers
- [ ] Remove option to open in Obsidian, and use [Pushcut](https://www.reddit.com/r/shortcuts/comments/dzcri5/creating_notification_that_can_trigger_an_action/?utm_source=share&utm_medium=ios_app&utm_name=iossmf) to have a confirmation notification that also opens the note in Obsidian.
	- [ ] As an alternative, perhaps put a confirmation alert at the end with an option to open Obsidian.
- [x] Have a default folder so that you don’t have to pick every time when they’re all going to Bookmarks.
- [ ] Since I'm changing the name of the shortcut, need to delete the old one on first run.
- [ ] Try using a folder action rather than manually inputting filepaths.
- [ ] Learn how to use Automator/AppleScript and write a script that will send data from a pre-Monterey Mac to Messages, to activate a Personal Automation.
- [ ] Option to extract text from PDF
- [ ] Given the automatic header in Obsidian 1.0, remove H1s from every template
- [ ] Show how to set up a Personal Automation to automatically import Evernote exports
- [ ] Import YouTube playlist (look at <https://routinehub.co/shortcut/4088/>)?
- [x] Did I already fix the “YouTube app sends text type” problem and thus break YouTube support? Check.
- [x] Do I really need “Link only” in New Note? Seems pointless. 
	- [x] Apparently, as I've used it. 
- [ ] Validate YAML, specifically titles. The only thing that messes things up is double quotes. Both single and double quotes would be a major problem. 
	- [ ] Obviously, this is in the process of putting all the titles back, as requested (for 3.0 release)
	- [ ] Having umpteen different output sections is getting old. I don’t want to have to run whatever routine this turns out to be on every different one. On the other hand, this could happen at the end.
- [ ] Move link to full readme to top of internal readme?
	- [ ] Also don’t call them both the readme?
- [x] Move “get urls” from the top to various places you need it. It is not useful unless you’re dealing with a URL type, right?
- [ ] This list has gotten cumbersome and includes a bunch of stuff not fit for public consumption. Move what shouldn’t be public-facing to its own note and transclude the Proposed Features and Known Bugs there. 
- [ ] Facebook support 
- [ ] Twitter clips are currently in HTML. The way they're imported, it should be possible to display them in nice cards with JavaScript. Figure out how to do that in Obsidian: https://forum.obsidian.md/t/add-external-javascript-to-support-custom-webcomponents/42057 https://developer.twitter.com/en/docs/twitter-for-websites/javascript-api/guides/set-up-twitter-for-websites
- [x] Maybe instead of proliferating options, I can have a startup option for “custom options.” If that's not selected, it will just import in Markdown without asking. 
- [ ] Change “Use raw Web contents” to “More options.”
- [ ] Use your link shortener app for the Twitter links in the docs for all shortcuts
- [ ] Regularize formatting and content in readmes in all shortcuts and all locations (Garden, RoutineHub, internal)
- [ ] Combine the two Evernote options and provide an option to prepend “Exported to Obsidian on \<date\>” and the link to the note in Obsidian
- [ ] Default to html for Web import, and restore “more options”
- [ ] Possible Reddit improvements:
	- [ ] Preview image
	- [x] HTML text
	- [ ] Post flair
	- [x] Option for link only
	- [ ] Option to grab comments

### Similar products
- [MarkDownload](https://forum.obsidian.md/t/markdownload-markdown-web-clipper/173)
- [Obsidian Web Clipper](https://forum.obsidian.md/t/obsidian-web-clipper-bookmarklet-with-full-markdown-support-for-images-headings-and-code-blocks/22068)
- [ReadItLater plugin](https://github.com/DominikPieper/obsidian-ReadItLater)
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
- [Test - Get Info From Twitter URL 2](https://www.icloud.com/shortcuts/f1e8b7b57c7d4619be508a212eaabf73) (via [Automators Talk](https://talk.automators.fm/t/save-tweet-information-via-siri-shortcuts/3697/7>))
- [Copy to Clipboard 2](https://www.reddit.com/r/shortcuts/comments/y90pwg/get_data_from_input_with_two_types/it2w482/)

## Version History

### 3.0.0-a.2 (2022-10-20)
#### New Features
- Adds Titles back to frontmatter (in progress)
- Supports Reddit comments (in progress)
- Adds “More options” option in initial menus, to hide some choices unless they're needed
	- Removed it again, because I hate it 
- Adds “Use raw Web contents” option to Web import options, to improve import for webpages that don't support Safari Reader

#### Bug Fixes
- Fixes broken Web import

### 3.0.0-a.1 (2022-10-20 (begun 2022-04-21))—Reddit alpha 1
#### New Features
- Imports images from webpages, creating a permanent archive. This is the default behavior, though there is a preference to turn it off. [In progress]
- Adds Evernote support
- Adds runtime options to import Web pages as Markdown, HTML, PDF, or [Markdown] extract
- Adds frontmatter indicating the origin of the clip, date created, and other info if available
- Adds image support
- When New File is chosen, images and photos will be imported into a new Note, not merely placed in the Attachments folder
- Changes name from “Save to Obsidian” to “Obsidian Clipper”
- Adds option to save new notes to a specific folder
- Moves full readme file to <https://syleria.netlify.app/garden/obsidian-clipper-readme/,> leaving a stub in the Shortcut
- Moves dialogs to early on in the Shortcut run, so the user can answer questions and then ignore the Shortcut until it's finished [In progress]
- Adds ability to add tags and comments to new notes
- Adds option to turn off version checking
- Adds support for Web links to Markdown and other text files
- Gets webpages of URLs entered when the shortcut is run by itself
- Adds support for importing PDFs
- Adds support for Twitter tweets
- Adds “Link only” option for Web pages. **Note:** The native Obsidian share sheet extension does this quicker and better
- Adds Reddit support

#### Bug Fixes
- Removes slashes from filenames, which caused files to be created in subfolders
- Fixes issues caused by inputs having multiple data types. User will now be asked to choose which to use
- Errors out on `blob:` URLs rather than failing silently
- Improves handling of Internet connection check
- Fixes an issue where clips with the same name as an existing file would be appended to the existing file
- Opens Obsidian earlier to help ensure notes open correctly

### 2.1.0 (2022-03-30)
#### New Features
- Saves web pages as Reader articles
- Adds ability to opt in to beta versions

#### Bug Fixes
- Now works in any language
- Accepts unsupported file types
- Opens correct file if appended to a nested file

### 2.0.1 (2022-03-29)
#### Bug Fixes
- Fixes shortcut name and beta status

### 2.0.0 (2022-03-28)
#### New Features
- Option to append to existing note (especially useful for images!)

#### Bug Fixes
- Doesn’t fail if there’s no Internet connection

### 1.5.2
#### Bug Fixes
- Fixes version checking error

### 1.5.1
#### Bug Fixes
- Can handle filenames with periods (I’m a little concerned that this will cause other files not to automatically open in Obsidian—I had left the extension off the link for a reason—, but it works in my testing so far)

### 1.5.0
#### New Features
- Built-in update checking with [UpdateKit API](https://www.mikebeas.com/updatekit-api/v1)

#### Bug Fixes
- Fixes error in duplicate handling mechanism (Shortcuts doesn’t need the period when it looks for file extensions; doh!)
- Now can handle Markdown files! (doh again!)  
[These bugs were fixed in 1.5, but not included in the release notes on Routinehub until 1.5.1, because I wanted to test the new update mechanism. And then I found another bug anyway 🤷‍♂️]

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
- Fixes lack of input options

### 1.1.0
#### New Features
- Adds photo support

### 1.0.0
- Initial release, inspired by “[[Feature] iOS share sheet extension](https://forum.obsidian.md/t/feature-ios-share-sheet-extension/14873)”