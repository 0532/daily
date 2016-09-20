### 项目命名

全部采用小写方式， 以下划线分隔。

例：my\_project\_name

### 目录命名

参照项目命名规则；

有复数结构时，要采用复数命名法。

例：scripts, styles, images, data\_models

### 单行注释

双斜线后，必须跟一个空格；

缩进与下一行代码保持一致；

可位于一个代码行的末尾，与代码间隔一个空格。

if \(condition\) {

`// if you made it here, then all security checks passed`

` allowed();}`



`var zhangsan = 'zhangsan'; // one space after code`

多行注释

最少三行, '\*'后跟一个空格，具体参照右边的写法；

建议在以下情况下使用：

* 难于理解的代码段
* 可能存在错误的代码段
* 浏览器特殊的HACK代码
* 业务逻辑强相关的代码、

### 换行

换行的地方，行末必须有','或者运算符；

以下几种情况不需要换行：

* 下列关键字后：`else`, `catch`, `finally`
* 代码块'{'前

以下几种情况需要换行：

* 代码块'{'后和'}'前
* 变量赋值后

```
// not goodvar a = {
    b: 1
    , c: 2};

x = y
    ? 1 : 2;

// goodvar a = {
    b: 1,
    c: 2};
```

