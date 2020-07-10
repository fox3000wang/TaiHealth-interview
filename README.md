# 钛康科技面试

考试要求 30 分钟做完

## 第一题

```js
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i));
}
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i));
}
// 3 3 3 1 2 3
```

## 第二题

```js
let c = {
  greeting: 'Hey',
};
let d;
d = c;
c.greeting = 'Hello';
console.log(d.greeting);
// Hello
```

## 第三题

```js
let a = 3;
let b = new Number(3);
let c = 3;
console.log(a == b);
console.log(a === b);
console.log(b === c);
// true flase flase
```

## 第四题

```js
const items = ['a', 'b', 'c', 'd'];
for (let i in items) {
  console.log(i);
}
for (let i of items) {
  console.log(i);
}
// a b c d 1 2 3 4
```

## 第五题

```js
const myPromise = Promise.resolve(Promise.resolve('Promise!'));

function funcOne() {
  myPromise.then(res => res).then(res => console.log(res));
  setTimeout(() => console.log('Timeout!'));
  console.log('Last line!');
}
async function funcTwo() {
  const res = await myPromise;
  console.log(await res);
  setTimeout(() => console.log('Timeout!'));
  console.log('Last line!');
}
funcOne();
funcTwo();
// Last line! Promise! Promise! Last line!  Timeout! Timeout!
```

## 前五题的答案 C A C C D（我反正全对了）

## 第六题 实现一段布局的 css

## 第七题 实现一个 mul 函数

```js
const mul = x => {
  let s = x;
  let c = y => {
    s *= y;
    return c;
  };
  c.toString = () => s;
  return c;
};
console.log(mul(2)(3)(4)); // 24
console.log(mul(4)(3)(4)); // 48
```

## 第八题

请编写一个组件以显示图像。 提出要求

- 图像在 div 容器中
- 图片大小未知，
- 容器的大小为 300px 高度和 100％宽度
- 图像应放置在容器的中央
- 图像可以放大，但不能拉伸。
- 当图像仍在加载时，显示“正在加载...”标签。
