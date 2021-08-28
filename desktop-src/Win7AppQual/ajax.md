---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e683bb441642e8f9764ac0cfe8313d0aa0df92ae3276f986f5fdf6837d6c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795924"
---
# <a name="ajax"></a>AJAX

функции AJAX в Windows Internet Explorer 8, такие как [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) и [обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) , имеют собственные свойства, которые могут конфликтовать с существующими пользовательскими свойствами.

Windows Internet Explorer предоставляет новые свойства для определенных функций AJAX, таких как [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), даже в режиме совместимости. При добавлении пользовательских свойств в объект события они могут конфликтовать с этими новыми свойствами, такими как **Source**.

Следующий пример кода работает в более ранних версиях Internet Explorer, но не в более новых версиях, так как новые функции используют свойство **Source** .


```JScript
event.source = myObject;
```



В следующем примере кода показано, как можно изменить этот объект, чтобы он оставался совместимым.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устранение проблем совместимости в веб-приложениях с помощью представления совместимости](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



