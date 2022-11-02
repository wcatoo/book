<meta charset="utf-8">

## Markdown guide -- extened syntax
拓展语法在基础语法的基础上满足一些特殊的需求<br>

### Table
> 3个及以上(-)创建每列的头标题 (|)创建每列
```markdown
| abc  | bcd |
|------|-----|
| abc  | bcd | 
```

### Alignment
> 列表中单元格对齐方式<br> 
> :--- 左对齐<br>
> :--:居中<br>
> ---: 右对齐<br>
```markdown
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```
<!-- 需要下载插件 -->
### Footnote
```markdown
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.<br>
[^bignote]: Here's one with multiple paragraphs and code.
```

### Definition Lists
```markdown
First Term
: This is the definition of the first term.
```

<!-- 划线删除 -->
### Strikethrough
```markdown
~~abc~~
```

### Task Lists
```markdown
    - [x] a
    - [ ] b
```

### Eoji
> markdown支持的表情快捷码 [list of emoji shortcodes](https://gist.github.com/rxaviers/7360908 "markdown支持的表情快捷码")<br>
```markdown
    Gone camping! :tent: Be back soon.
```

### Heightlight
> 一些支持markdown语法的高亮 ==高亮==<br>
> 也可以用html方式的高亮(均支持) <mark>asdasd</mark>

### 下标
> 一些支持markdown语法的下标 H~2~o<br>
> html 语法的下标 H<sub>2</sub>O

### 下标
> 一些支持markdown语法的上标 H^2^o<br>
> html 语法的下标 H<sup>2</sup>O