# JavaScriptStyleGuideMironova


## Правила оформления JavaScript-кода


1.[Объекты](#объекты)

  1.1 [Создание объекта](#создание-объекта)

  1.2 [Зарезервированные слова](#зарезервированные-слова)

  1.3 [Ключевые слова](#ключевые-слова)

  1.4 [Создание обьекта на 3 и более элементов](#создание-объекта-на-3-и-более-элементов)

1.[Переменные](#переменные)


1.[Функции](#функции)


  3.1 [Именование функции](#именование-функции)

  3.2 [Передача функции в функцию](#передача-функции-в-функцию)


1.[Отступы](#отступы)


  4.1 [Горизонтальные отступы](#горизонтальные-отступы)

  4.2 [Вертикальные отступы](#вертикальные-отступы)


1.[Пробелы](#пробелы)


1.[Скобки](#скобки)


1.[Кавычки](#кавычки)


1.[Точка с запятой](#точка-с-запятой)


1.[Комментарии](#комментарии)


## 1. Объекты


### 1.1 Создание объекта


Для создания объекта используйте фигурные скобки. Не создавайте объекты через конструктор new Object.


Хорошо


`  var item = {};`


Плохо


`  var item = new Object();`


### 1.2 Зарезервированные слова


Не используйте зарезервированные слова в качестве ключей объектов. Они не будут работать в IE8.


**Хорошо**


`  var superman = {
    defaults: { clark: 'kent' },
    hidden: true
  };`


**Плохо**


`  var superman = {
    default: { clark: 'kent' },
    private: true
  };`


### 1.3 Ключевые слова


Не используйте ключевые слова (в том числе измененные). Вместо них используйте синонимы.

**Хорошо**


`  var superman = {
    type: 'alien'
  };`


**Плохо**


`  var superman = {
    class: 'alien'
  };`


### 1.4 Создание обьекта на 3 и более элементов.


При создании обьектов, равно как и массивов, содержащих большое количество свойств(элементов), и тем самым образующих строки, длиной более 20 символов, необходимо выполнять ряд условий:


  -[Открывающая скобка располагается на той же строке;]
  -[Каждое свойство оформляется на новой строке;]
  -[Пробел после двоеточия;]
  -[Закрывающая скобка располагается на новой строке.]


**Хорошо**


`  var superman = {
    defaults: { clark: 'kent' },
    type: 'alien',
    hidden: true
  };`


**Плохо**


`  var superman = {defaults: { clark: 'kent' }, type: 'alien', hidden: true};`


## 2. Переменные


Для именования переменных используйте существительные на английском языке(не транслит!). Имя переменной должно быть осмысленным.
Имя может состоять из букв, цифр, символов $ и _, не должно начинаться с цифры.


**Хорошо**


`  var vegetables;
  Плохо
  var ovoschi;
  var rrfgov;`


## 3. Функции


### 3.1 Именование функции


Имя функции должно быть глаголом на английском языке или начинаться с него. Для имён, состоящих из нескольких слов, используйте camelCase.


**Хорошо**


`  function editName() {
    // тело функции
  };`


**Плохо**


`  function pravkaspiska() {
    // тело функции
  };`


### 3.2 Передача функции в функцию


При передаче функции, как аргумент в другую функцию, оформляйте код как в примере ниже.


`  var arr = ['Яблоко', 'Апельсин', 'Груша'].forEach(function (item, i, arr) {
    alert(i + ': ' + item + ' (массив:' + arr + ')');
  });`


## 4. Отступы


### 4.1 Горизонтальные отступы


Отступ при вложенности - 2 пробела на каждый уровень вложенности.

**Хорошо**


`  if (age < 98) {
    for (var i = 0, iMax = items.length; i < iMax; ++i) {
      // тело цикла
    }
  }`


**Плохо**


`  if (age < 98) {
  for (var i = 0, iMax = items.length; i < iMax; ++i) {
  // тело цикла
  }
  }`


### 4.2 Вертикальные отступы


Между логическими блоками(циклами, функциями и т.д.) следует оставлять пустую строку. Это делает код более читабельным. Избегайте блоков кода более 9 строк подряд.


**Хорошо**


`  var i;
  var iMax = items.length;
  for (i = 0; i < iMax, ++i) {
    // тело цикла
  }

  function showName() {
    // тело функции
  }`


**Плохо**


`  var i;
  var iMax = items.length;

  for (i = 0; i < iMax, ++i) {
    // тело цикла
  }
  function showName() {
    // тело функции
  }`


## 5. Пробелы


Используйте пробелы между параметрами и не используйте между именем функции и скобкой;


**Хорошо**


`  function edit(name, age) {
    // тело функции
  }`


**Плохо**


`  function edit (name,age) {
    // тело функции
  }`


При создании анонимной функции необходимо использовать пробел перед скобкой;


**Хорошо**


`  function (name, age) {
    // тело функции
  }`


**Плохо**


`  function(name,age) {
    // тело функции
  }`


Используйте пробелы вокруг операторов.


**Хорошо**


`  if (age < 100) {
    // тело цикла
  }`


**Плохо**


`  if (age<100) {
    // тело цикла
  }`


## 6. Скобки


Открывающая фигурная скобка располагается на той же строке. Перед скобкой пробел. Закрывающая скобка располагается на новой строке.


**Хорошо**


`  function edit(name, age) {
    if (age < 100) {
      // тело цикла
    }
  }`


**Плохо**


`  function edit(name, age)
  {
    if (age < 100) {/*тело цикла*/}
  }`


## 7. Кавычки


Всегда в коде скрипта используйте одинарные кавычки, если не требуется иного. Двойные кавычки допустимы, если в этой же строке необходимо использовать апостроф (') или одинарные кавычки для других целей.


**Хорошо**


`  var string = 'строка';
  var phrase = "you're next";`


**Плохо**


`  var string = "строка";`


## 8. Точка с запятой


В конце выражения обязательна точка с запятой.


**Хорошо**


`  alert('Привет');
  alert('Мир');`


**Плохо**


`  alert('Привет')
  alert('Мир')`


## 9. Комментарии


Для пояснения кода используются комментарии. Комментарии не исполняются интерпретатором JavaScript.


Однострочные комментарии начинаются с двойного слэша //. За ним обязательно должен идти пробел;
Многострочные комментарии располагаются между /* и */. За символом начала комментария обязательно должен идти пробел. Символ конца комментария располагается на новой строке.


**Хорошо**


`  /* Пример комментария.
  Многострочного комментария.
  */`


`  // Пример однострочного комментария.`


**Плохо**


`  /*Пример комментария.
  Многострочного комментария.*/`



`  //Пример однострочного комментария.`
