---
date created: Wednesday, August 30th 2023, 09:26:42
date modified: Friday, September 1st 2023, 09:36:19
---

# Lab 11 - Extra - Hierarchy

This lab is merely a construct or trick to create an easy to navigate notes system. Heavily inspired by Zettelkasten and other concepts on which I can talk for hours I would like to give you this one trick: Create hierarchy in your notes.  

Normally this is a cumbersome proces but I've really tuned it down to bare metal which will keep paying off:

> **Every time you create a note, think about what note would be the parent of this note.**

Whether "Meetings with Mr. X", "Fossil fuels" or "Company Y", put `up::` in the top of your note and put a link to the note you're referencing.

If you do this continously you'll find that your notes will be amazingly easy to navigate. Sometimes you'll find that you have not yet created the note you'd put this under. That's fine, just create it at your leasure.

The note from the example "Company Y" could just contain the following query (see: [Lab 10 - Extra - Dataview](Lab%2010%20-%20Extra%20-%20Dataview.md)) and be very helpful:

<pre><code>
``` dataview
LIST
FROM [[Company Y]]
```
</code></pre>

*Remember: `FROM [[Company Y]]` finds all pages which link to that page*.

To improve quality of life, we can even amp up the relevance:

<pre><code>
``` dataview
LIST
FROM [[Company Y]]
SORT file.mtime DESC
```
</code></pre>

Now the most recently edited files will be on the top. Mostly I find the file I'm looking for is in the first five listed!

## Note - Structure notes (Zettelkasten) or Map of Content

Often these notes are then referred to as "Structure notes" or "Map of content". A lot of people, including me, generally like to put these structure notes outside of my other notes, so the structure is in a different folder or location and your notes are pure collections or knowledge.

You can really adjust these to your liking. I like mine to be short and bulleted, but some people create pictures, canvases or entire stories and textst in which they put the links.  
If you feel like this would benefit you, let me know, as I've found quite a clever trick to enable you doing just that.

Here's a practical example of a MoC I use:

![](assets/Lab%2011%20-%20Extra%20-%20Hierarchy-1.png)

The linking between the notes creates a hierarchy that makes relations visible and enable you to browse the context:

![](assets/Lab%2011%20-%20Extra%20-%20Hierarchy.png)

## Exercise

- [ ] Try creating 3 central logical "top" notes in your collection, add the above dataview query and start linking some notes.
