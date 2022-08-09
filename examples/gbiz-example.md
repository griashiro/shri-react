---

layout: yandex2

style: |
    /* собственные стили можно писать здесь!! */
    .add-margin-bottom {
        margin-bottom: 80px !important;
    }

    .smaller h2 {
        font-size: 90px !important;
    }

    strong em,
    .blockquote em {
        font-style: italic !important;
    }

    .shout h2 {
        width: 100%;
        text-align: center;
    }

    .wide-picture-caption {
        width: 1000px !important;
    }

    .reduce-line-height code {
        line-height: 1.2 !important;
    }

    .monospaced, 
    .monospaced h2{
        font-family: Hack, monospaced !important;
    }

    .wide-gif img {
        width: 1000px;
    }

    .tape img {
        width: 500px;
        margin-left: 150px !important;
    }
    .glue img {
        width: 600px;
    }

---



<!-- Первый слайд (Титульник) -->
# ![](themes/yandex2/images/logo-{{ site.presentation.lang }}.svg){:.logo}

<!-- Второй слайд: Название и Автор -->
## {{ site.presentation.title }}
{:.title.smaller}

### ![](themes/yandex2/images/title-logo-{{ site.presentation.lang }}.svg){{ site.presentation.service }}

<div class="authors">

{% if site.author %}
<p>{{ site.author.name }}{% if site.author.position %}, {{ site.author.position }}{% endif %}</p>
{% endif %}

</div>



<!-- Начало презентации -->



## λ-исчисление
{:.fullscreen}

![](pictures/math.jpg)
<figure markdown="1">
λ-исчисление
</figure>



## Сделать код *понятнее*
{:.blockquote}

## JavaScript
{:.fullscreen}

![](pictures/js.jpeg)
<figure markdown="1">
JavaScript
</figure>



## Коалы тоже грустят
{:.fullscreen}

![](pictures/sad-coala.jpg)
<figure markdown="1">
Коалы тоже грустят
</figure>



## Понимание = Доверие
{:.blockquote}




## Функциональный свет
{:.fullscreen}

![](pictures/light.jpg)
<figure markdown="1">
Добавить функционального света
</figure>
{:.wide-picture-caption}



## ЧТО *проще* КАК
{:.blockquote}



## Императивный vs Декларативный
{:.section.smaller}

### Все дело в стиле



## Мам, хочу пиццу!
{:.fullscreen}

![](pictures/pizza.jpg)
<figure markdown="1">
Мам, хочу пиццу!
</figure>



## Мам, возьми муку, замеси тесто...
{:.fullscreen}

![](pictures/testo.jpg)
<figure markdown="1">
Мам, возьми муку, замеси тесто...
</figure>
{:.wide-picture-caption}



## Императивный vs Декларативный

```js
const array = [1, 2, 3, 4, 5]
const isEven = (x) => x % 2 === 0
```

```js
// императивный стиль
const evenNumbers = []

for (let i = 0; i < array.length; i++) {
    if (isEven(array[i])) {
        evenNumbers.push(array[i])
    }
}
```
{:.next}



## Императивный vs Декларативный

```js
const array = [1, 2, 3, 4, 5]
const isEven = (x) => x % 2 === 0
```

```js
// декларативный стиль
const evenNumbers = array.filter(isEven)
```
{:.next}




## Каждый из нас по своему котик
{:.fullscreen}

![](pictures/team.jpg)
<figure markdown="1">
Каждый из нас по своему котик
</figure>
{:.wide-picture-caption}



## Который любит звезды
{:.fullscreen}

![](pictures/sky.jpg)
<figure markdown="1">
Который любит звезды
</figure>




## Итак, вы решили изучить ФП
{:.section.smaller}



## Первый раз за рулем
{:.fullscreen}

![](pictures/first.jpg)
<figure markdown="1">
Первый раз за рулем
</figure>



## Опытный водитель
{:.fullscreen}

![](pictures/car.jpg)
<figure markdown="1">
Уже опытный водитель
</figure>



## Похожие технологии
{:.fullscreen}

![](pictures/learn.jpg)
<figure markdown="1">
Похожие технологии изучать проще
</figure>
{:.wide-picture-caption}




## За штурвалом вертолета
{:.fullscreen}

![](pictures/fly.jpg)
<figure markdown="1">
Тут все по другому
</figure>



## Снова про дзен
{:.fullscreen}

![](pictures/meditation.jpg)
<figure markdown="1">
Очистить разум. Стать пустым.
</figure>
{:.wide-picture-caption}



## Дверь в новый мир
{:.fullscreen}

![](pictures/door.jpg)
<figure markdown="1">
Дверь в новый мир
</figure>



## Декларативные языки

```css
/* css */
.button {
    width: 42px;
}
```
{:.next}

```sql
-- SQL
SELECT title, genre
FROM films
WHERE rating > 7
```
{:.next}



## На заметку

**Задача ФП - сделать код понятнее**
{:.add-margin-bottom}

- ...Понимание = Доверие
- ...ЧТО *проще* КАК
- {:.next.monospaced}I = []



## function не всегда f(x)
{:.section}

### Функции в деталях



## Лейбниц
{:.fullscreen}

![](pictures/leibniz.jpg)
<figure>
Функция
</figure>



## Джон Мокли
{:.fullscreen}

![](pictures/eniac.jpg)

<figure>
Процедура
</figure>



## Функции vs Процедуры

**В JS и функции и процедуры - это function**

```js
// функция
function sqr (x) {
    return x * x
}
```
{:.next}

```js
// процедура - функция с побочными эффектами
function print (text) {
    console.log(text)
}
```
{:.next}



## Терминология
{:.section}

### Функции в деталях



## Параметры и Аргументы

- ...<b>Параметры</b> - переменные в объявлении функции
- ...<b>Аргументы</b> - конкретные значения, переданные при вызове

```js
function fetch (url, options) {
    // ... ajax запрос
}
```
{:.next}

```js
const options = { method: 'GET' }
fetch ('/api', options)
```
{:.next}



## Сигнатура

**Количество, порядок и тип параметров**

```js
// утиная типизация

function fetch (url, options)
```
{:.next}



## Сигнатура

**Количество, порядок и тип параметров**

```js
// JSDoc

/**
 * @param {string} url
 * @param {Object} [options]
 */
function fetch (url, options)
```

## Сигнатура

**Количество, порядок и тип параметров**

```js
// TypeScript

interface FetchOptions {
    method?: "GET" | "POST"
    // ... что-нибудь еще
}
```

```js
function fetch (url: string, options: FetchOptions)
```
{:.next}



## Арность

**Число параметров, хранится в свойстве length**

```js
function translate (text, lang)
```
{:.next}

```js
translate.length // 2
```
{:.next}


## Арность: хитрости

```js
// аргументы по умолчанию
function foo (x = 0)
```
{:.next}


```js
// остаточные параметры
function bar (...args)
```
{:.next}


```js
// деструктуризация
function baz ({a, b})
```
{:.next}

```js
foo.length // 0
bar.length // 0
baz.length // 1
```
{:.next}



## Функция первого класса
{:.fullscreen}

![](pictures/box.jpeg)
<figure >
Функция первого класса
</figure>



## Функция первого класса
{:.fullscreen}

![](pictures/cat.jpeg)
<figure >
Кто меня вызывал?
</figure>



## Функции первого класса

**Ведут себя как полноценные объекты**

```js
// можно создавать
const empty = () => {}
```
{:.next}

```js
// присваивать
const nothing = empty
```
{:.next}

```js
// возвращать и передавать
const toDo = (fn) => fn
toDo (nothing)()
```
{:.next}


## Функция высших порядков
{:.fullscreen}

![](pictures/hof.jpg)
<figure >
Функции высших порядков
</figure>



## Функции высших порядков

**Принимаю/возвращаю/создают другие функции**

```js
const array = [4, 8, null, 16, null, 42]
const normalized = array.filter(Boolean)
```
{:.next}

```js
document.body.addEventListener('click', () => {})
```
{:.next}

```js
fetch('/api').then((res) => res.json())
```
{:.next}



## Компоненты высших порядков

```jsx
import React from 'react';

const higherOrderComponent = (WrappedComponent) => {

  class HOC extends React.Component {
      render() {
          return <WrappedComponent />
      }
  }
    
  return HOC
}
```
{:.next}



## Замыкание

**Функция + её область видимости**

![](pictures/scope.jpg)
{:.image-right}

```js
function makeCounter (count = 0) {
    function printCount () {
        console.log(count)
    }

    return () => {
        count++
        printCount()
    }
}
```




## Замыкание

**Функция + её область видимости**

```js
const firstCounter = makeCounter()
const secondCounter = makeCounter(7)
```
{:.next}

```js
firstCounter() // 1
firstCounter() // 2
```
{:.next}

```js
secondCounter() // 8
```
{:.next}



## Лексикографическая область видимости

**Область видимости на момент создания функции**

```js
const area = 'global'

function local () {
    const area = 'local'
    return () => { console.log(area) }
}

const result = local()
```
{:.next}


```js
result() // 'local'
```
{:.next}



## [Замыкания в деталях](https://htmlacademy.ru/blog/195-lets-learn-javascript-closures){:target="_blank"}
{:.shout}







## Приключение начинается
{:.section}



## Композиция
{:.section}

### Эпизод 1



## Программа - поток данных
{:.fullscreen}

![](pictures/compose/flow.jpg)
<figure>
Программа - поток данных
</figure>



## Поток данных. Версия №1

```js
const text = `Съешь ещё этих мягких 
французских булок, да выпей же чаю`
```

```js
const wordsFound = words(text)
const wordsUsed = unique(wordsFound)
```
{:.next}

<div markdown='1' style='position: absolute; left: 400px'>

![](pictures/factory/factory1.png)
{:style='position: absolute; top: 45px' .next}

![](pictures/factory/factory2.png)
{:style='position: absolute; left: 700px' .next}

![](pictures/factory/store.png)
{:style='position: absolute; left: 350px; top: 80px; transform: scale(0.3)' .next}

</div>




## Поток данных. Версия №2

```js
const text = `Съешь ещё этих мягких 
французских булок, да выпей же чаю`

function uniqueWords (text) {
    return unique(words(text))
}

const wordsUsed = uniqueWords(text)
```


<div markdown='1' style='position: absolute; left: 400px; bottom: 360px;'>

![](pictures/factory/factory1.png)
{:style='position: absolute; left: 288px; top: 46px' .next}

![](pictures/factory/factory2.png)
{:style='position: absolute; left: 700px' .next}

![](pictures/factory/store.png)
{:style='position: absolute; left: -40px; top: 80px; transform: scale(0.3)' .next}

</div>



## Поток данных. Версия №2

```js
const text = `Съешь ещё этих мягких 
французских булок, да выпей же чаю`

function uniqueWords (text) {
    return unique(words(text))
}

const wordsUsed = uniqueWords(text)
```


<div markdown='1' style='position: absolute; left: 400px; bottom: 360px;'>

![](pictures/factory/factory3.png)
{:style='position: absolute; top: -220px; left: 360px; transform: scale(2.5); z-index: 10'}

</div>



## Серьёзно?
{:.fullscreen}

![](pictures/compose/woops.jpg)
<figure>
Серьёзно?
</figure>



## Композиция

**Фабрика для производства заводов**
{:.add-margin-bottom}

- ...Композиция - цепочка вложенных вызовов
- ...compose(h, g, f)(x) = h(g(f(x)))
- ...Конвейер который едет справа налево



## Конвейер

```bash
$ ls -l | grep '.txt'
```
{:.next}

```js
const double = (n) => n * 2
const increment = (n) => n + 1
```
{:.next}

```js
// без конвейерного оператора
double(increment(double(double(5)))) // 42
```
{:.next}

```js
// с конвейерным оператором
5 |> double |> double |> increment |> double // 42
```
{:.next}


## Поток данных. Версия №3

```js
const text = `Съешь ещё этих мягких 
французских булок, да выпей же чаю`

const uniqueWords = compose(unique, words)
const wordsUsed = uniqueWords(text)
```

<div markdown='1' style='position: absolute; left: 1100px; top: 100px;'>

![](pictures/factory/abstract-factory.png)
{:style='position: absolute; .next}

![](pictures/factory/factory3.png)
{:style='position: absolute; transform: scale(0.4); left: 208px; top: 40px;' .next}

</div>

<div markdown='1' style='position: absolute; left: -140px; bottom: 360px;'>

![](pictures/factory/factory1.png)
{:style='position: absolute; left: 288px; top: 46px' .next}

![](pictures/factory/factory2.png)
{:style='position: absolute; left: 700px' .next}

![](pictures/factory/store.png)
{:style='position: absolute; left: -40px; top: 80px; transform: scale(0.3)' .next}

![](pictures/factory/close.png)
{:style='position: absolute; top: 260px; left: 135px; transform: scale(2)' .next}

</div>






## Point Free Style

**Функции не упоминает данные, которые обрабатывают**

```js
// "точечный" стиль, используется параметр text
function uniqueWords (text) {
    return unique(words(text))
}
```
{:.next}

```js
// "бесточечный" стиль
const uniqueWords = compose(unique, words)
```
{:.next}



## Функции - это кубики Lego
{:.fullscreen}

![](pictures/compose/lego.jpg)
<figure>
Функции - это кубики Lego
</figure>



## Полезная деталь
{:.fullscreen}

![](pictures/compose/part.jpg)
<figure>
Полезная деталь
</figure>



## Полезная деталь

```js
const text = `Съешь ещё этих мягких 
французских булок, да выпей же чаю`
```

```js
// полезная деталь
const uniqueWords = compose(unique, words)
```

```js
// которая пригодится для новых построек
const uniqueWordsCount = compose(count, uniqueWords)
```



## [Реализация композиции в Redux](https://github.com/reduxjs/redux/blob/47f36156971807a764613a13f04b4210ece48e58/src/compose.js#L12){:target="_blank"}
{:.shout.smaller}


## Пора добавить еще одну деталь


```js
function translater (lang, words)

const translate = compose(translater, unique, words)
```

```js
translate(text) // Booom! 💥
```
{:.next}




## Как так?!
{:.images.wide-gif}

![](pictures/compose/shock.gif)



## Продолжение следует...
{:.shout}




## Каррирование
{:.section}

### Эпизод 2



## В предыдущих сериях


- ...Композиция
- ...Бесточечный стиль


```js
function translater (lang, words)

const translate = compose(translater, unique, words)
```
{:.next}

```js
translate(text) // Booom! 💥
```
{:.next}



## Проблема в разных сигнатурах
{:.images.wide-gif}

![](pictures/curry/adapter.gif)



## Каррирование - это супер клей

![](pictures/curry/glue.png)
{:.image-left.glue}

**Преобразует функцию в *набор* функций с меньшим числом параметров**
{:.add-margin-bottom .next}

...Алгоритм:

1. ...Нанести на функцию клей
2. ...Клеить аргументы по одному и получать новую функцию
3. ...Функция вызовется как только будет передан последний аргумент




## Каррирование в действие

```js
function translater (lang, words)
```
{:.next}

```js
// наносим клей на функцию
const curriedTranslater = curry(translater)
```
{:.next}

```js
// приклеиваем аргумент, получаем новую функцию
const translateToRU = curriedTranslater('ru')
```
{:.next}

```js
const translate = compose(translateToRU, unique, words)
```
{:.next}

```js
translate(text) // теперь все работает 
```
{:.next}


## Каррирование в деталях
<!-- 1-й слайд -->

```js
function sum (x, y, z) {
    return x + y + z
}
```
{:.next}

```js
// наносим клей на функцию
const curriedSum = curry(sum)
```
{:.next}

```js
curriedSum(3) // sum(3)
```
{:.next}

```js
curriedSum(3)(14) // sum(3, 14)
```
{:.next}

```js
curriedSum(3)(14)(15) // 32
```
{:.next}



## Каррирование в деталях
<!-- 2-й слайд -->

```js
function sum (x, y, z) {
    return x + y + z
}
```

```js
// наносим клей на функцию
const curriedSum = curry(sum)
```

```js
const addTo42 = curriedSum(42) // sum(42)
```
{:.next}

```js
addTo42(20)(38) // 100
```
{:.next}



## Каррирование в деталях
<!-- 3-й слайд -->

```js
function sum (x, y, z) {
    return x + y + z
}
```

```js
// наносим клей на функцию
const curriedSum = curry(sum)
```

```js
const addTo42 = curriedSum(42) // sum(42)
```

```js
// клеим все что осталось за раз
addTo42(20, 38) // 100
```
{:.next}



## Частичное применение - это изолента

![](pictures/curry/tape.png)
{:.image-left.tape}

**Преобразует функцию в *единственную* функцию с меньшим числом параметров**
{:.add-margin-bottom .next}

...Алгоритм:

1. ...Примотать изолентой параметры к функции
2. ...Вызвать функцию



## Частичное применение в деталях

```js
// мотаем изолентой параметр к функции
const partialSum = partial(sum, 42)
```
{:.next}

```js
partialSum(20, 38) // 100
```
{:.next}

```js
partialSum(17) // NaN
```
{:.next}




## Частичное применение в действии

```js
function translater (lang, text)
```
{:.next}

```js
const translateToRU = partial(translater, 'ru')
```
{:.next}

```js
translateToRU(text) // все работает
```
{:.next}



## Частичное применение из коробки

```js
function translater (lang, text)
```

```js
const translateToRU = translater.bind(null, 'ru')
```
{:.next}

```js
translateToRU(text) // все снова работает
```
{:.next}



## Порядок аргументов имеет значение

```js
// Iteratee-first Data-last
function translater (lang, text)
```
{:.next}

```js
// Iteratee-last Data-first
function translater (text, lang)
```
{:.next}



## Привязка аргументов с конца

```js
function translater (text, lang)
```

```js
// flip меняет порядок аргументов
const curryRight = compose(curry, flip)
const curriedTranslate = curryRight(translater)
```
{:.next}

```js
const translateToRU = curriedTranslate('ru')
```
{:.next}

```js
translateToRU(text) // все работает
```
{:.next}



## Привязка аргументов с конца

```js
function translater (text, lang)
```

```js
const translateToRU = partialRight(translater, 'ru')
```

```js
translateToRU(text) // все снова работает
```
{:.next}



## Специализация
{:.fullscreen}

![](pictures/curry/store.jpeg)
<figure>
Специализация
</figure>


## Специализация в действии

```js
function ajax (url, data, callback) {
	// ... асинхронный запрос
}
```

```js
// наносим клей на функцию
const curriedAjax = curry(ajax)
```
{:.next}

```js
// специализация
const userFetcher = curriedAjax('api/users')
```
{:.next}

```js
// еще больше специализации
const currentUserFetcher = curriedAjax('api/users', { user: USER_ID })
```
{:.next}


## Реализация [curry](https://hackernoon.com/currying-in-js-d9ddc64f162e){:target="_blank"} и [partial](https://github.com/getify/Functional-Light-JS/blob/master/manuscript/ch3.md#some-now-some-later){:target="_blank"}
{:.shout.smaller}


## И если у вас еще нет изоленты
{:.images}

![](pictures/curry/take-tape.jpeg)


## Грозовые тучи побочных эффектов
{:.fullscreen}

![](pictures/clouds.jpeg)
<figure>
Грозовые тучи побочных эффектов
</figure>
{:.wide-picture-caption}



## Продолжение следует...
{:.shout}



## Чистота
{:.section}

### Эпизод 3



## В предыдущих сериях
{:.shout}



## В предыдущих сериях
- ...Каррирование
- ...Частичное применение
- ...Специализация



## Грозовые тучи побочных эффектов
{:.fullscreen}

![](pictures/clouds.jpeg)
<figure>
Грозовые тучи побочных эффектов
</figure>
{:.wide-picture-caption}



## И вот за окном идет дождь
{:.fullscreen}

![](pictures/rain.jpeg)
<figure >
И вот за окном идет дождь
</figure>
{:.wide-picture-caption}



## Коалы тоже грустят
{:.fullscreen}

![](pictures/sad-coala.jpg)
<figure markdown="1">
Коалы тоже грустят
</figure>



## Непредсказуемые последствия
{:.fullscreen}


![](pictures/tea.jpeg)
<figure >
Непредсказуемые последствия
</figure>
{:.wide-picture-caption}




## Побочные эффекты

- ...Глобальные переменные
- ...Мутация данных
- ...Взаимодействие с внешним миром



## Побочные эффекты: Глобальные переменные

```js
let status = 404
```
{:.next}

```js
function isSuccess () {
    return status === 200 ? true : false
}
```
{:.next}

```js
function isSuccess (status) {
    return status === 200 ? true : false
}
```
{:.next}



## Побочные эффекты: Мутация данных

```js
const fruits = ['orange', 'apple', 'banana']
```
{:.next}

```js
function sortFruits (fruits) {
    return fruits.sort()
}
```
{:.next}

```js
const sortedFruits = sortFruits(fruits)
sortedFruits // ['apple', 'banana', 'orange']
```
{:.next}

```js
fruits // ['apple', 'banana', 'orange']
```
{:.next}



## Побочные эффекты: Мутация данных

```js
const fruits = ['orange', 'apple', 'banana']
```

```js
function sortFruits (fruits) {
    const copy = [...fruits]
    return copy.sort()
}
```
{:.next}

```js
const sortedFruits = sortFruits(fruits)
sortedFruits // ['apple', 'banana', 'orange']
```
{:.next}

```js
fruits // ['orange', 'apple', 'banana']
```
{:.next}



## Побочные эффекты: I/O

```js
function arrange () {
    const data = fetch('/api')
    // ... работа с data
}
```
{:.next}

```js
const data = fetch('/api')

function arrange (data) {
    // ... работа с data
}
```
{:.next}


## Борьба с побочными эффектами

- ...Чистые функции
- ...Иммутабельные (неизменяемые) данные



## Чистые функции

**Без побочных эффектов**
{:.add-margin-bottom}

- ...Работают детерминированно
- ...Вызывают только чистые функции


## Чистые функции: Детерменированность

```js
function sqr (x) {
    return x * x
}
```
{:.next}

```js
function random () {
    return Math.random()
}
```
{:.next}


## Чистые функции: Только чистота

```js
let state = 'ok'

function notPure () {
    state = null
}
```
{:.next}

```js
function pure () {
    notPure() // вызов нечистой функции
}
```
{:.next}



## Чистота относительна
{:.blockquote}



## Чистые функции: Мемоизация

**Функция с памятью**
{:.next}

```js
const sqr = memoize(x => x * x)
```
{:.next}

```js
const sqr = (function () {
    const cache = {}; // мемоизация
    return (x) => {
        if (cache[x]) {
            return cache[x]
        }
        // ... вычислить квадрат
    }
})()
```
{:.next}


## Чистые функции: преимущества

- ...Кешируемость
- ...Простота
- ...Ссылочная прозрачность
- ...Легко тестировать
- ...Легко распараллеливать



## Чистые функции  ❤️  Неизменяемые данные
{:.shout.smaller}



## JS очень динамичен

```js
const immutable = {value: 42, sadness: {level: 3}}
immutable = {} // ошибка
```
{:.next}

```js
immutalbe.value = 23
```
{:.next}

```js
const frozen = Object.freeze(immutable)
immutalbe.value = 23 // ошибка
```
{:.next}

```js
froze.sadness.level = 100500 // :(
```
{:.next}



## Копия данных: Объекты

```js
const state = { value: 42 }
```
{:.next}

```js
const copy = Object.assign({}, state)
```
{:.next}

```js
const copy = {...state}
```
{:.next}


## Копия данных: Массивы

```js
const fruits = ['orange', 'apple', 'banana']
```
{:.next}

```js
const copy = [].concat(fruits)
```
{:.next}

```js
const copy = [...fruits]
```
{:.next}



## Настоящая неизменяемость
{:.images .two}

[![](pictures/immutable.png)](https://facebook.github.io/immutable-js/){:target="_blank"}

[![](pictures/immer.png)](https://github.com/mweststrate/immer#immer){:target="_blank"}



### На картинки можно кликать


## Чистота и неизменяемость в Redux


```js
function addTodo (state = initialState, action) {
    switch (action.type) {
        case ADD_TODO: {
            return {
                ......state,
                todos: [ ......state.todos, action.todo ]
            }
        }
        default: return state
    }
}
```


## Абсолютная чистота

```js
const nothing = () => {}
```
{:.next}


## Абсолютная чистота

```js
const nothing = () => {} // бесполезная программа
```

**Программы пишут ради побочных эффектов**
{:.add-margin-bottom.next}

**Наша задача свести побочные эффекты к минимуму**
{:.next}


## чистые функции и неизменяемые данные <br>*наше все*
{:.blockquote.smaller}


## Финал
{:.section}


## Быстрое погружение
{:.fullscreen}

![](pictures/boom.jpg)
<figure >
Быстрое погружение
</figure>


## Ключ в мир ФП
{:.fullscreen}

![](pictures/key.jpeg)
<figure >
Ключ в новый мир
</figure>


## Ключ в мир ФП

- ...[Functional-Light JavaScript](https://github.com/getify/functional-light-js#functional-light-javascript){:target="_blank"}
- ...[Mostly adequate guide to FP](https://github.com/MostlyAdequate/mostly-adequate-guide#about-this-book){:target="_blank"}
- ...[Functional Programming Jargon](https://github.com/hemanth/functional-programming-jargon#functional-programming-jargon){:target="_blank"}
- ...[Ramda](https://ramdajs.com){:target="_blank"}



## Благодарности

Алексею Калину,<br>Диме Андриянову,<br>Лейсан Гильфановой,<br>Артуру Кенжаеву,<br>Александру Павловичу,<br>Руслану Хуснетдинову,<br>Валерию Гордееву,<br>Марине Максимовой,<br>Светлане Мерзляковой


## Я понял кое-что важное
{:.images}

![](pictures/kail.jpg)


## Каррируй.
{:.shout.smaller}
## Каррируй. Композируй.
{:.shout.smaller}
## Каррируй. Композируй. Очищай.
{:.shout.smaller}



<!-- ## Контакты 
{:.contacts}

{% if site.author %}

<figure markdown="1">

### {{ site.author.name }}

{% if site.author.position %}
{{ site.author.position }}
{% endif %}

</figure>

{% endif %}

{% if site.author2 %}

<figure markdown="1">

### {{ site.author2.name }}

{% if site.author2.position %}
{{ site.author2.position }}
{% endif %}

</figure>

{% endif %} -->

<!-- разделитель контактов -->
<!-- ------- -->

<!-- left -->
<!-- - {:.skype}author
- {:.mail}author@yandex-team.ru
- {:.github}author -->

<!-- right -->
<!-- - {:.twitter}@author
- {:.facebook}author -->

<!-- 

- {:.mail}author@yandex-team.ru
- {:.phone}+7-999-888-7766
- {:.github}author
- {:.bitbucket}author
- {:.twitter}@author
- {:.telegram}author
- {:.skype}author
- {:.instagram}author
- {:.facebook}author
- {:.vk}@author
- {:.ok}@author

-->
