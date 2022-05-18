---

theme: default

---
<!-- _footer: "※思想強めなので話半分で聞いてください※" -->

# Vim Is All You Need

<div style="text-align: right">岩崎悠紀</div>

---
<!-- paginate: true -->

# みなさんエディタは何を使っていますか？

- VScode
- Jetbrain（IntelliJ, PyCharm）
- ~~emacs~~

---

# ではこういう場合どうしますか？

### ある文字列を""で囲みたい...

```c
printf(hogehoge) //これを
```

```c
printf("hogehoge") //こうしたい
```

カーソルが一番左の「h」にあるとき、「"⇨\<bs\>⇨⇨⇨⇨⇨⇨⇨⇨"」とか（またはショートカット）

---

# 矢印キー、遠くないですか？

vimだったらこの処理、「ysiw"」で可能です。（基本的にホームポジション）
遥か彼方の矢印キーを押しに行かずに済みます。

他にも
```c
hogehoge // これを
↓
printf(hogehoge) // 「ysiwfprintf<CR>」
↓
printf("hogehoge") // 「fhysiw"」
↓
printf(something("hogehoge")) // 「f"ysa"fsomething<CR>」
```

---

# でもVimだけじゃ限界があるでしょ？

---
<!-- _footer: "https://github.com/junegunn/fzf" -->

### Q. どうやってファイル開くの？
### A. 安心してください。Fzf(ファジーファインダー)があります。

![height:350px](https://raw.githubusercontent.com/junegunn/i/master/fzf-preview.png)

---
<!-- _footer: "https://github.com/tpope/vim-fugitive, https://advancedweb.hu/dive-into-git-history-with-fugitive-vim/" -->

### Q. どうやってGitを使うの？
### A. 安心してください。Fugitiveがあります。

Vim上で「:G add hoghoge.txt」などのコマンドを打つことができます。

![height:300px](https://advancedweb.hu/assets/posts/fugitive-vim-gblame/gblame-cb306be4ddcc3e62e9eb5aed98a1b8de9e1052db9f5faceccb2278cdff958699.gif)

---
<!-- _footer: "https://github.com/prabirshrestha/vim-lsp" -->

### Q. どうやって補完するの？
### A. 安心してください。vim-lspがあります。

![height:350px](/Users/202204004/ghq/github.com/IwasakiYuuki/slides/marp/vim-tmux-vimium/img/completion.png)

---
<!-- _footer: "https://qiita.com/reireias/items/5364dcaada1a5b88a206" -->

### Q. どうやってLint, Formatするの？
### A. 安心してください。ALEがあります。

![height:350px](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F214526%2F41aae68e-4c07-f861-c1b0-6b8c3ec31765.gif?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&w=1400&fit=max&s=4fe40ba51b2b451ca63fd15ddc3764a8)

---

# 色々できるのはわかった...
# けどターミナル使えないと不便じゃない？
### 安心してください。Tmuxがあります。

---

# Tmux

Terminalの画面を分割、セッション単位で管理することができるツール。

![height:350px](/Users/202204004/ghq/github.com/IwasakiYuuki/slides/marp/vim-tmux-vimium/img/tmux.png)

---

# でもこれに慣れちゃうとその他の操作が辛い...

---
<!-- _footer: "https://github.com/jeffreytse/zsh-vi-mode" -->

# じゃあその他の操作もVimにすればいい（解決）

### Zsh-vi-mode

![height:350px](https://user-images.githubusercontent.com/9413601/105746868-f3734a00-5f7a-11eb-8db5-22fcf50a171b.gif)

---
<!-- _footer: "https://qiita.com/okamu_/items/d9ee9cdc1b5005a0cf1c" -->

# じゃあその他の操作もVimにすればいい（解決）

### Vimium（Chrome）

![height:350px](https://qiita-image-store.s3.amazonaws.com/0/62822/8464ff34-c152-a718-43e6-17d7937495da.gif)

---
<!-- _footer: "https://qiita.com/ta9star/items/da9af53c4bf542d3ae7a" -->

# じゃあその他の操作もVimにすればいい（解決）

### Marp（スライド作成）

![height:350px](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/247753/be754770-c055-d9f5-fa62-7068d59d4f84.gif)

---

# 最後に

開発スピードが上がるか、と言われると、正直微妙だと思います。
本気で極めないと上がらないかも。
僕自身まだ初心者レベルなので全然上がっていないです。（元はIntelliJ使ってました。）

ただ、マウスを触らないのでストレスフリーになったという感想です。
（分離型キーボードの人はさらに恩恵があるかも）

---

# 余談

先ほど説明したVimiumは、SpreadSheetやNotionといったWebアプリケーションと非常に相性が悪いです。
なので、マウスを使わざるおえない時が結構あります...

あと、僕の環境の設定ファイルが以下に置いてあるので、Vimをこれから触る人はもしかしたら参考になるかも。
https://github.com/IwasakiYuuki/dotfiles
