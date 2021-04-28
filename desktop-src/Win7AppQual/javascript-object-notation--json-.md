---
description: Нотация объектов JavaScript (JSON)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: Нотация объектов JavaScript (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b5f12a2c4e3a4cd0a66a8f917c3cdf41ed17d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088192"
---
# <a name="javascript-object-notation-json"></a>Нотация объектов JavaScript (JSON)

[Нотация объектов JavaScript (JSON)](https://www.json.org/) — это простой и упрощенный формат обмена данными, основанный на подмножестве нотации объектного литерала языка JavaScript. Подсистема JavaScript в Windows Internet Explorer 8 реализует [предложение ECMAScript 3,1 JSON](https://www.ecma-international.org/) для собственных функций обработки JSON (которые используют [json2.js API-интерфейс Дугласа Крокфорда](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).

Internet Explorer 8 включает собственный объект JSON, который соответствует поддержке JSON, описанной в [рабочем черновике предложения ES 3.1](https://www.ecma-international.org/). Некоторые веб-страницы обнаруживают собственный объект JSON, а затем используют его нестандартным способом. Такое использование обычно вызывает ошибку сценария и прерывает обработку запросов AJAX. В следующем примере кода показан неправильный способ использования объекта JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Вместо этого в следующем примере кода демонстрируется хороший способ использования объекта JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer содержит встроенную поддержку JSON, представляя глобальный объект JSON с двумя встроенными методами: **stringify** и **Parse**. Глобальный объект JSON определяется в подсистеме JavaScript и создается на этапе инициализации подсистемы. Для обеспечения обратной совместимости эта функция доступна, только если на веб-сайте используется последняя версия функций JavaScript с использованием режима макета "Internet Explorer 8 Standards" (документ). Эта функция также может повлиять на поведение веб-страниц, зависящих от глобальной переменной JSON, или использовать [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Можно переопределить глобальный объект JSON. Но если веб-страница использует режим макета "Internet Explorer 8 Standards" (документ), он больше не является неопределенным объектом. Так как модуль JavaScript создает экземпляр JSON в качестве глобального имени, он возвращает значение false, например "if (! this.JSON)", и в пользовательском коде его необходимо изменить.

Веб-страницы, использующие [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) , скорее всего, не затрагиваются. С некоторыми исключениями эти страницы должны работать быстрее. Исключения вызваны различиями в реализации собственного JSON и json2.js в обозревателе Internet Explorer. Например, во время сериализации собственная реализация JSON обнаруживает циклы и не переходит в бесконечную рекурсию, например json.js. Дополнительные сведения об этих исключениях см. в [блогах по JavaScript](/archive/blogs/jscript/).

Дополнительные сведения см. в статьях [Документация по JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) , [Управление версиями и поддержка версий модуля JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Устранение проблем совместимости в веб-приложениях с помощью представления совместимости](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
