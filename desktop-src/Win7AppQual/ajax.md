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
# <a name="ajax"></a><span data-ttu-id="8f28a-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="8f28a-103">AJAX</span></span>

<span data-ttu-id="8f28a-104">Функции AJAX в Windows Internet Explorer 8, такие как [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) и [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) , имеют собственные свойства, которые могут конфликтовать с существующими пользовательскими свойствами.</span><span class="sxs-lookup"><span data-stu-id="8f28a-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="8f28a-105">Windows Internet Explorer предоставляет новые свойства для определенных функций AJAX, таких как [Обмен сообщениями между документами (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), даже в режиме совместимости.</span><span class="sxs-lookup"><span data-stu-id="8f28a-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="8f28a-106">При добавлении пользовательских свойств в объект события они могут конфликтовать с этими новыми свойствами, такими как **Source**.</span><span class="sxs-lookup"><span data-stu-id="8f28a-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="8f28a-107">Следующий пример кода работает в более ранних версиях Internet Explorer, но не в более новых версиях, так как новые функции используют свойство **Source** .</span><span class="sxs-lookup"><span data-stu-id="8f28a-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="8f28a-108">В следующем примере кода показано, как можно изменить этот объект, чтобы он оставался совместимым.</span><span class="sxs-lookup"><span data-stu-id="8f28a-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="8f28a-109">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="8f28a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f28a-110">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="8f28a-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



