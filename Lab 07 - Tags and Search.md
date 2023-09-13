---
date created: Wednesday, February 1st 2023, 18:57:41
date modified: Wednesday, September 13th 2023, 14:00:23
---

# Lab 07 - Tags and Search

### Index

- [What's a tag?](#What's%20a%20tag?)
- [How to make tags](#How%20to%20make%20tags)
    - [Exercise 1](#Exercise%201)
- [Searching for tags](#Searching%20for%20tags)
- [Searching](#Searching)
    - [Exercise 2](#Exercise%202)
- [Queries](#Queries)

Obsidian really takes of and excels as a knowledge management tool because of it's support for tags and it's fast and powerful search. This is where you knowledge becomes useful. Documenting stuff isn't hard. Finding your note a year later, that's the true challenge.

### What's a tag?

A tag is a powerful concept. It's a way to label notes or items. The importance and use of tagging is rapidly expanding in many tools, systems and networks. The idea of a tag is that it's like a sticker. You create it and you keep sticking it on anything you feel that should be labeled with your sticker.

The tags become a field you can search for: All files tagged with `#tag`. As tags have autocomplete, it's really easy and fast to stick to a convention, a strict naming system.  
Many people see tags as a natural successor to folders (in mail, in file-systems, everywhere). You can only put a file in one folder.

What if a file or email is about two diffent topics?  
This is the main reason for tags: **You can put as many tags in a note as you want**.

Other reasons:  

- *Self contained:* the tag is in the file, and depends on nothing else.
- *Cross-compatibility:* many other programs and editors recognize the tags and use them straight away too.
- *Independant:* Even if tags aren't supported, you can still use a fileprint tool or editor to look for the `#tag`.

Here's a good article if you want to dive into a good system for creating and organizing tags if you are interested:  
[Forget Folders: The Best Ways to Organize Your Files with Tags and Labels](https://zapier.com/blog/how-to-use-tags-and-labels/)

### How to make tags

To create a tag you just start using it. Type a tag and it exists. It will directly manifest in Autocomplete.  
A tag is a `#` followed by a number of letters, numbers and dashes and underscores:

- `#This_is_a_good_tag`
- `#123_Testing-tag`
- `#Topic_12`

Obsidian adds something powerfull: Tag nesting. You can add tags as a subtag to a main tag. In Obsidian this gives the note both tags at once.

- `#Topic/subtopic`
- `#Maintag/subtag`

If you apply the second tag to a note, the note would be found by `#Maintag` and by `#Maintag/subtag`. This nested tag strategy helps you organize your tags easily.

### Exercise 1

- [ ] Create 3 tags and place them in some notes.
- [ ] Try adding a tag by writing parts of the tag, to see how the autocomplete works (you don't have to start at the beginning of the tag).
- [ ] Notice what happens when you click a tag.

### Searching for tags

You can search for your tags in two ways: By matching the tag and by matching the content of the tag. By matching the tag you'll only find content that bears the tag. By matching content of the tag it won't be a strict match.

tag:#specific/thing will only match the tag.  
`#spec` matches all shapes and subtags, and is case insensitive.

### Searching

When you click the search box and then click the search field you get useful options:

![|300](assets/Lab%207%20-%20Tags%20and%20Search.png)

All things you type must be true together within one note. The search autmatically asumes a hard "AND", all things must be true. You can add "OR" to find notes for which either is true. You can group with ()'s.

With `line()` you can find words that are specifically on the same line. This is often very handy! With `block()` the same alinea, and with `section()` the part between 2 headers.  
A powerful and yet often overlooked powertool of the search is the sort order. You can sort by last modified, which almost always ensures that what you are looking for is on top!

![|350](assets/Lab%207%20-%20Tags%20and%20Search-1.png)

#### Exercise 2

- [ ] Try working with the search and toggles.
- [ ] Press the `Read more` in the search to see the other capabilities. It show's you the [Obsidian search documentation](https://help.obsidian.md/Plugins/Search)

![|350](assets/Lab%207%20-%20Tags%20and%20Search-2.png)

## Queries

A nice and often overlooked feature of Obisidian is Queries. You can enter a search in a query-block, making a page contain your search results dynamically. When you are effectively using Tags, you will find it useful for instance to make a search field containing [your main tags](Addendum%203%20-%20Methods%20of%20Note-taking%20and%20Organizing.md#Forget%20Folders:%20The%20Best%20Ways%20to%20Organize%20Your%20Files%20with%20Tags%20and%20Labels.). Use it like this:

<pre><code>``` query
#Tag
```</code></pre>
