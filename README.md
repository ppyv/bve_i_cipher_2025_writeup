# Writeup

## Question 1

### 問題

> TIBERIVS CLAVDIVS CAESAR says
> 
> "20250401/KvvTxqi/OdvrXrzzf/GffpvNsziqy/Qodrgt
> 
> *DGG ".kwpo""

### 解法
あぶり出しで
```
TIBERIVS CLAVDIVS CAESAR says

"20250401/KvvTxqi/OdvrXrzzf/GffpvNsziqy/Qodrgt
*HAFOXGH FDSLWDO OHWWHUV.
*DGG ".kwpo""



ただし、"http://bveiweb.aikotoba.jp/"の直後に答えを書くこと。 Hint: 数字は変化しない
```
を得る。

シーザー暗号であり、 https://www.dcode.fr/caesar-cipher などに通すと右に3シフトで次を得る。

```
"20250401/HssQunf/LasoUowwc/DccmsKpwfnv/Nlaodq
*EXCLUDE CAPITAL LETTERS.
*ADD ".html""
```

注釈として「大文字を除け」「`.html`をつけろ」とあるので、すなわち解答は http://bveiweb.aikotoba.jp/20250401/ssunf/asoowwc/ccmspwfnv/laodq.html である。

## Question 2

### 問題
画像である。

### 解法
これをダウンロードし、 `p2q.png` を得る。この画像には、最下部に模様が視認でき、ステガノグラフィであることを疑わせる。

ヒントを読むと、「暗号を解く方法、道具の名前は、すでに示してあります。」とある。
ここで、他と異なり、赤線引きになっている文字はノガテス、斜体になっている文字はハツネである。
赤線引きは逆から読むとステガノであり、国産のステガノグラフィソフトウェアとして[初音](https://www.vector.co.jp/soft/win95/util/se309150.html)が存在する。これをダウンロードする。

解除モードで偽装済みPNGファイルに `p2q.png` を、出力ディレクトリに任意のディレクトリを指定し、パスワード欄は空欄のまま実行する。出力ディレクトリに `ans2.txt` を得る。

`ans2.txt` の内容は次の通りである。
```
1. 6ｺある ｷ の文字色のカラーコードを求め、出てきた順に並べる。
※出てきた順は普通に ｷ が出てきた順。文を読む順で。最初は62...と続く
※色抽出は拡大して丁寧に行うことを強く勧める。
2. 並べた16進数を文字列に変換。（これを以降 文字列Sと呼ぶ）
3a. 画像に隠れている4桁の素数2つを掛けた後、それに9を足す（この数を以降3aと呼ぶ）
3b. 3aに9を掛ける（この数を以降3bと呼ぶ）
4. http://bveiweb.aikotoba.jp/20250401/に続けて、 文字列S/3a/3b/13000.html を記載する
これが答え。
```

任意のペイントソフトウェアで `p2q.png` を開き、指示通りｷのカラーコードを抽出する。順に626561, 646763, 662F62, 656164, 676265, 2F6762である。これを連結した `626561646763662F626561646762652F6762` を https://www.dcode.fr/ascii-code に通し、16進 (HEX) からの変換として文字列S `beadgcf/beadgbe/gb` を得る。

次に「画像に隠れている4桁の素数」とは、画像の縦横の大きさのことである（縦1861ピクセル、横1237ピクセル）。これをかけて9を足し、3aとして2302066を得る。

次に3aに9をかけ、20718594を得る。

従って解答は http://bveiweb.aikotoba.jp/20250401/beadgcf/beadgbe/gb/2302066/20718594/13000.html である。

## Question 3

### 問題

> b=2(6), f=10(6), r=30(6), y=41(6)であるとき
> 
> 
> 文字列αを 42(6) 14(6) 1(6) 22(6) 5(6) 14(6) 13(6) 3(6) 34(6) 13(6) 13(6) 20(6) 31(6)
> 
> 文字列βを 4(6) 1(6) 4(6) 20(6) 24(6) 20(6) 4(6)
> 
> 文字列γを 42(6) 21(6) 15(6) 15(6) 42(6) 10(6) 2(6)
> 
> 文字列δを 2(6) 41(6) 1(6) 42(6) 10(6) 33(6) 1(6) 31(6)
> 
> とする。
> 
> 次のページのurlは
> 
> http://bveiweb.aikotoba.jp/20250401/文字列α/文字列β/文字列γ/文字列δ.html
> 
> である。

### 解法

あぶり出しで
```
ヒント: html = 12(6) 32(6) 21(6) 20(6) である。
```
を得る。

1行目の「b=2(6), f=10(6), r=30(6), y=41(6)であるとき」より、右辺についてこのような記数法をするのは底を明示する場合であるので、6を底とする位取り記数法（6進法）であると仮定する。このとき、それぞれ2, 6, 18, 25となる。左辺に注目すると、bはアルファベットの2番目の文字、fは6番目の文字、rは18番目の文字、yは25番目の文字であるから一致する。

これに基づいてα、β、γ、δの4つの文字列を書き下すと、次のようになる。
```
α: 26 26 26 10 48 16 18 60
β: 26 16 10 58 60
γ: 49 36 19 38 10 58 60
δ: 19 20 10 37 16
```

ゆえに、解答は http://bveiweb.aikotoba.jp/20250401/zjanejicviils/dadlpld/zmkkzfb/byazfuas.html である。

## Question 4A

### 問題


> TIBERIVS CLAVDIVS CAESAR says
> 
> " \xG80F\xGI87\xG80F\xGIII \xG80F\xGI87\xG80F\xGIII \xG80F\xGI87\xG80F\xGIII \xG80F\xGI86 \xG80F\xGI89\xG80G\xGF01 \xG80F\xGI86\xG80F\xGIII \xG80F\xGI86\xG80G\xGF01 \xG80F\xGI8E
> 
> \xG80F\xGI87\xG80F\xGIII \xG80F\xGI86\xG80F\xGIII \xG80F\xGI86 \xG80F\xGI8D\xG80G\xGF01 \xG80F\xGI8E
> 
> \xG80F\xGI89\xG80G\xGF02 \xG80F\xGI88\xG80F\xGIII \xG80F\xGI86\xG80G\xGF02 \xG80F\xGI88\xG80G\xGF01 \xG80F\xGI86 \xG80F\xGI8D\xG80G\xGF01 \xG80F\xGI8E
> 
> \xG80F\xGI86\xG80G\xGF02 \xG80F\xGI87 \xG80F\xGI86 \xG80F\xGI88\xG80G\xGF00 \xG80F\xGI86\xG80F\xGIII "
> 
> 
> ヒント：数字・記号は復号しない。


### 解法

あぶり出しで次を得る。
```
最初に/20250401/までを記載。最後に.HTMLを記載。
```

また、 `title` タグより、次を得る。
```
【A】 SrfnhwEho→Qxp
```

まず問題文に `\x` で始まる6桁の文字列が規則正しく並んでいることから、これはUnicodeエスケープシーケンス（`\u` で始まり、16進の4文字が続く）に写されることを想定する。

シーザー暗号としたとき、 `\u` で始まるように写されるのは右に3文字シフトであり、次を得る。
```
\uD80C\uDF87\uD80C\uDFFF \uD80C\uDF87\uD80C\uDFFF \uD80C\uDF87\uD80C\uDFFF \uD80C\uDF86 \uD80C\uDF89\uD80D\uDC01 \uD80C\uDF86\uD80C\uDFFF \uD80C\uDF86\uD80D\uDC01 \uD80C\uDF8B

\uD80C\uDF87\uD80C\uDFFF \uD80C\uDF86\uD80C\uDFFF \uD80C\uDF86 \uD80C\uDF8A\uD80D\uDC01 \uD80C\uDF8B

\uD80C\uDF89\uD80D\uDC02 \uD80C\uDF88\uD80C\uDFFF \uD80C\uDF86\uD80D\uDC02 \uD80C\uDF88\uD80D\uDC01 \uD80C\uDF86 \uD80C\uDF8A\uD80D\uDC01 \uD80C\uDF8B

\uD80C\uDF86\uD80D\uDC02 \uD80C\uDF87 \uD80C\uDF86 \uD80C\uDF88\uD80D\uDC00 \uD80C\uDF86\uD80C\uDFFF
```

これを https://dencode.com/string/unicode-escape などのツールで変換すると、次を得る。
```
𓎇𓏿 𓎇𓏿 𓎇𓏿 𓎆 𓎉𓐁 𓎆𓏿 𓎆𓐁 𓎋

𓎇𓏿 𓎆𓏿 𓎆 𓎊𓐁 𓎋

𓎉𓐂 𓎈𓏿 𓎆𓐂 𓎈𓐁 𓎆 𓎊𓐁 𓎋

𓎆𓐂 𓎇 𓎆 𓎈𓐀 𓎆𓏿
```

これらはヒエログリフの数字であり、𓏺が1つで1、𓎆が1つで10を表す。この関係性から、次に写される。
```
26 26 26 10 48 16 18 60
26 16 10 58 60
49 36 19 38 10 58 60
19 20 10 37 16
```

このとき、 `title` タグの文字列をシーザー暗号として右に3字シフトすると、`【X】 PocketBel->Num` を得る。このことから、先の文字列はポケベル入力における換字表に通すことが示唆される。

Web検索で得られる換字表や変換ツールにより、先の数値は次に写される。
```
FFFERAC/
FAEW/
SKDMEW/
DJELA
```

ここにあぶり出しより `.HTML` を付加し、中間解答 https://bveiweb.aikotoba.jp/20250401/FFFERAC/FAEW/SKDMEW/DJELA.HTML を得る。


## Question 4B

### 問題

画像である。フィンランド語が表示される。

### 解答

この画像ファイルをダウンロードする。直接はダウンロードできないようにされているため、ソースコードを開き、CSSで参照されている画像ファイルに直接アクセスし、ダウンロードする。 `ba.png` を得る。

ここでも画像にランダムなノイズが乗っていることから、初音に通す。これにより、 `HEX.png` を得る。

`HEX.png` をstringsコマンド（Linux向け。Windows向けには別途準備されたい）に通す。PNGのファイル終了を意味する `IEND` の後より、URLに展開できそうな文字列 `thbb://pdqweqp.iuywfcjm.xx/20250401/qfmrtke/rnho/eqfzrq/y5shn.thux` を得る。

httpとおぼしきところがthbbに写されていること、jpとおぼしきところがxxに写されていることから、シーザー暗号ではないことが分かる。また、htmlとおぼしきところがthuxに写されており、ある周期でhがtに、tがhに写されることが分かる。すなわち多表式の換字式暗号であることを想定する。

多表式の換字式暗号としてはヴィジュネル暗号が最もポピュラーであることから、これを試行する。 https://www.dcode.fr/vigenere-cipher のVigenere ciphertext欄に上記文字列を置く。

ここで問題の画像を見ると、 `HEX.png` に描かれている鍵の画像と `moi` の文字が同じ色で描かれていることがわかる。Knowing the Key/Passwordを選択して `MOI` を入力し、DECRYPTを押す。Results欄に中間解答 http://bveiweb.aikotoba.jp/20250401/ereffcs/dfva/werrfc/q5gtf.html を得る。

### 別解

平文が `http://bveiweb.aikotoba.jp/20250401/*******/****/******/*****.html` であると想定されることから、既知平文攻撃を行う。dCodeにおいてKnowing a plaintext wordを選択し、 `bveiweb.aikotoba` を入力する。これによって鍵 `MOIMOI` を得る。

改めて、 Knowing the Key/Passwordを選択し `MOIMOI` を入力すると、中間解答 http://bveiweb.aikotoba.jp/20250401/ereffcs/dfva/werrfc/q5gtf.html を得る。

実際の鍵は `MOI` であるが、ヴィジュネル暗号は平文に対して鍵を繰り返し適用するため、同じ文字列の繰り返しである鍵 `MOIMOI` でも問題なく復号できる。

## Question 4C

### 問題

背景画像の上に、次の文字列が表示される。

> wktktkwktkwkwkwkwktktktkwktkwkwkwktktktkwktkwkwkwktktktkwkwkwkwkwkwktktktkwktkwkwkwktkwktktktktkwkwktkwktktktktkwktktkwkwkwktkwkwktktktkwktktkwkwktktkwkwktkwktkwktktkwktkwkwktkwktktktkwktktktkwktktkwkwktkwktkwktktkwkwkwktkwkwkwktkwktktktkwkwktktkwkwkwkwktkwktktkwktkwkwktkwktktkwktkwktktkwktktkwktktktktkwktktktkwktkwkwkwktktkwktktktktkwktktkwkwkwktkwkwktktkwkwkwkwktkwkwktkwktktktkwkwktktkwktkwktkwkwktktktkwkwkwkwkwkwktkwktktktktkwkwktktkwkwktkwkwkwktktkwkwkwkwkwkwktktkwkwktkwkwkwktktkwktkwktkwkwktktkwkwkwkwkwkwktktkwktkwkwkwkwktktkwkwkwkwkwkwktktkwkwkwktkwkwktkwktktktktkwktktkwkwktkwktkwktktktkwkwktkwkwktktkwkwktkwktkwktktkwkwktktkwkwktktkwkwktktkwkwktktkwkwkwktktkwktktktkwkwktktkwkwktkwktktktktkwktktkwkwktkwkwkwktktkwkwktktkwkwktktktkwktktkwkwktktkwkwkwkwktkwkwktkwktktktktkwktktktkwktktktkwktktkwkwktkwktkwktktktkwkwktkwkwktktktkwkwktkwkwktktkwkwktktkwkwktktkwkwkwktktkwkwktkwktktktktkwktktktkwkwktktkwktktktkwktktktkwkwktkwktktktktkwktktkwkwkwktktkwktktkwkwkwkwktkwkwktkwktktktktkwktktktktkwktkwkwkwktktkwkwkwktkwkwktkwktktktktkwkwktktkwkwkwkwkwkwktktkwkwktkwkwktktkwkwkwkwktkwkwktkwktktktkwkwktktkwktkwkwkwkwktktktkwktkwkwkwktktkwktktkwktkwktktkwktktkwkwkwkwkwkwktktkwktkwkwkwkwktkwktkwk

### 解答

三度に渡ってステガノグラフィの存在を暗示する画像が表示されるので、ソースコードからダウンロードする。
`kdwvxqh.png` を得る。

これを初音に通すと、 `wkwktktk.zip` を得る。

同封されている `README!!!.txt` の内容は次の通り。

```
2025/03/27作成 ・　2025/04/01公開


■はじめに・・・

ダウンロードありがとうございます。
そして、よくぞここまでたどり着きました！


このアプリは、例のwktkを解読するコンソールアプリです。



■使用方法

☆使用の前に、Microsoft Windows デスクトップ ランタイム8.0  は入れておいてください。
・展開して実行します（ウイルススキャンで引っかかるかもしれませんが、実行する場合は設定いじったりして何とか下さい！）
・起動して、入力。そして実行ボタンを押すだけです。（見ればすぐわかると思います！）



■削除方法　

このフォルダごと消してください。



■注意事項及び免責

・改造・解析・再配布はご自由にどうぞ。（しても意味ないけど。）

☆本ソフトを使用しての直接的、二次的被害についての責任は一切負いません。



■最後に

ここまで本当にお疲れさまでした。
今年の暗号が簡単だったとか、難しかったとか・・・人や団体によって感じ方は様々でしょう。
しかし、ここまで来たならもう全て解けたも同然ですから。
あと僅かです。頑張ってください。
```

`wkwktktk.exe` を起動し、画面上に表示されていた文字列を入力する。次を得る。

```
011010000111010001110100011100000011101000101111001011110110001001110110011001010110100101110111011001010110001000101110011000010110100101101011011011110111010001101111011000100110000100101110011010100111000000101111001100100011000000110010001101010011000000110100001100000011000100101111011001010111001001100101011001100110011001100011011100110010111101100100011001100111011001100001001011110111011101100101011100100111001001100110011000110010111101110011011101110010111101100011011000010010111101111010001100010010111100110000001100100110000100101110011010000111010001101101011011000000110100001010
```

https://www.dcode.fr/ascii-code の ASCII ciphertext (decimal, hexadecimal, etc.) にこれを張り付けてDECRYPT/CONVERT ASCIIを押す。
ResultsのBIN /8欄に解答 http://bveiweb.aikotoba.jp/20250401/ereffcs/dfva/werrfc/sw/ca/z1/02a.html を得る。
