+++
date = '2025-04-04T18:00:00+09:00'
draft = false
title = '【配布】uwe_overlap_uv'
tags = ['Maya', '配布']
+++

## ナニコレ？
UV頂点を、一番近くのUV頂点にスナップするスクリプトです。

▼ダウンロードはこちら  
[uwe_overlap_uv.py](https://github.com/kinouwe/uwe-maya/blob/main/python/uv/uwe_overlap_uv.py)

とりあえずpython3環境にのみ対応しています。  
Python2環境も必要という念を感じたら用意するかも。

このファイルをMayaのscriptsフォルダに配置してください。  
デフォルトは`C:\Users\USERNAME\Documents\maya\scripts`

Pythonモードでスクリプトエディタに以下を入力して実行してください。
```python
 import uwe_overlap_uv
 uwe_overlap_uv.gui()
 ```
シェルフに登録するのもコレ↑でOK


## 使い方
UV頂点選択モードで、スナップさせたいUVの近くになんとなく置きます  
[![Image from Gyazo](https://i.gyazo.com/thumb/240/28edf6d962a1f32526eb3cbe236e5f69.png)](https://gyazo.com/28edf6d962a1f32526eb3cbe236e5f69)

Overlap UVボタンを押します  
[![Image from Gyazo](https://i.gyazo.com/768a85466df17965b406031f81b8c238.png)](https://gyazo.com/768a85466df17965b406031f81b8c238)

もし以下のようなエラーが表示されたら、  
[![Image from Gyazo](https://i.gyazo.com/f61df322b7885c4ed0310904526442d6.png)](https://gyazo.com/f61df322b7885c4ed0310904526442d6)  
Thresholdってとこのスライダーを右にずずいと動かして数字をデカくしてください。  
この数字の範囲内でしか近傍頂点を探索しません。めっちゃ離れてるUV頂点は無視します（処理軽くしたいから

## 注意点
[![Image from Gyazo](https://i.gyazo.com/0ff02100da5e6f83bf0157ae4448e96f.png)](https://gyazo.com/0ff02100da5e6f83bf0157ae4448e96f)  
こんな感じでねじれかけてるUVがあった場合、重なる先のUVが事故ることがあります

[![Image from Gyazo](https://i.gyazo.com/283715e758e21b1f7b20654f5eb69280.png)](https://gyazo.com/283715e758e21b1f7b20654f5eb69280)  
事故ったパターン

[![Image from Gyazo](https://i.gyazo.com/9ddbdabb114e63d20ee0a0e67213a76f.png)](https://gyazo.com/9ddbdabb114e63d20ee0a0e67213a76f)  
なので結果の精度を上げたいときはあらかじめいい感じにシルエットは合うようにしてください


## 実際に使っているところの雰囲気  

<video controls src="https://i.gyazo.com/7b75833c0bdc5bc564c9910f41e7cd10.mp4" title="[https://gyazo.com/7b75833c0bdc5bc564c9910f41e7cd10]"></video>


## ライセンス

ライセンスはMITです。  
本ツールを使用したことによる如何なる結果にも私は責任を負いません。
