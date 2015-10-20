# Задача к лекции «Замыкания в Javascript» – «Мальчишник в Вегасе»

:sos: [Как создать Pull Request](https://github.com/urfu-2015/guides/blob/master/how-to-pull-request.md)  
:warning: При создании PullRequest'а не забудьте указать ваши имя и фамилию.

### Общие требования

Мы очень хотим, чтобы код вы написали сами, а __не пользовались внешними библиотеками__.

Прежде чем отправлять решение проверьте его на соответствие [общим требованиям](https://github.com/urfu-2015/guides/blob/master/js-codestyle.md).

А также на соответствие codestyle. Для этого в корне выполните:

```js
// Устанавливаем проверяльщик
npm install

// Проверяем
npm run test

// В результате выведутся ошибки, если они есть
// Если какие-либо ошибки будут не понятны – смело спрашиваем у ментора
```

### Задача

Как-то я (Сергей) посмотрел фильм «Мальчишник в Вегасе» и подумал, что неплохо
было бы устроить отвязный мальчишник. Как я узнал позже, для этого, конечно,
необходимо жениться :(. Поэтому мне надо устроить и мальчишник, и свадьбу.

У меня есть книга друзей, где описаны друзья и их связи с другими друзьями
__faceBook.js__. Чтобы было удобно искать друзей, я решил написать итератор
__iterator.js__.

Он умеет обходит друзей начиная с того, кого указываешь при создании итератора:

```js
//  phoneBook   – книга
//  Cергей      - ищем с себя
//  3           – максимальное кол-во рукопожатий до человека (при превышении обход завершается)
var friends = iterator.get(phoneBook, 'Cергей', 3);

// Берём следующего друга
// .next() Возращается JSON с именем и телефоном
friends.next(); // { name: 'Васян', phone: '+70000000000' }

// .prev() Возвращаемся к предыдущему
friends.prev();
```

Принципы обхода:

- Обход мы начинаем с ближайших друзей, затем берём ближайших друзей ближайших друзей
  (следующий круг рукопожатий) и так далее.

- Если друзей у человека несколько обходим их в АЛФАВИТНОМ порядке

- Если нет следующего друга, `.next()` должен возвращать `null`

- Если нет предыдущего друга, `.prev()` должен возвращать `null`

- Если стартовой точки обхода не существует в книге, `.next()` и `.prev()` должны возвращать `null`

Подробности вас ждут в файле __index.js__.

### Необязательное задание (+80 к логике)

Дополнительное задание описано в в файле __index.js__.  
Будет непоправимо круто, если вы его осилите!

![](http://st-im.kinopoisk.ru/im/kadr/8/6/7/kinopoisk.ru-The-Hangover-867067.jpg)
