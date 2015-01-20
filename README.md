# iframe-resizer
クロスドメインでもiframeの中身にiframeの高さを揃えるライブラリ

## 条件

親子ともにスクリプトを埋め込める環境であること。他人のサイトの高さは取ることができません。

## 使い方

### 親側

FrameReceiver.jsを読み込みます。

```html
<script src="./FrameReceiver.js"></script>
```

リサイズさせたいiframeには必ずIDとクラスをつけます。

```html
<iframe src="./frames/content.html" id="content" class="iframe-resize"></iframe>
```

### 子側

FrameSender.jsを読み込みます。

```html
<script src="./FrameSender.js"></script>
```

## サイズ変更

初回及びwindowがリサイズされたときに高さが更新されます。

## Public Functions

### FrameReceiver.send()

親側からiframeの高さを更新します。任意のタイミングで高さの再取得が可能です。

### FrameSender.send();

子側からiframeの高さを更新します。任意のタイミングで高さの再取得が可能です。


## License

MIT License