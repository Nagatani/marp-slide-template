# marp-slide-template


> **Warning**
> 未だメンテ中です。

## pdf sample

[PDF sample](my-presentation.md.pdf)

## install 

```bash
$ npm ci
```

## usage

slides直下に`my-presentation.md`を配置して、Marp用のMarkdownを書く

```bash
$ npm run makepdf -file=my-presentation.md
```

`dist/my-presentation.md.pdf`が生成される

WSL2のUbuntu環境の場合は、Google ChromeかChromiumを入れろと言われるので、下記インストール手順でインストールし、`CHROME_PATH`を通してからスクリプトを利用する

```bash
$ CHROME_PATH=/usr/bin/google-chrome; npm run makepdf -file=my-presentation.md
```


## memo: install google-chrome to WLS2 Ubuntu

```bash
$ sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
$ sudo wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
$ sudo apt update
$ sudo apt install google-chrome-stable -y
```
