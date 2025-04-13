
![](https://avatars.mds.yandex.net/i?id=8c5468d51c8b47635eaabe567064b256-4411346-images-thumbs&n=13 "задачи по JavaScript")
# Популярные задачи на собеседовании по JavaScript

## **Задача 1** ##
У нас есть массив 
```javascript
сonst a1 = [10, 8, 1, 0, 5]
```
Напишите функцию, в которой:
1. если число кратно 3 (% 3), то будет выводиться сообщение Fizz;
2. если число кратно 5 (% 5), то будет выводиться сообщение Buzz
3. eсли число кратно и 3, и 5, то будет выводиться сообщение FizzBuzz
4. если число не кратно 3 и 5, то будет выводиться сообщение err


<details>
<summary>Смотреть ответ</summary>

Реализация
1. Нужно пройти по массиву (минимальное количество раз)
2. Проверить каждое число на кратность 3 и 5 
```javascript
function FizzBuzz(arr) {
   for (let i = 0; i < arr.length; i++) {

      let outString = "";
      if (arr[i] % 3 === 0) {
         outString += "Fizz"
      }
      if (arr[i] % 5 === 0) {
         outString += "Buzz"
      } else {
         console.log("err");
      }

      console.log(outString);

   }
}
FizzBuzz(a1);
```
   


</details>
<hr />

## **Задача 2** ##
У нас есть неизменяемая переменная n, у которой значение 100. 
Найдите количество простых чисел от 2 до n

<details>
<summary>Смотреть ответ</summary>

Реализация
1. Нужно пройти по каждому числу от 2 до n
2. Проверить, простое ли оно, если простое, прибавить 1
```javascript
const n = 100;

function isPrime(val) {
   for (let i=2; i<val;i++){
      if(val % i === 0) return false;
   }
   return true;
}

function countPrimes(n) {
   let counter = 0;
   for (let i=2; i<=n; i++) {
      if (isPrime(i)) counter++;
   }
   return counter;
}

const primes = countPrimes(100);
console.log(primes)
```
   

Ответ 25
</details>

<hr />


