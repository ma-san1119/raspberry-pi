ATOMからgithubに書き込む方法
============================

---
やりたいこと
-----------

- atomでファイルを作り，Dropboxに保存。
- ファイルのgit管理をDropboxで行う。
- githubに上げる。githubのmarkdown機能に期待（だめ？）


さて，満足できるでしょうか？

---
操作(まだ理解したわけではない)
--------------------------

0. atomにmarkdown-preview-plusとmathjax-wrapperをインストールし，markdown-previewをdisableにする。
1. atomでファイルを作る。.mdファイル。
2. Ctrl-) でgit画面を開き，add, commitを行う。Dropboxに.gitができる。
3. ブラウザでgithubにログインし，raspberry-piフォルダを作る。
4. terminalでDropboxの.gitのあるフォルダに移動し，addする。Usernameとパスワードを聞かれるので入力。`$ git remote add origin https://github.com/ma-san1119/raspberry-pi.git`
5. つづいてpushする。`$ git push -u origin master`
6. atomで`ctrl-(`とするとgithubパネルが開くのでログインする。その際Tokenを求められるのでこれを生成し入力する。自動で案内されるので心配することはない。
7. atom右下のボタンでpushやらできる模様。
8. ブラウザのgithubにファイルが出てくるのでダブルクリックするとファイルが表示される。

しかしgithubに数式がうまく出ない！ (atomではうまく出た。)
あたまに
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
をつければいいらしい。

$$
y=\int_{-\infty}^{\infty} x^2 dx
$$
