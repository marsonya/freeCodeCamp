---
id: bad87dee1348bd9aede07836
title: 使用 id 属性来设定元素的样式
challengeType: 0
videoUrl: 'https://scrimba.com/c/cakyZfL'
forumTopicId: 18339
---

# --description--

通过`id`属性，你可以做一些很酷的事情，例如，就像 class 一样，你可以使用 CSS 来设置他们的样式

可是，`id`不可以重用，只应用于一个元素上。同时，在 CSS 里，`id`的优先级要高于`class`，如果一个元素同时应用了`class`和`id`，并设置样式有冲突，会优先应用`id`的样式。

选择`id`为`cat-photo-element`的元素，并设置它的背景样式为`green`，可以在`style`标签里这样写：

```css
#cat-photo-element {
  background-color: green;
}
```

注意在`style`标签里，声明 class 的时候必须在名字前插入`.`符号。同样，在声明 id 的时候，也必须在名字前插入`#`符号。

# --instructions--

尝试给含有`cat-photo-form`id属性的`form`表单的背景颜色设置为`green`。

# --hints--

设置`form`元素的 id 为`cat-photo-form`。

```js
assert($('form').attr('id') === 'cat-photo-form');
```

`form`元素应该含有`background-color`css 属性并且值为 `green`。

```js
assert($('#cat-photo-form').css('background-color') === 'rgb(0, 128, 0)');
```

确保`form`元素含有`id`属性。

```js
assert(
  code.match(/<form.*cat-photo-form.*>/gi) &&
    code.match(/<form.*cat-photo-form.*>/gi).length > 0
);
```

不要在`form`元素上添加其他`class`属性或者`style`行内样式。

```js
assert(!code.match(/<form.*style.*>/gi) && !code.match(/<form.*class.*>/gi));
```

# --solutions--

