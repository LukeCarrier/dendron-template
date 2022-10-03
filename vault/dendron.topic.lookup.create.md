---
id: 0e57f8d1-e501-49db-974c-01eb64c20c22
title: Creating Notes
desc: ''
updated: 1664168248412
created: 1608494562268
---
## Summary

While we call it the `Lookup Bar`, you can also use it to create notes that don't exist. When you lookup for a note that hasn't been created, Dendron will create it for you. 

To try it yourself, bring up the lookup bar. Type `hello` and hit `Enter`.

## Creating new note

When looking up a note that does NOT have any special characters [" ","|","*","^","$","!","=","'"] (note: space is deemed as special character), and does NOT yet exist, `Create New` will bubble up to the top of query results to make it convenient to create a new note.

A new note will be created when you hit `Enter` while `Create New` is selected.

## Creating Notes with template applied

Similar to how you can [[create a new note|dendron://dendron.dendron-site/dendron.topic.lookup.create#creating-new-note]], you can create a new note and select a template to be applied upon creation.

If you hit `Enter` while `Create New with Template` is highlighted, you will be prompted again to select the template to be applied.
If you hit `Enter` again after selecting the template, a new note will be created with the template already applied.

> Lookup modifiers that can conflict with the template application will be disabled when you create notes this way.  
> 
> This means [[selectionExtract|dendron://dendron.dendron-site/dendron.topic.lookup.modifiers#selectionextract]] will have no effect even when selected.

> Lookup modifiers that apply templates or modify the note themselves in any way will disable this behavior.
>
> This means `Create New with Template` will not appear if you are [[creating a task note|dendron://dendron.dendron-site/dendron.topic.tasks#creating-a-task-note]]

## Creating Special Notes

Dendron has builtin notion for certain types of notes with [[pre-defined hierarchies|dendron.topic.special-notes]]. These notes can be created by toggling the corresponding **note button**  on the lookup menu or by using the respective builtin shortcuts.

- values:
  - none (default): create a regular note
  - journal: create a journal note (cmd/ctrl + shift + j)
  - scratch: create a scratch note (cmd/ctrl + shift + s)

## Creating Notes with a Selection

If you have text highlighted while creating a new note with a lookup, the new note will be created using the text selected. How the text will be used depends on  the `dendron.defaultLookupCreateBehavior` setting.

- values:
  - selectionExtract (default): create new note with text from the old note. remove text from the old note
  - selection2link: create new empty note and turn selection into a link referencing the old note

<a href="https://www.loom.com/share/61d754c1dca84b99b2786b2f89473566">
<img style="" src="https://cdn.loom.com/sessions/thumbnails/61d754c1dca84b99b2786b2f89473566-with-play.gif"> </a>

## Vault Selection for New Notes

If you have multiple vaults in your workspace, you can control the behavior of which vault your new note will be placed in:

![[dendron.topic.multi-vault#vault-location-when-creating-a-note:#navigating-links]]
