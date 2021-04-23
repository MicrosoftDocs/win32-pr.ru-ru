---
title: Атрибуты wire_marshal и user_marshal
description: В этом разделе обсуждается реализация преобразования типов данных программиста с помощью атрибутов MIDL \ проводная \_ Упаковка \ и \ пользовательское \_ маршалирование \.
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070418"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="7df76-103">Атрибуты "проводное \_ маршалирование" и "пользовательское \_ маршалирование"</span><span class="sxs-lookup"><span data-stu-id="7df76-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="7df76-104">В этом разделе обсуждается реализация преобразования типов данных программиста с помощью \[ пользовательских АТРИБУТОВ MIDL [Wire \_ ](/windows/desktop/Midl/wire-marshal) \] и \[ [ \_ Marshal](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="7df76-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="7df76-105">Сведения представлены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7df76-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="7df76-106">Атрибут Wired \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="7df76-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="7df76-107">Атрибут пользовательской \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="7df76-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="7df76-108">Тип \_ Усерсизе функция</span><span class="sxs-lookup"><span data-stu-id="7df76-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="7df76-109">Тип \_ Усермаршал функция</span><span class="sxs-lookup"><span data-stu-id="7df76-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="7df76-110">Тип \_ Усерунмаршал функция</span><span class="sxs-lookup"><span data-stu-id="7df76-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="7df76-111">Тип \_ Усерфри функция</span><span class="sxs-lookup"><span data-stu-id="7df76-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="7df76-112">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="7df76-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 