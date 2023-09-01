---
date created: Wednesday, August 30th 2023, 09:11:41
date modified: Thursday, August 31st 2023, 15:07:29
---

# Lab 10 - Extra - Dataview

## Index

- [What is Dataview?](#What%20is%20Dataview?)
    - [Practical example - Why do you want this?](#Practical%20example%20-%20Why%20do%20you%20want%20this?)
- [How to Dataview](#How%20to%20Dataview)
    - [Query result types](#Query%20result%20types)
    - [Query sources (from)](#Query%20sources%20(from))
    - [Filter your results (where)](#Filter%20your%20results%20(where))
- [Exercise](#Exercise)

## What is Dataview?

Dataview is a plugin that enables you to query your notes like a database. These queries can be embedded in your notes to be constantly up to date and all-compassing.

It helps you to create and maintain lists or indexes.

### Practical example - Why do you want this?

You like to read books. You like to log some excerpt, how you liked it and when you finished it.

You've just read "Dune". You make a note "Dune.md" in your vault and put the info in there. The author of Dune is Frank Herbert. You also put that in the note.  

Now you want to read a new book. You decide to read "Dune Messiah", another book of Frank Herbert.  
Again, you put a note in your vault: "Dune Messiah.md".

Now, if you want to find the books of this author, you have to content-search for his name. The results will more or less be all the notes of books you've read from him. That's nice, it gives you the overview on the author.

As you've read two books from him now you decide to create a note for the author: "Frank Herbert.md". You put in there that was a successful writer in the 1970s and 1980s. It makes sense to list the books that you've read from him in there. So, you put in links to his two books.

You also keep a list of what you've read, so you create a "Books I've read.md". You also put the links in there.

You find out these books are part of the "Dune Chronicles" series. You make a note "Dune Chronicles - Series", and again decide to list the books in there. You update the books to contain the series. You update the author to display the Series as well.

So, for every new book that you will read, you'll have to remember to make and update 3 notes: Author, Series, Book. And don't forget to put it on the "Books I've read" list.

This will quickly become very intensive and bothersome.

With Dataview you would just put in the new book, and the author and series would be updated automatically.

## How to Dataview

### Install dataview

- [ ] Install the community plugin: `dataview`
    - [ ] Go to `Settings` -> `Community plugins`
    - [ ] Turn off `Restricted mode`
    - [ ] Click `Community plugins` - `Browse`
    - [ ] Search for `dataview` and install it.
    - [ ] Enable the plugin `dataview` in `Settings` -> `Community plugins`

### Use dataview

Let's start with the key concepts:

In order to create a query you create a codeblock for dataview:

<pre><code>
``` dataview
```
</code></pre>

### Query result types

In this you start the query by choosing the result format:

- LIST  
  Just a bullet list
- TABLE  
  A markdown table
- TASK  
  A task list
- CALENDAR  
  Shows your results as dots in a calendar view

This would bring us to:

<pre><code>
``` dataview
LIST
```
</code></pre>

### Query sources (from)

Then you choose where the results should come from.

- Folders: "directory/subdir"
    - This wil include all markdown files in this location. If you just type "directory" it will list all files in that directory and subdirectories.
- Files: "directory/subdir/file.md"
- `#TAG`
    - All files in the vault containing this tag.
- Links
    - Links that point to a file - incoming (eg all notes that point to "this" note)
    - Links that come from a file - outgoing (eg all the notes that "this" note points to)

This would bring us to:

<pre><code>
``` dataview
LIST
FROM "books/" OR #Dune
```
</code></pre>

### Filter your results (where)

We've made too wide a net in the query above. It will find all notes in the folder "books", not just the relevant books. For this we can use where. Just the results in which "where" is true will be listed.

<pre><code>
``` dataview
LIST
FROM "books/" OR #Dune
WHERE containers(file.name, "dune")
```
</pre></code>

This statement is iffy.There can be booktitle with no dune in the title. WHERE normally searches in the meta data fiels. You can add `series: dune` in the frontmatter ([read about frontmatter](https://help.obsidian.md/Editing+and+formatting/Properties)) and even in "datafields" as defined by the dataview plugin. If you list `Series: Dune` in the note, you can make Series a key and Dune a value by adding ":" - `Series:: Dune`

This changed it in a searchable key/value pair, effectively the same as putting it in the frontmatter.

Here's a real life example, which is beyond the scope of this lab, but gives you some feel:

<pre><code>
```dataview
TABLE without ID
file.link AS Naam, Bedrijf, Rol
FROM #Mensen AND ((#ON2IT OR [[ON2IT]]) AND !"Mensen/ON2IT/Ex")
WHERE contains(Bedrijf, "ON2IT")
SORT file.name asc, Bedrijf desc
```
</code></pre>

## Exercise

- [ ] Put some tags in some notes and create an index for the tag-topic using dataview. Notice how easy this is!
- [ ] Put some frontmatter in your notes and index them using a dataview query to get some feeling for this. A bit harder but very versatile!
- [ ] Add [Dataview documentation](https://blacksmithgu.github.io/obsidian-dataview/) to your favourites, as you'll be using it in the future!
