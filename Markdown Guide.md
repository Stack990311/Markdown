# Markdown 基础

- [Markdown 基础](#markdown-基础)
  - [为什么要用markdown？](#为什么要用markdown)
  - [Markdown引言](#markdown引言)
  - [Markdown举例](#markdown举例)
  - [Markdown语法](#markdown语法)
- [标题](#标题)
- [一级标题](#一级标题)
  - [二级标题](#二级标题)
          - [六级标题](#六级标题)
      - [加粗和斜体](#加粗和斜体)
    - [Lists 列表](#lists-列表)
    - [Links 链接](#links-链接)
    - [Images 图片](#images-图片)
    - [Inline Code 行内代码](#inline-code-行内代码)
    - [Code Blocks 代码块](#code-blocks-代码块)
    - [Tables 表格](#tables-表格)
  - [对文件路径的理解](#对文件路径的理解)
  - [其他注意事项](#其他注意事项)
  - [Markdown工具介绍](#markdown工具介绍)
    - [macOS](#macos)
      - [Typora](#typora)
      - [VS Code](#vs-code)
      - [Xcode 略](#xcode-略)
      - [其他](#其他)
  - [文字编辑效率upup](#文字编辑效率upup)
  - [用Markdown编辑数学公式（From LaTex）](#用markdown编辑数学公式from-latex)
    - [希腊字母表](#希腊字母表)
    - [运算](#运算)
      - [简单运算](#简单运算)
      - [复杂运算](#复杂运算)
      - [基本初等函数](#基本初等函数)
      - [点缀](#点缀)
      - [二元关系](#二元关系)
      - [For Entertainment](#for-entertainment)
      - [箭头](#箭头)
      - [包裹结构](#包裹结构)
    - [括号](#括号)
    - [Vector向量](#vector向量)
      - [方程组](#方程组)
  - [文档布局](#文档布局)
    - [空格](#空格)
    - [紧缩](#紧缩)
    - [字号](#字号)
    - [字体](#字体)
  - [总结](#总结)

* [总结](#总结) 
## 为什么要用markdown？
> word格式太多，开发者不需要
> word是二进制文件，后缀为.doc or .docx，机器0和1存储文字样式，而某些内容只有word才能打开
> word无法用Git进行逐行管理，操作成本和存储成本过高
> 纯文本文件.txt以字符形式存储，最后跟上文字结束符EOF，读取速度比word快得多
> 纯文本文件不带格式，大小也比word小得多



## Markdown引言

* Markdown给纯文本带来格式，也可以将其看作简单的Html
* 文字是很常见的一种表达方式，用`txt`文件就可以在计算机中方便的呈现文字；我们也说了格式是可以增强文本的表现力的，比如用Word给这些文字添加格式。但问题是单单`txt`的表现能力捉急，Word中添加格式的操作成本、存储成本都太高了,由于`.docx`文件是二进制文件，其无法用Git进行逐行管理），能不能找到二者的平衡呢？

有，这个东西就是`Markdown`。

`Markdown`其实是一种写作风格/方式，我们用这种风格/方式写出来的纯文本文件（和`.txt`是一样的）叫做markdown文件，一般以.md作为文件后缀（而不是`.txt`）。.md文件虽然是纯文本，但其中用一些特殊的字符（如`* # [] ()` …）给纯文本带来格式（这与`html`文件是相似的，也可以将`markdown`看作是简单的`html`）。这些格式通过某种方式进行渲染（注：渲染：指将计算机中的某些数据呈现在屏幕上）你就可以看到它们代表的格式了！

## Markdown举例
 * 几乎每个Github仓库都有README.md对仓库进行说明
 * 方便格式管理，极大提高写作效率
 * 利用vscode & Markdown在网上写笔记很爽
 * Markdown支持代码注释风格

## Markdown语法

# 标题
```markdown
# 一级标题
## 二级标题
.....
###### 六级标题
```
# 一级标题
## 二级标题
.....
###### 六级标题

#### 加粗和斜体
```
 *This text will be italic*
 _This will also be italic_
 
    **This text will be bold**
    __This will also be bold__

    _you can **combine** them_
    ***you can also be bold & italic***
```

*This text will be italic*
 _This will also be italic_
 
**This text will be bold**
__This will also be bold__

_you can **combine** them_
***you can also be bold & italic***

### Lists 列表
unordered 无序列表
```
* Item1
* Item2
    * Item 2a
    * Item 2b
```
* Item1
* Item2
    * Item 2a
    * Item 2b

### Links 链接
``[Text](url)``：中括号，后面小括号，中括号里必须放链接；不需要说明的话，可以直接写链接
```
[GitHub Official Site](heeps://github.com)
https://github.com
<https:github.com>
```
[GitHub Official Site](https://github.com)
https://github.com
<https://github.com>

### Images 图片
```![Text](url)```：感叹号，中括号（说明，但不必须），小括号（图片链接）

`![Github Logo](https://github.com/fluidicon.png)`

![Github Logo](https://github.com/fluidicon.png) 

### Inline Code 行内代码
第一段为markdown语言，第二段为显示结果
``` `include`表示头文件，`using namespace std`声明命名空间```

`include`表示头文件，`using namespace std`声明命名空间

### Code Blocks 代码块 
加入代码块的时候，在前面加三个` ``` `,结尾加三个` ``` `就可以了，如果用某种语言写成，可以在第一个` ``` `后面加上语言名称，例如：`" ```swift 或 ```C++"`，markdown支持几乎所有编程语言的高亮显示
 ```swift
 var natural_numbers: Array<int> = [0,1,2,3]
 print(natural_numbers.capacity) 
 ```

 
### Tables 表格
```
First Header | Second Header
-------------|---------------
Content from cell 1 | Content from cell 2
Content from first column | Content from second column
  ```
First Header | Second Header
-------------|---------------
Content from cell 1 | Content from cell 2
Content from first column | Content from second column

## 对文件路径的理解
我们在插入链接的时候，会使用：

`[俄乌前线录像](https://www.bilibili.com/video/BV1GL411K7aK?share_source=copy_web)`

点击查看[俄乌前线录像](https://www.bilibili.com/video/BV1GL411K7aK?share_source=copy_web)

更普通的，这个链接可以换成文件，可以通过相对路径相互引用：

点击查看[测试文档](./Markdowntest.md)，当然也可以写绝对路径，但文件移动位置的话链接就会失效，只要相对路径不变就不会出现问题

更普遍的，可以将链接这篇文章中的某个标题，比如[Markdown引言部分](#markdown引言)

## 其他注意事项

有的时候你在markdown明明换行了，可是上传到GitHub上面一看，文字都粘在一起了。这是为什么呢？

英文在分段的时候，不像我们写文章段前空两格，他们会直接在两段之间多空一行。一般的回车只是用来方便阅读，不然一行的内容太长了。

如果你不希望这种方式生效，可以在一行后面加两个空格；但这样很麻烦，还是多加回车吧；最好在每种语法前后都空行，这样也能有效减少语法不被识别的情况

## Markdown工具介绍

### macOS

#### Typora

所见即所得的`markdown`编辑软件，全平台通用，各种意义上都是`markdown`编辑的首选

主要用来写单独的markdown，可以专门开一个文件夹放自己的笔记

#### VS Code

安装插件`Markdown All in One`，可以支持很多快捷操作，直接开文件命名为`.md`编辑就可以了。

一般来说，代码都是和`Markdown`文件放在一起的，用VSCode编辑README.md会很方便

#### Xcode 略

#### 其他

打算以后自己的文稿都用Markdown来写，可以搜索一些付费制/订阅制的功能更强大的软件

## 文字编辑效率upup

最后呢，再教大家一些快速写文档的方法。这种方法在macOS上的大多数文字/代码编辑软件上都适用（包括Xcode）。

〇 双击选中一个词：这里词指一个中文的词语或者一个英文的单词

〇 三击选中一行

〇 ⌥左右：以词为单位移动光标

〇 ⌘上下左右：移动光标到行首/行未/文头/文末

〇 按住⇧：文字选中；⇧上下左右 / ⇧⌥左右 / ⌘⇧上下左右

〇 按住⌥：矩形区域选中

〇 ⌥⌫、⌘⌫；fn⌫：删除词、删除到行首；向后删除 delete；⌘X也是一种删除的方式

## 用Markdown编辑数学公式（From LaTex）

### 希腊字母表
 Name | Display | Capital Case | Display | Var Case | Display 
:-----:|:-------:|:----------:|:--------:|:---------:|:------:
`\alpha` | $\alpha$  | `A` | $A$
`\beta`  | $\beta$  |  `B`|$B$
`\gamma`| $\gamma$ | `\Gamma`| $\Gamma$
`\theta`|$\theta$|`\Theta`|$\Theta$|`\vartheta`|$\vartheta$
`\mu`|$\mu$|`M`|$M$
`\delta`|$\delta$|`\Delta`|$\Delta$
`\epsilon`|$\epsilon$|`E`|$E$|`\varepsilon`|$\varepsilon$
`\sigma`|$\sigma$|`\Sigma`|$\Sigma$|`\varsigma`|$\varsigma$
`\pi`|$\pi$|`\Pi`|$\Pi$|`\varpi`|$\varpi$
`\omega`|$\omega$|`\Omega`|$\Omega$|`\varOmega`|$\varOmega$
`\xi`|$\xi$|`\Xi`|$\Xi$
`\zeta`|$\zeta$|`Z`|$Z$
`\chi`|$\chi$|`X`|$X$
`\rho`|$\rho$|`P`|$P$|`\varrho`|$varrho$
`\phi`|$\phi$|`\Phi`|$\Phi$|`\varphi`|$\varphi$
`\eta`|$\eta$|`H`|$H$
`\lambda`|$\lambda$|`\Lambda`|$\Lambda$
`\kappa`|$\kappa$|`K`|$K$
`\nu`|$\nu$|`N`|$N$
`\upsilon`|$\upsilon$|`\Upsilon`|$\Upsilon$
`\psi`|$\psi$|`\Psi`|$\Psi$
`\tau`|$\tau$|`T`|$T$
`\iota`|$\iota$|`I`|$I$
`\omicron`|$\omicron$|`O`|$O$

* 有代码的希腊大写字母，通过`\var`前缀获得斜体
* 没有代码的希腊大写字母，直接敲获得斜体，`\text`前缀获得正体
* 也可以使用`\rm`将下一个单词变正，`\text T`的作用范围只是下一个字母；可以尝试加`{}`

### 运算

#### 简单运算
Type | Typeset
:---:| :---:
`+`|$+$
`-`|$-$
`\pm`|$\pm$
`\mp`|$\mp$
`\times`|$\times$
`\cdot`|$\cdot$
`\div`|$\div$
`\bmod`|$\bmod$
`\cap`|$\cap$
`\cup`|$\cup$
`\wedge or \land`|$\wedge$
`\vee or \lor`|$\lor$
`\ast`|$\ast$
`\det`|$\det$

#### 复杂运算
Type | Typeset
:--:|:--:
`\sqrt{abc}`|$\sqrt{abc}$
`\sqrt[n]{abc}`|$\sqrt[n]{abc}$
`\frac{abc}{xyz}`|$\frac{abc}{xyz}$
`\int_{a}{b}`|$\int_{a}^{b}$
`\iiint_{a}^{b}`|$\iiint_{a}^{b}$
`\oint_{a}^{b}`|$\oint_{a}^{b}$
`frac{\mathrm{d}^{n} y}{\mathrm{d} x^n}`|$\frac{\mathrm{d}^{n} y}{\mathrm{d} x^n}$
`\frac{\partial f}{\partial x}`|$\frac{\partial f}{\partial x}$
`\frac{\partial ^{n} f}{\partial x^{n}}`|$\frac{\partial ^{n} f}{\partial x^{n}}$
`\sum_{i=1}^{n}`|$\sum_{i=1}^{n}$
`\prod_{i=1}^{n}`|$\prod_{i=1}^{n}$
`\bigcap_{i=1}^{n}`|$\bigcap_{i=1}^{n}$
`\bigcup_{i=1}^{n}`|$\bigcup_{i=1}^{n}$

#### 基本初等函数
Type | Typeset
:--:|:--:
`\arccos`|$\arccos$
`\arcsin`|$\arcsin$
`\arctan`|$\arctan$
`\cosh`|$\cosh$
`\cot`|$\cot$
`\lg`|$\lg$
`\ln`|$\ln$
`\log`|$\log$
`\sin`|$\sin$
`\tan`|$\tan$
`\tanh`|$\tanh$
* $lim,inf ,sup,min,max$等直接在前面加`\`即可
* 键盘上直接敲出的符号，前面直接加`\`即可

#### 点缀
<style> table th:first-of-type { width: 200px; } </style>
Name |Type | Typeset
:-:|:-:|:-:
幂乘|`a^n`|$a^n$
下标|`a_n`|$a_n$
取反|`\bar{a}`|$\bar{a}$
一阶导数|`\dot{a}`|$\dot{a}$
二阶导数|`\ddot{a}`|$\ddot{a}$
向量|`\vec{a}`|$\vec{a}$
估计值|`\hat{a}`|$\hat{a}$
弯弯（我也不知道是什么）|`\tilde{a}`|$\tilde{a}$
空心圆|`\mathting{a}`|$\mathring{a}$
二阶导|`f^{''}`|$f^{''}$
角度|`90^\circ`|$90^\circ$
什么玩意角|`\overset{\frown}\psi`|$\overset{\frown}\psi$
未知等于| `\overset{?}{=}`| $\overset{?}{=}$
下方标注|`\underset{t\in R}{max}`|$\underset{t\in R}{max}$

#### 二元关系

Type | Typeset
:-:|:-:
`<`|$<$
`>`|$>$
`\le`|$\le$
`\ge`|$\ge$
`\leqslant`|$\leqslant$
`\geqslant`|$\geqslant$
`=`|$=$
`\ne`|$\ne$
`:`|$:$
`\in`|$\in$
`\notin`|$\notin$
`\ni \owns`|$\owns$
`\ll`|$\ll$
`\gg`|$\gg$
`\sim`|$\sim$
`\approx`|$\approx$
`\cong`|$\cong$
`\equiv`|$\equiv$
`\subset`|$\subset$
`\supset`|$\supset$
`\subseteq`|$\subseteq$
`\sebsetneqq`|$\subsetneqq$
`\perp`|$\perp$
`\parallel`|$\parallel$
`\mid`|$\mid$
`\propto`|$\propto$

####其他符号

Type |Typeset
:-:|:-:
`\therefore`|$\therefore$
`\because`|$\because$
`\ell`|$\ell$
`\partial`|$\partial$
`\infty`|$\infty$
`\varnoting`|$\varnothing$
`\forall`|$\forall$
`\exists`|$\exists$
`\triangle`|$\triangle$
`\angle`|$\angle$
`\surd`|$\surd$
`\nabla`|$\nabla$
`\neg \lnot`|$\lnot$
`\ldots`|$\ldots$
`\cdots`|$\cdots$
`\vdots`|$\vdots$
`\S`|$\S$

#### For Entertainment
Type |Typeset
:-:|:-:
`\spadesuit or \spades`|$\spades$
`\hearsuit or hearts`|$\hearts$
`\diamondsuit or \diamonds`|$\diamondsuit$
`\clubsuit`|$\clubs$


#### 箭头
Type |Typeset
:-:|:-:
`\to or \rightarrow`|$\to$
`\leftarrow`|$\leftarrow$
`\Rightarrow`|$\Rightarrow$
`\Leftarrow`|$\Leftarrow$
`Longrightarrow`|$\Longrightarrow$
`\Longleftarrow`|$\Longleftarrow$
`\Leftrightarrow`|$\Leftrightarrow$
`\iff or \Longleftrightarrow`|$\iff$

#### 包裹结构
Type |Typeset
:-:|:-:
`\overrightarrow{AB}`|$\overrightarrow{AB}$
`\overline{AB}`|$\overline{AB}$
`\underline{abc}`|$\underline{abc}$
`\tilde{abc}`|$\tilde{abc}$
`\widetilde{abc}`|$\widetilde{abc}$
`\overbrace{abc}`|$\overbrace{abc}$
`\underbrace{abc}`|$\underbrace{abc}$

### 括号
####普通括号
Type |Typeset
:-:|:-:
`( )`|$( )$
`[ ]`|$[ ]$
`\lbrace \rbrace`|$\lbrace \rbrace$
`\langle \rangle`|$\langle \rangle$

* 使用`\left \(`和`\right \}`打出大的包裹括号. 用.代替括号可以空出来一半的括号
####绝对值/取模
绝对值/取模

`\left | a \right |`
$\left | a \right |$
`\left \| \boldsymbol{a} \right \|`
$\left \| \boldsymbol{a} \right \|$

### Vector向量
Type |Typeset
:-:|:-:
`\begin{matrix} a&b&c \\ c&d \end{matrix}`|$\begin{matrix} a&b \\ c&d \end{matrix}$
`\begin{pmatrix} a&b \\ c&d \end{pmatrix}`|$\begin{pmatrix} a&b \\ c&d \end{pmatrix}$
`\begin{bmatrix} a&b \\ c&d \end{bmatrix}`|$\begin{bmatrix} a&b \\ c&d \end{bmatrix}$
`\begin{Bmatrix} a&b \\ c&d \end{Bmatrix}`|$\begin{Bmatrix} a&b \\ c&d \end{Bmatrix}$
`\begin{vmatrix} a&b \\ c&d \end{vmatrix}`|$\begin{vmatrix} a&b \\ c&d \end{vmatrix}$
`\begin{Vmatrix} a&b \\ c&d \end{Vmatrix}`|$\begin{Vmatrix} a&b \\ c&d \end{Vmatrix}$

*两侧括号也可以用 `\left \right+括号` 来包裹

####增广矩阵
```markdown
\left[
    \begin{array}{cc|c}
      1 & 2 & 3 \\
      4 & 5 & 6
    \end{array}
\right]
```
$\left[
    \begin{array}{c|cc}
      1 & 2 & 3 \\
      4 & 5 & 6
    \end{array}
\right]$

#### 方程组
```markdown
\left\{
\begin{array}{c}
    a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1 \\
    a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2 \\
    \vdots \\
    a_{n1}x_1+a_{n2}x_2+\cdots+a_{nn}x_n=b_n
\end{array}
\right.
```
$\left\{
\begin{array}{c}
    a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1 \\
    a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2 \\
    \vdots \\
    a_{n1}x_1+a_{n2}x_2+\cdots+a_{nn}x_n=b_n
\end{array}
\right.$

- 左侧花括号

    ```latex
    \begin{equation}
    % \begin{equation*} 加'*'去掉公式编号
    \left\{
    \begin{aligned}     %请使用'aligned'或'align*'
    2x + y &= 1  \\     %加'&'指定对齐位置
    2x + 2y &= 2
    \end{aligned}
    \right.
    \end{equation}
    % \end{equation*}   加'*'去掉公式编号

    % 注意：在 markdown 环境下，某些特殊字符，如'\', '*'等，会首先被 markdown 语法转义，然后再被 Latex 转义。
    % 因此有时候 '\{'需要写作'\\{'，'*'需要写作'\*'，'\\'需要写作'\\\\'等，视不同的解释环境而定
    ```

    $$ \begin{equation}
    \left\{
    \begin{aligned}
    2x + y &= 1 \\\\
    2x + 2y &= 2
    \end{aligned}
    \right.
    \end{equation} $$

    **注**：如果各个方程需要在某个字符处对齐（如等号对齐），只需在所有要对齐的字符前加上 `&` 符号。如果不需要公式编号，只需在宏包名称后加上 `*` 号。

  ####

- $\bold{分情况讨论方程式}$

    ```latex
    f(x) =
    \begin{cases}
    x^2 \qquad & a \gt 0 \\
    e^x \qquad & a \le 0
    \end{cases}
    ```

    $$ f(x) = \begin{cases}
    x^2 \qquad & x \gt 0 \\
    0\qquad & x =0\\
    e^x \qquad & x \lt 0
    \end{cases} $$


    $$ \begin{aligned}
    a &= 1 \\
    bcd &= 2
    \end{aligned} $$


## 文档布局
### 空格
Type |Typeset
:-:|:-:
`aa`|$aa$
`a\ a`|$a\ a$
`a\quad a`|$a\quad a$
`a\qquad a`|$a\qquad a$

### 紧缩
Type |Typeset
:-:|:-:
`a\!a`|$a\!a$
`a\negmedspace a`|$a\negmedspace a$
`a\negthickspace a`|$a\negthickspace a$

### 字号
Type |Typeset
:-:|:-:
`text`|$text$
`\tiny text`|$\tiny text$
`\small text`|$\small text$
`\normalsize text`|$\normalsize text	$
`\large text`|$\large text$
`\huge text`|$\huge text$


### 字体
Type |Typeset
:-:|:-:
`\mathbf{ABC}`|$\mathbf{ABC}$
`\mathcal{ABC}`|$\mathcal{ABC}$
`\mathit{ABC}`|$\mathit{ABC}$
`\mathsf{ABC}`|$\mathsf{ABC}$
`\mathtt{ABC}`|$\mathtt{ABC}$
`\boldsymbol{ABC}`|$\boldsymbol{ABC}$
`\boldsymbol{\alpha\beta}`|$\boldsymbol{\alpha\beta}$
`\mathbb{ABC}`|$\mathbb{ABC}$
`\mathfrak{ABC}`|$\mathfrak{ABC}$
`\mathscr{ABC}`|$\mathscr{ABC}$

## 总结

对我来说，Markdown给我的第一感觉是轻便且强大，有炫酷的LaTex数学公式，对后续论文的写作有一定帮助，而且最重要的是记笔记/博客/日志/写文档很爽。感谢清华大学9字班的[杨希杰同学](https://yang-xijie.github.io)（B站账号：[我不是小杰](https://space.bilibili.com/24502827?spm_id_from=333.337.search-card.all.click))和THU在Github上的[在线课程](https://thu-ios.github.io/tutorials)。希望这篇文档可以帮助更多的人❤️❤️❤️