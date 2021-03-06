---
id: 587d7dbf367417b2b2512bbb
title: 使用 @while 当条件满足时样式生效
challengeType: 0
forumTopicId: 301454
---

# --description--

Sass 中的`@while`指令与 JavaScript 中的`while`类似。只要满足条件，它就会一直创建 CSS 代码。

`@for`挑战提供了一个创建简单网格系统的示例。这也适用于`@while`。

```scss
$x: 1;
@while $x < 13 {
  .col-#{$x} { width: 100%/12 * $x;}
  $x: $x + 1;
}
```

首先，定义变量`$x`并将其设置为 1。接下来，使用`@while`指令，当`$x`小于 13 时创建网格系统 。 在设置`width`的 CSS 规则后，`$x`增加 1 以避免无限循环。

# --instructions--

使用`@while`创建一系列具有不同`font-sizes`的 class。

从`text-1`到`text-10`应该有 10 个不同的 class。然后将`font-size`设置为 15px 乘以当前索引号。注意不要写成死循环！

# --hints--

你的代码应使用`@while`指令。

```js
assert(code.match(/@while /g));
```

你的代码应将索引变量设置为 1 才能启动。

```js
assert(code.match(/\$.*:\s*?1;/gi));
```

你的代码应该递增计数器变量。

```js
assert(code.match(/\$(.*)\s*?:\s*\$\1\s*\+\s*1\s*;/gi));
```

`.text-1`class 的`font-size`应为 15px。

```js
assert($('.text-1').css('font-size') == '15px');
```

`.text-2`class 的`font-size`应为 30px。

```js
assert($('.text-2').css('font-size') == '30px');
```

`.text-3`class 的`font-size`应为 45px。

```js
assert($('.text-3').css('font-size') == '45px');
```

`.text-4`class 的`font-size`应为 60px。

```js
assert($('.text-4').css('font-size') == '60px');
```

`.text-5`class 的`font-size`应为 75px。

```js
assert($('.text-5').css('font-size') == '75px');
```

# --solutions--

