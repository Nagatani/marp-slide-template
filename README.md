# marp-theme-for-lecture

講義資料のスライドを作成する際に、パワーポイント使いたくないので作った。

## slide markdown sample

- [slides/my-presentation.md](slides/my-presentation.md)

## pdf sample

- [my-presentation.md.pdf](my-presentation.md.pdf)

## install 

```bash
$ npm ci
```

## usage

slides直下に`new-slide.md`を配置したとして、Marp用のMarkdownを書く

### start server

HTMLでのスライドデザインの確認や、VS Codeのプレビューがうまく設定できなかったときなどは、下記コマンドでローカルサーバーを立ち上げる

```bash
$ npm run serve
```

### generate html

```bash
$ npm run makehtml -file=new-slide.md
```

`dist/new-slide.md.html`が生成される

### generate pdf

```bash
$ npm run makepdf -file=new-slide.md
```

`dist/new-slide.md.pdf`が生成される

### run on WSL2 Ubuntu

WSL2のUbuntu環境の場合は、Google ChromeかChromiumを入れろと言われるので、下記インストール手順でインストールし、`CHROME_PATH`を通してからスクリプトを利用する

```bash
$ CHROME_PATH=/usr/bin/google-chrome; npm run makepdf -file=new-slide.md
```

#### install google-chrome to WLS2 Ubuntu

```bash
$ sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
$ sudo wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
$ sudo apt update
$ sudo apt install google-chrome-stable -y
```
