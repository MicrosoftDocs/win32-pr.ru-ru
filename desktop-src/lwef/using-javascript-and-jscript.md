---
title: Использование JavaScript и JScript
description: Использование JavaScript и JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960684"
---
# <a name="using-javascript-and-jscript"></a>Использование JavaScript и JScript

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

если вы используете JavaScript или Microsoft JScript для доступа к интерфейсу программирования microsoft Agent, следуйте соглашениям для этого языка, чтобы указать методы или свойства:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

В настоящее время JavaScript не имеет синтаксиса событий для объектов, отличных от HTML. Однако в Internet Explorer можно использовать `<SCRIPT>` тег **for... Синтаксис события** :

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Поскольку не все браузеры поддерживают этот синтаксис событий, может потребоваться использовать JavaScript только для страниц, поддерживающих Microsoft Internet Explorer, или для кода, который не требует обработки событий.

для доступа к коллекциям объектов агента используйте функцию [**перечислителя**](https://www.bing.com/search?q=**Enumerator**) JScript. однако версии JScript, добавленные до Internet Explorer 4,0, не поддерживают эту функцию и не поддерживают коллекции. Чтобы получить доступ к методам и свойствам объекта [**character**](/windows/desktop/lwef/the-characters-object) , используйте [**символьный**](character-method.md) метод. Аналогично, чтобы получить доступ к свойствам объекта [**Command**](/windows/desktop/lwef/the-command-object) , используйте метод [**Command**](command-method.md) .

 

 