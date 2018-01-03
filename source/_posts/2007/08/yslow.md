---
title: YSLOW 勉強 &#x3a; まとめ
date: 2007-08-18T16:29:00.000Z
categories:
- web
tags:
- yslow
---
*   [1 : HTTPのリクエストを最小限にしよう](/blog//2007/08/yslow_1_minimize_http_requests/)
*   [2 : CDNを利用しよう](http://memolog.org/2007/08/yslow_2_use_a_content_delivery.html)

<!-- more -->
*   [3 : Expires Header を追加しよう](http://memolog.org/2007/08/yslow_3_add_an_expires_header.html)
*   [4 : Gzip 化しよう](http://memolog.org/2007/08/yslow_4_gzip_components.html)
*   [5 : CSSはページの上に配置しよう](http://memolog.org/2007/08/yslow_5_put_css_at_the_top.html)
*   [6 : スクリプトはページの下に配置しよう](http://memolog.org/2007/08/yslow_6_move_scripts_to_the_bo.html)
*   [7 : CSS expressions の使用は控えよう](http://memolog.org/2007/08/yslow_7_avoid_css_expressions.html)
*   [8 : CSSとscriptは外部ファイルにしよう](http://memolog.org/2007/08/yslow_8_make_javascript_and_cs.html)
*   [9 : DNS lookups を減らそう](http://memolog.org/2007/08/yslow_9_reduce_dns_lookups.html)
*   [10 : Javascriptを最小化しよう](http://memolog.org/2007/08/yslow_10_minify_javascript.html)
*   [11 : リダイレクトを控えよう](http://memolog.org/2007/08/yslow_11_avoid_redirects.html)
*   [12 : 重複するscriptを削除しよう](http://memolog.org/2007/08/yslow_12_remove_duplicate_scri.html)
*   [13 : ETags を設置しよう](http://memolog.org/2007/08/yslow_13_configure_etags.html)

YSLOWの勉強のまとめ。最後に自分の所感をまとめておきます。

YSLOWにおける13の評価基準を一つずつ見てきてわかったことは、YSLOWとは、HTTPの応答を減らせる余地があるかないかを評価するためのツールだということ。それは1の解説にあった「「ユーザーの待ち時間の大半は画像やCSS、javascript、Flashなどのページの構成要素のダウンロードに費やされている」という原則を根本としている。

評価基準はHTTPの応答を減らせるアイデアを13個連ねたといった体裁で、それぞれの難易度がまちまちです。[7 : CSS expressions の使用は控えよう](http://memolog.org/2007/08/yslow_7_avoid_css_expressions.html)のように比較的簡単なものから、[2 : CDNを利用しよう](http://memolog.org/2007/08/yslow_2_use_a_content_delivery.html)のように対応が開発的にも・コスト的にも難しいものまであるし、[10 : Javascriptを最小化しよう](http://memolog.org/2007/08/yslow_10_minify_javascript.html)のように、対応は難しくなくても、メンテナンスが猥雑になる懸念があるものもある。すべてを「A」にするよう努力するよりは、全体の利益とコストを鑑みて、ケースバイケースで最適な対応を考えるのが肝要なのかと思います。

13の評価基準をオペレーション作業とHTMLコーディング作業のふたつに分けるとしたら、[2](http://memolog.org/2007/08/yslow_2_use_a_content_delivery.html)、[3](http://memolog.org/2007/08/yslow_3_add_an_expires_header.html)、[4](http://memolog.org/2007/08/yslow_4_gzip_components.html)、[9](http://memolog.org/2007/08/yslow_9_reduce_dns_lookups.html)、[11](http://memolog.org/2007/08/yslow_11_avoid_redirects.html)、[13](http://memolog.org/2007/08/yslow_13_configure_etags.html)がオペレーション作業で、[1](http://memolog.org/2007/08/yslow_1_minimize_http_requests.html)、[5](http://memolog.org/2007/08/yslow_5_put_css_at_the_top.html)、[6](http://memolog.org/2007/08/yslow_6_move_scripts_to_the_bo.html)、[7](http://memolog.org/2007/08/yslow_7_avoid_css_expressions.html)、[8](http://memolog.org/2007/08/yslow_8_make_javascript_and_cs.html)、[10](http://memolog.org/2007/08/yslow_10_minify_javascript.html)、[12](http://memolog.org/2007/08/yslow_12_remove_duplicate_scri.html)はHTMLコーディング作業に分けられるかと思います。

HTMLコーディングを業務の一部にしていたものとしては、やはり後者の方がより興味がそそられました。どれもわりと普通のことが書かれている感がありますが、たとえば「大規模な集客を想定しているポータルサイトだから、画像の点数を減らしてサイトが重くならないようにしよう」とか、そういったソリューションを持ったHTMLコーディングなどを頭に妄想させていると、わくわくしますね。たぶん誰も気がつかないと思いますが、サーバーの負荷を少し減らして、そして最終的には地球に優しいHTMLになっている、はず（かなあ）。

最後に、この勉強を書き連ねている最中に見つけた、日本語でより詳細に記しているサイトを紹介しておこうと思います（勉強始める前に探しておけばよかった）。

*   [Webサイトの高速化 フロントエンドのパフォーマンスの重要性 (Yahoo! developer netoworkより翻訳) || パフォーマンスチューニングBlog: インターオフィス](http://www.inter-office.co.jp/contents/177)
