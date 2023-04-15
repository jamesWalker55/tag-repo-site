---
weight: 3
title: Advanced search operators
type: docs
---

### Advanced search operators

#### in:

This searches for files that are under the given path. This includes files in subfolders.

Example query:

```
in:apple
```

Example output:

```
apple/a.txt
apple/b.txt
apple/subfolder/cool.txt
apple/subfolder/hello.txt
```

#### children:

This searches for files that are direct children of given path. This does not include files in subfolders.

Example query:

```
children:apple
```

Example output:

```
apple/a.txt
apple/b.txt
```

#### ext:

This searches for files that have the given extension.

Example query:

```
ext:wav
```

Example output:

```
apple/sound.wav
bee/buzz.wav
cat/purr.wav
```

#### leading:

This searches for files that have a path which starts with the given text.

Example query:

```
leading:a
```

Example output:

```
apple/image.png
air/composition.txt
apex/gameplay.mp4
```

#### inpath:

This searches for files that contain the given text in the path.

Example query:

```
inpath:hello
```

Example output:

```
hello world/screenshot.png
videos/how to say hello in spanish.mp4
othello/script.txt
```
