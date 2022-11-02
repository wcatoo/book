## Markdown guide -- basic syntax
<p>基本语法是所有Markdown应用都支持的语法<br>

----
* 
----
<!-- 标题 -->
### Headings
> #表示标题 如#一级标题  ##二级标题等<br>

<!-- 段落 -->
### Paragraphs
> 段落空一行可以表示段落 
```markdown
paragraphs one
<!-- 空一行 -->
paragraphs two
```

<!-- 断行 -->
### Line break
> 一行结束可以用两个以上的空格或者\<br>表示，推荐使用\<br>这样可读性更好一点    

<!-- 显示强调 -->
### Emphasis
#### Bold
> \*\*blod\*\* 或者\_\_blod\_\_
#### Italic
> \*italic\* 或者 \_italic\_

<!-- 块显示 -->
### Blockquote
> \> 表示显示一个块 块中的内容可以和正常的语法写法一致，同时也可以嵌套

<!-- 列表 -->
### List
#### ordered list
```markdown
    1. first
    2. second
    3. third
```
#### unordered list
```markdown
    * first
    * second
    * third
    
    - first
    - second
    - third
    
    + first
    + second
    + third
```

### Code
> \`\`\`language<br>
>   int main()<br>
> \`\`\`

### Image
> \![图片文字说明]\(图片地址 "可选标题")

### Horizontal Rules
> \---<br>
> \***星号<br>
> \___下划线<br>

### Links
> \[描述](地址 "可选标题") [google](https://www.google.com "谷歌网站")

### URL Email address
> \<地址>  <https://www.google.com>

### Formatting link
```markdown
[hobbit-hole][1]

[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
```

### Link image
> \[\![图面描述]\(图面地址)](link地址)
```markdown
    [![An old rock in the desert](/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

```


