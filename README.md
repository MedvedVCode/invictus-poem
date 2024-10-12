# Приложение Invictus poem
это веб-приложение, которое выводит стихотворение. Кнопками управления можно отключать четверостишия. Каждой кнопке соответствует свое четверостишие. отключить можно все, кроме одного. Работает на любом разрешении монитора от 450пикс до 8000пикс.

## 1. Установка:
```sh
Node.js 20.17
npm
```

### Установка зависимостей

```sh
 npm install 
 ```

### Запуск приложения
```sh
 npm run dev
 ```
Приложение будет доступно по ссылке [http://localhost:5173](http://localhost:5173)

### Деплой и минификация приложения в папку dist
```sh
 npm run build
 ```

## 2. Структура проекта:
### src/: 
  * __components/__: Вложенные компоненты приложения 
	* HeaderComp.vue - выводит автора и название стихотаорения, получает их через __props: title и author__;
	* PoemTextComp.vue - выводит текст стихотворения, импортирует poem - массив объектов четверостиший, через computed метод showPoem выводит все четверостишия с флагом __isShowed:true__;
	* SwitcherComp.vue - выводит кнопки управления четверостишиями, импортирует poem - массив объектов четверостиший, содержит переменную __countShowedQuatrain__ - счетчик видимых четверостиший, через метод __quatrainShow__ включает/выключает четверостишия.
  * __assets/__: Статические ресурсы.
	* icon/: logo.svg - Иконка для закладки страницы
	* __styles/__: main.css - общие стили приложения 
  * __data-poem/__: Хранит данные проекта.
	* poem.js: содержит массив объектов с полями: __id, isShowed,quatrainText__.
  * App.vue: Основной компонент приложения, содержит остальные компоненты.
  * main.js: Точка входа приложения.

	## Контактная информация:
	Автор: Денис Федоров
	E-mail: ssboshen@yandex.ru
	Tel: @Denis_V_Fedorov