importance: 3

---

# "this" の値を説明してください

<<<<<<< HEAD:1-js/99-js-misc/04-reference-type/3-why-this/task.md
下のコードで、`user.go()` メソッドを4回連続で呼び出すつもりです。
=======
In the code below we intend to call `obj.go()` method 4 times in a row.
>>>>>>> fbf443e414097e5a3a41dd1273ef9a4a3230e72c:1-js/99-js-misc/04-reference-type/3-why-this/task.md

しかし、呼び出し `(1)` と `(2)` は `(3)` と `(4)` とは異なっています。なぜでしょう？

```js run no-beautify
let obj, method;

obj = {
  go: function() { alert(this); }
};

obj.go();               // (1) [object Object]

(obj.go)();             // (2) [object Object]

(method = obj.go)();    // (3) undefined

(obj.go || obj.stop)(); // (4) undefined
```