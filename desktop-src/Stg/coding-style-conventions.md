---
title: Соглашения о стиле написания кода
description: В этой серии примеров используются соглашения о стиле написания кода для облегчения ясности и согласованности.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797371"
---
# <a name="coding-style-conventions"></a>Соглашения о стиле написания кода

В этой серии примеров используются соглашения о стиле написания кода для облегчения ясности и согласованности. Используются соглашения об нотации "Венгерский". Они стали распространенной практикой программирования в программировании Win32. Они включают в себя обозначения префикса переменной, которые придают именам переменных предложение типа переменной.

В следующей таблице перечислены стандартные префиксы.



| Prefix | Описание                         |
|--------|-------------------------------------|
| а      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| CB     | Число байтов                      |
| Кредит     | Значение ссылки цвета               |
| /CX     | Число x (коротких)                  |
| dw     | DWORD (без знака)               |
| f      | Флаги (обычно несколько битовых значений) |
| fn     | Функция                            |
| модуле\_    | Глобальный                              |
| h      | Дескриптор                              |
| i      | Целочисленный тип                             |
| l      | Long                                |
| lp     | Длинный указатель                        |
| Пн\_    | Элемент данных класса              |
| n      | Короткое целое                           |
| p      | Указатель                             |
| s      | Строка                              |
| SZ     | Строка, завершающаяся нулем              |
| tm     | Метрика текста                         |
| u      | Целое число без знака                        |
| признан     | Long без знака (ULONG)               |
| w      | WORD (без знака)               |
| x, y    | координаты x, y (краткое)            |



 

Они часто объединяются, как показано ниже.



| Сочетание префикса | Описание                                             |
|--------------------|---------------------------------------------------------|
| псзмистринг        | Указатель на строку.                                  |
| m \_ псзмистринг     | Указатель на строку, которая является элементом данных класса. |



 

Другие соглашения перечислены в следующей таблице.



| Обозначение       | Описание                                              |
|------------------|----------------------------------------------------------|
| кмикласс         | Префикс "C" для имен классов C++.                          |
| комйобжекткласс  | Добавьте префикс "CO" для имен классов COM-объектов.                  |
| кфмиклассфактори | Добавьте в префикс "CF" имена фабрик класса COM.                 |
| IMyInterface     | Префикс "I" для имен классов интерфейса COM.                |
| Цимпиминтерфаце | Для классов реализации COM-интерфейса следует добавить префикс "Цимпи". |



 

Некоторые последовательные соглашения для блоков заголовков комментариев используются в этой серии примеров, как показано ниже.

## <a name="file-header"></a>Заголовок файла

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>Блок простых комментариев

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Заголовок объявления класса

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>Заголовок определения метода класса

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Неэкспортированная или локальная функция

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>Заголовок определения экспортированной функции

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>Заголовок объявления COM-интерфейса

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>Заголовок объявления класса COM-объекта

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

Все эти соглашения блока комментариев имеют одинаковые начальные и конечные строки токена. Такая согласованность поддерживает автоматическую обработку заголовков каким бы то ни было образом. Например, скрипты AWK могут быть написаны для фильтрации заголовков функций в отдельный текстовый файл, который затем может служить основанием для документа спецификации. Аналогичным образом, такие средства, как неподдерживаемая служебная программа АУТОДУКК (в настоящее время доступная на компакт-диске библиотеки разработки Майкрософт для разработчиков сети), можно использовать для обработки блоков комментариев в этих заголовках.

В следующей таблице перечислены начальные и конечные строки токенов, используемые в примерах учебников.



| Токен | Описание                      |
|-------|----------------------------------|
| /\*+  | Начало заголовка файла                |
| +\*/  | Конец заголовка файла                  |
| /\*-  | Начало заголовка блока с обычными комментариями |
| -\*/  | Конец заголовка блока обычного комментария   |
| /\*Ц  | Начало заголовка класса               |
| Ц\*/  | Конец заголовка класса                 |
| /\*Пн  | Начало заголовка метода              |
| Пн\*/  | Конец заголовка метода                |
| /\*Ж  | Начало заголовка функции            |
| Ж\*/  | Конец заголовка функции              |
| /\*Сохранении  | Начало заголовка интерфейса           |
| Сохранении\*/  | Конец заголовка интерфейса             |
| /\*Вывода  | Начало заголовка класса COM-объекта    |
| Вывода\*/  | Конец заголовка класса COM-объекта      |



 

Эти заголовки также можно использовать в качестве визуальных подсказок для быстрого сканирования исходных файлов. Они также позволяют быстро получить доступ к определенному исходному расположению, если вы настроили строки поиска в редакторе, а затем "Повторить последний Поиск", чтобы быстро найти эти заголовки.

Например, строка поиска "M + M" найдет начало заголовков метода, а "M-M" найдет начало фактического определения метода или кода реализации.

 

 




