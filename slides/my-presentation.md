---
marp: true
paginate: true
theme: base
footer: 大学名や講義名などを書く予定。著作権表示でも良いかも
---

<!--
_class: title
_paginate: false
-->


# Sample of lecture slides
## 講義名などをここに書きたい
他に何か書きたい場合はこちらに書きます。

![bg cover](images/title-bg.svg)

---

# 目次

1. 書式サンプル
2. コード貼り付け
3. 長文書いたり注釈入れたり
3. WSL2環境下のあれこれ

---
<!-- _header: 書式サンプル -->

## 見出し2 （Hedding2）
### 見出し3 （Hedding3）
#### 見出し4 （Hedding4）
##### 見出し5 （Hedding5）
###### 見出し6 （Hedding6）

- テキストのサンプルです。 
  - ***強調文字*** : `**強調文字**`
  - **強調文字** : `**強調文字**`
  - *斜体* : `*斜体*`
  - ~~訂正線~~ : `~~訂正線~~`
  
---
<!-- _header: コード貼り付け -->

## Hello, World!!

下記コードを`HelloWorld.java`というファイル名で保存します。

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!!");
    }
}
```

上記コードを保存したディレクトリにカレントディレクトリを移動し、下記コマンドでコンパイル後、動作確認をしましょう。

```bash
$ javac HelloWorld.java
$ java HelloWorld
```


---
<!-- _header: ちょっとはみ出る長文書いたり注釈入れたり -->
## ダミーテキスト
現代社会においては、情報の収集や発信が容易になり、様々な情報が瞬時に共有されるようになりました。しかし、その一方で、情報の過剰な量や真偽の確認が困難な情報も多くなっています。特に、SNSの普及により、情報の拡散がより迅速になり、誤った情報が拡散されることも少なくありません。このような中で、情報リテラシーがますます重要視されるようになってきています。

情報リテラシーとは、情報を扱う能力であり、信頼できる情報を選別し、正しく活用する力を指します。情報リテラシーを持つことは、個人の判断力や問題解決能力を向上させるだけでなく、社会全体の情報の質を高めることにもつながります。例えば、政治や社会問題に関する情報を扱う場合、正確な情報を入手し、それを正しく評価する能力が求められます。また、ビジネスの分野でも、信頼性の高い情報を収集し、それを基に的確な判断を下すことが必要です。

情報リテラシーを身につけるためには、情報源を選別し、情報の真偽を判断する能力が必要不可欠です。インターネット上には、様々な情報が存在していますが、その中には誤った情報や偏った情報も多くあります。情報源を信頼性の高いものに限定し、情報の真偽を確認することが重要です。また、情報を取り扱う際には、情報の出所や意図を考慮することも大切です。情報がどのような目的で発信されたのかを確認し、その情報がどのような影響をもたらす可能性があるのかを考えることが必要です。

情報リテラシーは、今後ますます必要とされるスキルの一つとなっています。情報リテラシーを身につけることで、個人の能力や社会全体の情報の質が向上し、より良い社会を作ることができます。$^{*1}$

> 1. Create by Chat-GPT 3.5 [https://chat.openai.com/](https://chat.openai.com/)

---


<!--
_class: subtitle
_paginate: false
-->

# セクションタイトル

---
<!-- _header: WSL2 UbuntuはChromeから入れる -->

## install google-chrome to WLS2 Ubuntu

```bash
$ sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
$ sudo wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
$ sudo apt update
$ sudo apt install google-chrome-stable -y
```

WSL2のUbuntu環境の場合は、Google ChromeかChromiumを入れろと言われるので、上記インストール手順でインストールし、`CHROME_PATH`を通してからスクリプトを利用する

```bash
$ CHROME_PATH=/usr/bin/google-chrome; npm run makepdf -file=my-presentation.md
```


---

# [Image syntax](https://marpit.marp.app/image-syntax)

You can resize image size and apply filters through keywords: `width` (`w`), `height` (`h`), and filter CSS keywords.

```markdown
![width:100px height:100px](image.png)
```
![w:100px h:100px](images/bg-photo001.jpg)

```markdown
![blur sepia:50%](filters.png)
```
![w:100 h:100 blur sepia:50%](images/bg-photo001.jpg)


Please refer [resizing image syntax](https://marpit.marp.app/image-syntax?id=resizing-image) and [a list of CSS filters](https://marpit.marp.app/image-syntax?id=image-filters).

---

# Background image

You can set background image for a slide by using `bg` keyword.

```markdown
![bg opacity](images/bg-photo001.jpg)
```

![bg opacity](images/bg-photo001.jpg)

---

## Multiple backgrounds

Marp can use multiple background images.

```markdown
![bg blur:3px](https://fakeimg.pl/800x600/fff/ccc/?text=A)
![bg blur:3px](https://fakeimg.pl/800x600/eee/ccc/?text=B)
![bg blur:3px](https://fakeimg.pl/800x600/ddd/ccc/?text=C)
```

![bg blur:3px](https://fakeimg.pl/800x600/fff/ccc/?text=A)
![bg blur:3px](https://fakeimg.pl/800x600/eee/ccc/?text=B)
![bg blur:3px](https://fakeimg.pl/800x600/ddd/ccc/?text=C)

---

## Multiple backgrounds(vertical)

```markdown
![bg vertical blur:3px](https://fakeimg.pl/800x600/fff/ccc/?text=A)
![bg blur:3px](https://fakeimg.pl/800x600/eee/ccc/?text=B)
![bg blur:3px](https://fakeimg.pl/800x600/ddd/ccc/?text=C)
```

![bg vertical blur:3px](https://fakeimg.pl/800x600/fff/ccc/?text=A)
![bg blur:3px](https://fakeimg.pl/800x600/eee/ccc/?text=B)
![bg blur:3px](https://fakeimg.pl/800x600/ddd/ccc/?text=C)

---

## background

```markdown
![bg right](image.jpg)
```

![bg right](images/bg-photo001.jpg)

<!-- _footer: "*Photo by [Midjourney](https://midjourney.com/home/)*" -->

---

## Fragmented list

Marp will parse a list with asterisk marker as the fragmented list for appearing contents one by one.

```markdown
# Fragmented list

* One
* Two
* Three
```

# Fragmented list Sample
* One
* Two
* Three

---

## Math typesetting

[KaTeX](https://katex.org/) math typesetting such as $ax^2+bc+c$ can use with [Pandoc's math syntax](https://pandoc.org/MANUAL.html#math).

$ax^2+bc+c$

```tex
$ax^2+bc+c$
```

$$I_{xx}=\int\int_Ry^2f(x,y)\cdot{}dydx$$

```tex
$$I_{xx}=\int\int_Ry^2f(x,y)\cdot{}dydx$$
```

---

## Auto-scaling

*Several built-in themes* are supported auto-scaling for code blocks and math typesettings.

```text
Too long code block will be scaled-down automatically. ------------>
```
```text
Too long code block will be scaled-down automatically. ------------------------>
```
```text
Too long code block will be scaled-down automatically. ------------------------------------------------>
```
```text
Too long code block will be scaled-down automatically. ------------------------------------------------------------------------>
```

---

## [Scoped style](https://marpit.marp.app/theme-css?id=scoped-style)

If you want one-shot styling for current page, you can use `<style scoped>`.

```markdown
<style scoped>
a {
  color: green;
}
</style>

- [Green link!](https://marp.app/)
```

<style scoped>
a { color: green; }
</style>

- [Green link!](https://marp.app/)

