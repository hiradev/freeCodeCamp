---
id: 587d7b85367417b2b2512b38
title: Спільне використання оператору призначення замість оператору рівності
challengeType: 1
forumTopicId: 301191
dashedName: catch-use-of-assignment-operator-instead-of-equality-operator
---

# --description--

Розгалуження певних типів програм, які виконують різні дії у разі виконання певних умов, у JavaScript опирається на команди `if`, `else if` та `else`. Інколи такі умови відбуваються у формі перевірки або коли результат дорівнює значенню.

За цією логікою (принаймні в англійській мові), "якщо x дорівнює y, то..." на мову кодування можна перекласти, використовуючи `=` або оператор присвоєння. Це призводить до неочікуваних потоків керування у вашій програмі.

Як зазначено у попередніх завданнях, у JavaScript оператор присвоєння (`=`) надає значення для назв змінних. І оператори `==` та `===` перевіряють їх на рівність (потрійні `===` тести для суворої рівності, вказуючи, що як значення, так і тип є однаковими).

Поданий нижче код присвоює `x` значення 2, що оцінюватиметься як `true`. Майже кожне значення у JavaScript самостійно оцінюється до `true`, за винятком деяких випадків, які нам відомі як неправильні значення: `false`, `0`, `""` (пустий рядок), `NaN`, `undefined` та `null`.

```js
let x = 1;
let y = 2;
if (x = y) {

} else {

}
```

У цьому прикладі блок коду в межах оператора `if` не виконуватиметься для будь-якого значення `y`, якщо тільки `y` не буде помилковим. Блок `else`, який за нашими очікуваннями повинен тут виконуватися, насправді не буде запускатися.

# --instructions--

Виправіть умову таким чином, щоб програма виконувалася у правій гілці, і відповідне значення було присвоєне `result`.

# --hints--

Ваш код має виправити умову так, щоб відбувалася перевірка рівності замість використання оператора присвоєння.

```js
assert(result == 'Not equal!');
```

Умова має використовувати або `==`, або `===`, щоб відбувалася перевірка рівності.

```js
assert(code.match(/x\s*?===?\s*?y/g));
```

# --seed--

## --seed-contents--

```js
let x = 7;
let y = 9;
let result = "to come";

if(x = y) {
  result = "Equal!";
} else {
  result = "Not equal!";
}

console.log(result);
```

# --solutions--

```js
let x = 7;
let y = 9;
let result = "to come";

if(x === y) {
 result = "Equal!";
} else {
 result = "Not equal!";
}

console.log(result);
```