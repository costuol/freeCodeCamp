---
title: Random Method
localeTitle: Случайный метод
---
## Случайный метод

Метод JavaScript `Math.random()` - отличный встроенный метод для создания случайных чисел. Когда `Math.random()` выполняется, он возвращает случайное число, которое может находиться где-то между 0 и 1. `Math.random()` 0, а 1 исключено.

### Создание случайного числа с плавающей запятой между 0 и 1

Метод `Math.random()` возвращает число с плавающей запятой (десятичное), большее или равное 0, и меньшее (но никогда не равное) 1. Другими словами `0 <= x < 1` . Например:

```JavaScript
console.log(Math.random()); 
 // 0.7069207248635578 
 
 console.log(Math.random()); 
 // 0.765046694794209 
 
 console.log(Math.random()); 
 // 0.14069121642698246 
```

(Конечно, возвращаемые числа будут разными каждый раз. Это будет приниматься для всех следующих примеров - на каждом проходе будут возникать разные результаты).

Чтобы получить случайное число между большим диапазоном, умножьте результат `Math.random()` на число.

### Генерирование случайного числа с плавающей запятой между 0 и заданным максимальным значением

Обычно вам не нужны случайные числа от 0 до 1 - вам нужны большие числа или даже целые числа.

Например, если вам нужен случайный номер с плавающей запятой между 0 и 10, вы можете использовать:

```JavaScript
var x = Math.random()*10; 
 
 console.log(x); 
 // 4.133793901445541 
```

### Создание случайного числа с плавающей запятой в пределах диапазона

Если вам нужен случайный номер с плавающей запятой, который находится между двумя конкретными номерами, вы можете сделать что-то вроде этого:

```JavaScript
var min = 83.1; 
 var max = 193.36; 
 
 var x = Math.random()*(max - min)+min; 
 
 console.log(x); 
 // 126.94014012699063 
```

### Генерация случайного целого числа от 0 до max

Часто вам нужны целые числа. Для этого вам придется использовать некоторые другие методы из объекта `Math` , `Math.floor()` (округляется до ближайшего целого) и `Math.ceil()` (округляется до ближайшего целого).

Например, если вам нужно произвольно выбирать из массива из 10 элементов, вам понадобится случайное число от 0 до 9 включительно (помните, что массивы нулевые индексируются).

```JavaScript
var x = Math.floor(Math.random()*10); 
 
 console.log(x); 
 // 7 
```

(Помните, что `Math.random()` никогда не вернет ровно 1, поэтому `Math.random()*10` никогда не вернется ровно 10. Это означает, что после округления результат всегда будет 9 или меньше.)

### Генерация случайного целого числа от 1 до max

Если вам нужно случайное число с минимальным числом, `Math.ceil()` 1 (например, выбор случайного дня в январе), вы можете использовать метод `Math.ceil()` .

```JavaScript
var x = Math.ceil(Math.random()*31); 
 
 console.log(x); 
 // 23 
```

Другим способом было бы использовать предыдущую функцию (используя `Math.floor()` ) и добавить 1 к ней:

```JavaScript
var x = Math.floor(Math.random()*31)+1; 
 
 console.log(x); 
 // 17 
```

### Создание случайного целого в пределах диапазона

Наконец, иногда вам нужно случайное целое число между двумя конкретными целыми числами. Например, если вы пытаетесь выбрать билеты на лотерею и знаете номера самого низкого и самого большого числа:

```JavaScript
var min = 1718; 
 var max = 3429; 
 
 var x = Math.floor(Math.random()*(max-min+1)+min); 
 
 console.log(x); 
 //2509 
```

### Насколько случайным является Math.random ()?

Можно указать, что число, возвращаемое `Math.random()` является псевдослучайным числом, так как ни один компьютер не может генерировать по-настоящему случайное число, которое проявляет случайность во всех масштабах и во всех размерах наборов данных. Однако псевдослучайное число, генерируемое `Math.random()` , обычно достаточно для нужд почти любой программы, которую вы можете написать. Непорядочная случайность проявляется только в астрономически больших числах или когда нужны необычно точные десятичные числа.

### Дополнительная информация:

*   Документация: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
