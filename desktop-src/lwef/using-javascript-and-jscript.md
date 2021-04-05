---
title: Использование JavaScript и JScript
description: Использование JavaScript и JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133823"
---
# <a name="using-javascript-and-jscript"></a>Использование JavaScript и JScript

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Если для доступа к программному интерфейсу Microsoft Agent используется JavaScript или Microsoft JScript, следуйте соглашениям для этого языка, чтобы указать методы или свойства:

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

Для доступа к коллекциям объектов агента используйте функцию [**перечислителя**](https://www.bing.com/search?q=**Enumerator**) JScript. Однако версии JScript, представленные до Internet Explorer 4,0, не поддерживают эту функцию и не поддерживают коллекции. Чтобы получить доступ к методам и свойствам объекта [**character**](/windows/desktop/lwef/the-characters-object) , используйте [**символьный**](character-method.md) метод. Аналогично, чтобы получить доступ к свойствам объекта [**Command**](/windows/desktop/lwef/the-command-object) , используйте метод [**Command**](command-method.md) .

 

 