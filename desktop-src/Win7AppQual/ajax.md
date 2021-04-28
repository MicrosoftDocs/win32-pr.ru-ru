---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088762"
---
# <a name="ajax"></a>AJAX

Функции AJAX в Windows Internet Explorer 8, такие как [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) и [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) , имеют собственные свойства, которые могут конфликтовать с существующими пользовательскими свойствами.

Windows Internet Explorer предоставляет новые свойства для определенных функций AJAX, таких как [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), даже в режиме совместимости. При добавлении пользовательских свойств в объект события они могут конфликтовать с этими новыми свойствами, такими как **Source**.

Следующий пример кода работает в более ранних версиях Internet Explorer, но не в более новых версиях, так как новые функции используют свойство **Source** .


```JScript
event.source = myObject;
```



В следующем примере кода показано, как можно изменить этот объект, чтобы он оставался совместимым.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Устранение проблем совместимости в веб-приложениях с помощью представления совместимости](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



