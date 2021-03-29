---
title: Формат пары идентификатор/смещение
description: Вторая часть потока набора свойств содержит одну пару идентификаторов и смещений формата.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329539"
---
# <a name="format-identifieroffset-pair"></a><span data-ttu-id="cbaf3-103">Формат пары идентификатор/смещение</span><span class="sxs-lookup"><span data-stu-id="cbaf3-103">Format Identifier/Offset Pair</span></span>

<span data-ttu-id="cbaf3-104">Вторая часть потока набора свойств содержит одну пару идентификаторов и смещений формата.</span><span class="sxs-lookup"><span data-stu-id="cbaf3-104">The second part of the property set stream contains one Format Identifier/Offset Pair.</span></span> <span data-ttu-id="cbaf3-105">FMTID — это имя набора свойств; Он однозначно определяет способ интерпретации содержимого следующего раздела.</span><span class="sxs-lookup"><span data-stu-id="cbaf3-105">The FMTID is the name of the property set; it uniquely identifies how to interpret the contents of the following section.</span></span> <span data-ttu-id="cbaf3-106">Смещение — это расстояние в байтах от начала всего потока до начала раздела.</span><span class="sxs-lookup"><span data-stu-id="cbaf3-106">The Offset is the distance, in bytes, from the start of the whole stream to where the section begins.</span></span>

<span data-ttu-id="cbaf3-107">Следующая структура полезна при обработке пар идентификаторов и смещений формата.</span><span class="sxs-lookup"><span data-stu-id="cbaf3-107">The following structure is helpful in handling Format Identifier/Offset Pairs.</span></span>

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




