---
weight: 3
title: 高级搜索运算符
type: docs
---

### 高级搜索运算符

#### in:

这将搜索位于给定路径下的文件。这包括子文件夹中的文件。

查询示例：

```
in:apple
```

输出示例：

```
apple/a.txt
apple/b.txt
apple/subfolder/cool.txt
apple/subfolder/hello.txt
```

#### children:

这个操作符用于查找给定路径下直接的子文件。不包括子文件夹中的文件。

查询示例：

```
children:apple
```

输出示例：

```
apple/a.txt
apple/b.txt
```

#### ext:

这个操作符用于搜索具有特定扩展名的文件。

查询示例：

```
ext:wav
```

输出示例：

```
apple/sound.wav
bee/buzz.wav
cat/purr.wav
```

#### leading:

此搜索将查找其路径以给定文本开头的文件。

查询示例：

```
leading:a
```

输出示例：

```
apple/image.png
air/composition.txt
apex/gameplay.mp4
```

#### inpath:

这将搜索路径中包含给定文本的文件。

查询示例：

```
inpath:hello
```

输出示例：

```
hello world/screenshot.png
videos/how to say hello in spanish.mp4
othello/script.txt
```
