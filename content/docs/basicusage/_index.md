---
weight: 1
title: Basic Usage
type: docs
---

# Basic Usage

tagrepo operates on folders. When you start the software, the file list remains empty until you choose a folder to act as a **repository**. After choosing a folder, tagrepo scans the folder and builds a list of file paths. After this is complete, you can then assign tags to files, as well as search for files.

## Repositories

![Screenshot of a repository in Windows Explorer, demonstrating the automatically-generated `.tagrepo` folder](manual-repository.jpg)

A repository is a single folder. tagrepo operates in a single repository (folder) at a single time.

Every repository contains a folder named `.tagrepo`. This folder contains all the information tagrepo needs, like file paths and tags. If a folder doesn't yet have a `.tagrepo` folder, tagrepo automatically creates a `.tagrepo` folder at the base of the folder.

## File operations

![Screenshot of the the context menu in tagrepo](manual-contextmenu.jpg)

To access a file in the list, you can right click on a file to display a context menu. From the menu, you can either open the file, reveal the file (open the folder that contains the file), or copy the path of the file.

You can also select multiple files in the list, then right click to operate on all of them at the same time. Hold down the Shift key and click on two files to create a range selection, and hold down Ctrl to select each file individually.

## Tagging files

![Screenshot of the properties panel in tagrepo](manual-tagging.jpg)

A file can be assigned tags. A tag cannot contain spaces, since spaces are used to separate each tag. If you wish to create a tag with several words, consider using characters like `-` or `_` in the tag.

For example, `my cool tag` is an invalid tag - it gets treated as 3 separate tags by tagrepo: `my`, `cool`, and `tag`. You can consider using a tag like `my-cool-tag` instead.

Tagging is done through the properties panel. Click on the **Add tags** button to display an input field. You can then type in a list of tags to be added to the file you have selected (the tags must be separated by spaces).

To remove a tag from a file, first select the file. On the properties panel, click on the tag you want to remove. The tag to-be-removed will be highlighted as you mouse over it.

## Queries

![Screenshot of the query bar in tagrepo](manual-query.jpg)

tagrepo supports a flexible query language. It lets you search for files by tags or by their relative path.

You search for a file containing a tag by simply typing the name of the tag. If you want to search for multiple tags, type the name of each tag, separated by a space:

```
tag1 tag2 tag3 hello goodbye
```

The query bar also supports searching by the path of the file. These search operators begin with the name of the operator (e.g. `in`), followed by a colon `:`, then the text to search for. You can use quotes (`"`, `'`) in the text to include spaces in the search. Currently, five search operators are supported: `inpath`, `in`, `ext`, `children`, `leading`. These will be discussed later in [Advanced search operators]({{< relref "/docs/advancedquery" >}}).

```
in:drums
inpath:"hello world"
```

All of these operators can be combined freely with boolean operators. The operators include `|` for "or", and `-` for "not". Multiple search terms in a sequence are treated as an "and" group. Parenthesis (`(`, `)`) may also be used to group search terms.

```
kick drum (my_sample_pack | in:'Freesound' | in:'rendered_audio')
```
