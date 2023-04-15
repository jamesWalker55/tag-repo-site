---
weight: 3
title: 高度な検索演算子
type: docs
---

### 高度な検索演算子

#### in:

これにより、指定されたパスの下にあるファイルが検索されます。これには、サブフォルダ内のファイルも含まれます。

クエリ例：

```
in:apple
```

出力例：

```
apple/a.txt
apple/b.txt
apple/subfolder/cool.txt
apple/subfolder/hello.txt
```

#### children:

このオペレーターは、指定されたパスの直接の子ファイルを検索します。サブフォルダー内のファイルは含まれません。

クエリ例：

```
children:apple
```

出力例：

```
apple/a.txt
apple/b.txt
```

#### ext:

このオペレータは、指定された拡張子を持つファイルを検索します。

クエリ例：

```
ext:wav
```

出力例：

```
apple/sound.wav
bee/buzz.wav
cat/purr.wav
```

#### leading:

この検索は、指定されたテキストで始まるパスを持つファイルを検索します。

クエリ例：

```
leading:a
```

出力例：

```
apple/image.png
air/composition.txt
apex/gameplay.mp4
```

#### inpath:

これは、指定されたテキストを含むパスのファイルを検索します。

クエリ例：

```
inpath:hello
```

出力例：

```
hello world/screenshot.png
videos/how to say hello in spanish.mp4
othello/script.txt
```
