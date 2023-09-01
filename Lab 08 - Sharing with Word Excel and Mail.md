---
date created: Wednesday, February 1st 2023, 20:10:14
date modified: Wednesday, August 30th 2023, 10:39:51
---

# Lab 08 - Sharing with Word Excel and Mail

## Index

- [Sharing your docs - Export to Word, Excel or mail](#Sharing%20your%20docs%20-%20Export%20to%20Word,%20Excel%20or%20mail)
    - [Exercise](#Exercise)
- [Export to PDF](#Export%20to%20PDF)
- [Import from Excel](#Import%20from%20Excel)

## Sharing your docs - Export to Word, Excel or mail

A big part of working together is sharing documentation. Starting from Markdown is most often a good base to any other document. The styling options that Markdown offer are possible in nearly any other document system.  

When copying Markdown you copy plain text with markup code in it. If a receiving program recognizes this it will be converted to what it should be. When other people also use markdown you can just share the plain text code and do them a favour. For others you will rely on this translation in applications.

We can **massively** improve on this proces by copying HTML in stead of Markdown, since that is even more universally supported. We do however need a plugin to aid in this, which we will install and use in the next exercise.

### Exercise

- [ ] Go to `Settings` -> `Community plugins` and select browse<br>![](assets/Lab%208%20-%20Sharing%20with%20Word%20Excel%20and%20Mail.png)
- [ ] Search for `Copy as HTML` and select it.
- [ ] Enable the plugin.
- [ ] Open Microsoft word or start a new message in your favorite mail client.
- [ ] Take one of the demo notes from the demofiles I supplied in the [What's a Vault](Lab%2001%20-%20Installation%20and%20a%20Vault.md#What's%20a%20Vault)
- [ ] Make a selection and use the `cmd+p` (mac) or `Ctrl+p` combination to open commands. Type `html` and select `Copy as HTML: Copy as HTML command`.
- [ ] Open your mail or word document and past the clipboard.

**Note:** This will also work when copying a table from Markdown to Excel.

### Export to PDF

Obsidian allows you to export a page to PDF. Just press `cmd+p` (mac) or `ctrl+p` (others) and type `pdf`. Select `Export to PDF` and see what settings you get.

### Import from Excel

A table is quickly and easily made in Excel, and sometimes you just want to import tables from other resources. A quick hack is to past a table you want to import in Excel, adjust and copy it from there.

Install the plugin `Excel to Markdown table` and use that through the `cmd+p`/`ctrl+p` option to past an Excel table straight to a Markdown table.
