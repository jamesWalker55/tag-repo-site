---
title: Advanced search operators
type: docs
---

### The folder panel

![Screenshot of the folder panel in tag-query](https://jameswalker55.github.io/tag-repo-site/assets/manual-folder-panel-34890106.jpg)

The folder panel allows you to search for items based on their folder structure. This is hidden by default and can be enabled through the toolbar: `View > Folders`

By default, the folder panel searches for files that are **direct child### Advanced search operators

#### in:

This searches for files that are under the given path. This includes files in subfolders.

Example query:

in:apple

Example output:

**apple/**a.txt
**apple/**b.txt
**apple/**subfolder/cool.txt
**apple/**subfolder/hello.txt

#### children:

This searches for files that are direct children of given path. This does not include files in subfolders.

Example query:

children:apple

Example output:

**apple/**a.txt
**apple/**b.txt

#### ext:

This searches for files that have the given extension.

Example query:

ext:wav

Example output:

apple/sound**.wav**
bee/buzz**.wav**
cat/purr**.wav**

#### leading:

This searches for files that have a path which starts with the given text.

Example query:

leading:a

Example output:

**a**pple/image.png
**a**ir/composition.txt
**a**pex/gameplay.mp4

#### inpath:

This searches for files that contain the given text in the path.

Example query:

inpath:hello

Example output:

**hello** world/screenshot.png
videos/how to say **hello** in spanish.mp4
ot**hello**/script.txtren** of the folder. This means it does not search for files that are inside subfolders of the given path. This behaviour can be changed with the **"Recursive"** option in the panel settings. When enabled, the folder panel also searches for items that are in subfolders of the given path.

### Audio preview

![Screenshot of the audio toolbar in tag-query](https://jameswalker55.github.io/tag-repo-site/assets/manual-audio-preview-7e8800a3.jpg)

*Note: Audio preview is still in early development and may be buggy at times.*

The audio preview feature allows tagrepo to play an audio file when you click on an item. This is disabled by default and can be enabled through the toolbar: `Audio > Audio preview`

After enabling audio preview, tagrepo is able to preview the following file types: `.mp3`, `.wav`, `.flac`, `.ogg`. To preview a file, click on a file in the list.
