---
title: YSLOW 勉強 &#x3a; 13&#x3a; Configure ETags
date: 2007-08-16T16:29:00.000Z
categories:
- web
tags:
- yslow
---
*   [13: Configure ETags](http://developer.yahoo.com/performance/rules.html#etags)

[rules for high performance web sites](http://developer.yahoo.com/performance/rules.html)の十三個目（最後）。ETags（Entity Tags）を設定しよう。ブラウザが持ったキャッシュが古いかどうかを判断するための情報として、構成要素（component：画像とかスクリプトとか）のバージョンをETagで特定させることで、last-modified（修正日）よりも柔軟（で確度の高い）情報を提供することができる。

<!-- more -->

ETagにおける問題は、サーバーを特定させるような属性で（ETagが）構成されていると、複数台のサーバーで運用している場合に、キャッシュしたサーバーと、再度アクセスしたときのサーバーのEtagが異なるために、304（not modified）ではなく200のレスポンスを返してしまうということ。

複数台で運用しているウェブサービスで、ETagがサーバーを特定させるような書式になっている場合は（デフォルトの書式ではサーバーを特定させるような状態になっている）、ETagを利用すると返って動作が遅くなってしまう。ETagの恩恵に授かれない場合には、ETagを削除してしまった方がいい。
