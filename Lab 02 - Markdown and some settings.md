---
date created: Wednesday, February 1st 2023, 18:38:40
date modified: Wednesday, August 30th 2023, 09:18:06
---

# Lab 02 - Markdown and some settings

### Index

- [What's Markdown](#What's%20Markdown)
- [Change some settings](#Change%20some%20settings)

## What's Markdown

Markdown is a widely adopted markup language. It's very basic and simple, and is capable of just enough styling to keep it easy. Even if a person doesn't know Markdown, they are normally capable of reading Markdown documents with intuitive understanding.  
Markup is plain text with markup code. This means that it will open on any machine with a basic text editor. It is heavily supported with a lot of good and free editors out there. Obsidian is also a Markdown editor, with added focus on the Vault and notetaking as a proces.

**The most missed and therefor frustrating Markdown code:**  
End a sentence with two spaces to have a new line (return) within an alinea.

- [ ] Please take some time to shortly look over this cheatsheet (don't learn it!), so you know it's there and can help you if you even need it. You mostly don't, as Obsidian will help you with a graphical editor:  
      <https://github.com/adam-p/markdown-here/wiki/markdown-Cheatsheet>  
      *Or* a longer cheatsheet for future reference:  
      <https://www.freecodecamp.org/news/markdown-cheatsheet/>

## Change some settings

1. Click the cogwheel in the left bottom to open Obsidian's settings:  
    ![|75](assets/Lab%202%20-%20Markdown%20and%20some%20settings.png)
2. In the `Editor` settings set at least the below settings and next to that everything you like:
    - [ ] `Default view for new tabs: Editing view`
    - [ ] `Default editing mode: Live Preview`
    - [ ] `Editor status: enabled`
3. In `Files & Links`:
    - [ ] `New link format`: `Relative path to file`
        - This greatly aids in working together and keeping notes portable between computers.
    - [ ] Disable `Use [[Wikilinks]]`
        - **Important:** *While the linking is much nicer for humans, it is not compatible with the Markdown specs and makes you unable to share your notes with others. This can seriously impact cooperation and compatibility.*
    - [ ] Enable `Detect all file extensions`
    - [ ] `Default location for new attachments`: `In subfolder under current folder`
    - [ ] `Subfolder name`: `assets` (Strongly suggested, as this is a commonly used name)
1. In `Core plugins`:
    - [ ] Turn an all plugins except `Publish` and `Sync`. These are paid functionality in the cloud.
        - These are ***optional***:
            - `Audio Recorder`
            - `Format converter`
            - `Slash commands`
            - `Slides`
            - `Starred`
