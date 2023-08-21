# JavaScript Bootcamp ft phuquocchamp

## 1. An Introduction

### 1.1 An Introduction to JavaScript.

#### 1.1.1 Languages "over" JavaScript.

- Cú pháp của javascript sẽ không phù hợp cho đại đa số người dùng. Vì vậy có một số ngôn ngữ được sinh ra với cú pháp ngắn hơn, phù hợp hơn với mục đích của người sử dụng.
  - CoffeeScript
  - TypeScript
  - Flow
  - Dart
  - Brython
  - Kotlin
    1.

#### 1.2 Manuals and specificaitons

Một số nguồn tài liệu cần tham khảo:

[The ECMA-262 specification](https://www.ecma-international.org/wp-content/uploads/ECMA-262_14th_edition_june_2023.pdf "[The ECMA-262 specification](https://www.ecma-international.org/wp-content/uploads/ECMA-262_14th_edition_june_2023.pdf)")

[MDN JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference#functions)

## 2. Javascript Fundamentals

### 2.1 Hello World.

- We can use a `<script>` tag to add JavaScript code to a page.

* The `type` and `language` attributes are not required.
* A script in an external file can be inserted with `<script src="path/to/script.js"></script>`.

### 2.2 Code structure

### 2.3 The morden mode, "use strict".

Khi cập nhật, cải thiện tính năng trong javascript để code cũ có thể hoạt động mà không bị xung đột với code thì các tính năng của phiên bản mới bị tắt đi. Để sử dụng các tính năng mới này ta sử dụng "use strict" ở đầu file code javascript để cho engines hiểu là đang sử dụng theo tính năng mới.

```js
"use strict";

// this code works the morden way 
```

#### [Should we “use strict”?](https://javascript.info/strict-mode#should-we-use-strict)

The question may sound obvious, but it’s not so.

One could recommend to start scripts with `"use strict"`… But you know what’s cool?

Modern JavaScript supports “classes” and “modules” – advanced language structures (we’ll surely get to them), that enable `use strict` automatically. So we don’t need to add the `"use strict"` directive, if we use them.

**So, for now `"use strict";` is a welcome guest at the top of your scripts. Later, when your code is all in classes and modules, you may omit it.**

As of now, we’ve got to know about `use strict` in general.

In the next chapters, as we learn language features, we’ll see the differences between the strict and old modes. Luckily, there aren’t many and they actually make our lives better.

All examples in this tutorial assume strict mode unless (very rarely) specified otherwise.

### 2.4 Variables

Từ khóa *let* dùng để khai báo biến trong js. Với một số phiên bản code cũ hơn ta có thể thấy từ khóa *var*  thay vì *let*

> Mỗi từ khóa chỉ được khai báo 1 lần việc khai báo nhiều lần sẽ sinh ra lỗi cú pháp:

```javascript

let message = "this";
// error --> 
let message = "that";
```

#### Variable naming

Có 2 quy tắc khi đặt tên biến trong javascript

- Tên biến bắc buộc phải bao gồm hoặc *chữ cái, chữ số, $ và _.***
- Kí tự đầu tiên của tên biến không phải là chữ số.

>  Với tên biến gồm nhiều từ ta nên đặt tên biến theo kiểu **camelCase :** 
>
> ex: myVeryLongName

#### Constants Variable

Với các hằng số trong js ta sử dụng từ khóa const thay vì let.

>  Với mốt số biến hằng số dùng để lưu các giá trị khó nhớ. ta có thể sử dụng kết hợp Kí tự viết hoa và kí tự gạch dứới để đặt tên cho chúng :

```javascript
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";

// ...when we need to pick a color
let color = COLOR_ORANGE;
alert(color); // #FF7F00

```
