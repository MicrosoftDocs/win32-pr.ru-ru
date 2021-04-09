---
title: Атрибуты transmit_as и represent_as
description: В этом разделе обсуждается реализация преобразования типов данных программистов с помощью языка MIDL \ передать \_ как \ и \ представить \_ как \ атрибуты.
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890753"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="bc486-103">Атрибуты «передать \_ как» и «представить \_ как»</span><span class="sxs-lookup"><span data-stu-id="bc486-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="bc486-104">В этом разделе обсуждается реализация преобразования типов данных программиста с помощью MIDL " **\[** [**передать \_ как**](/windows/desktop/Midl/transmit-as) " **\]** и " **\[** [**представить \_ как**](/windows/desktop/Midl/represent-as) " **\]** .</span><span class="sxs-lookup"><span data-stu-id="bc486-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="bc486-105">Обсуждение представлено в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bc486-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="bc486-106">Атрибут **передачи \_ as**</span><span class="sxs-lookup"><span data-stu-id="bc486-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="bc486-107">**Тип \_ для функции \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="bc486-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="bc486-108">**Тип \_ из функции \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="bc486-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="bc486-109">Функция **типа \_ Free \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="bc486-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="bc486-110">Функция **типа \_ Free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="bc486-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="bc486-111">Атрибут **представления \_ как**</span><span class="sxs-lookup"><span data-stu-id="bc486-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="bc486-112">**Именованный \_ тип \_ из \_ локальной** функции</span><span class="sxs-lookup"><span data-stu-id="bc486-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="bc486-113">**Именованный \_ тип \_ для \_ локальной** функции</span><span class="sxs-lookup"><span data-stu-id="bc486-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="bc486-114">**\_ \_ \_ Локальная функция с именованным типом Free**</span><span class="sxs-lookup"><span data-stu-id="bc486-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="bc486-115">Функция **с именованным \_ типом \_ Free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="bc486-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 