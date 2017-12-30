---
title: hello hexo
date: 2017-12-30 13:38:05
tags:
---

[Gatsby](https://www.gatsbyjs.org/)はなかなかに高機能で素晴らしく、React、GraphQL、PWAなど技術的なプレイグラウンドとしても魅力的だったのだけど、それゆえにたとえばデザインを少し変えたいというときに、[Typography](http://kyleamathews.github.io/typography.js/)の実装上でどう変更するかを調べる必要があったり、[react-responsive-grid](https://github.com/KyleAMathews/react-responsive-grid)とかバンドルされてるReact Componentがどんな実装になっているかを確認したりとか、とにかく面倒くさい。この最初のラーニングカーブを乗り切ってしまえば便利なのかもしれないけど、メモ書きサイトを作るのにあまり時間をかけたくない（でもデザインは調整したい）という目的には、どうもオーバースペック感があった。あとpublicに生成されるファイルが変に多くて把握しにくいし、LightHouseのPerformanceのスコアも70前後（十分だけど）なのが少し気になった。

なので、何か別のスタティックサイトジェネレーターを使おうと思っていろいろ探した。[preact cli](https://github.com/developit/preact-cli)からのサイト生成も良さそうだったけど、この状態から個別のページを生成する実装を作るのはだいぶ面倒くさそうだったので諦めた。[jekyll](https://jekyllrb.com/)は必要十分な感じはあるけど実装がRubyなので、できればNode.jsで実装されているものを使いたい。

それで結局[Hexo](https://hexo.io/)を試している。今のところ簡単にスタティックサイトを作成したい（学習コストは低めに）という目的に十分あっているような気はしている。