---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999564"
---
# <a name="ajax"></a><span data-ttu-id="87866-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="87866-103">AJAX</span></span>

<span data-ttu-id="87866-104">Функции AJAX в Windows Internet Explorer 8, такие как [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) и [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) , имеют собственные свойства, которые могут конфликтовать с существующими пользовательскими свойствами.</span><span class="sxs-lookup"><span data-stu-id="87866-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="87866-105">Windows Internet Explorer предоставляет новые свойства для определенных функций AJAX, таких как [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), даже в режиме совместимости.</span><span class="sxs-lookup"><span data-stu-id="87866-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="87866-106">При добавлении пользовательских свойств в объект события они могут конфликтовать с этими новыми свойствами, такими как **Source**.</span><span class="sxs-lookup"><span data-stu-id="87866-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="87866-107">Следующий пример кода работает в более ранних версиях Internet Explorer, но не в более новых версиях, так как новые функции используют свойство **Source** .</span><span class="sxs-lookup"><span data-stu-id="87866-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="87866-108">В следующем примере кода показано, как можно изменить этот объект, чтобы он оставался совместимым.</span><span class="sxs-lookup"><span data-stu-id="87866-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="87866-109">См. также</span><span class="sxs-lookup"><span data-stu-id="87866-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87866-110">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="87866-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



