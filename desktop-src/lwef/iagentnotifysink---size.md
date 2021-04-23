---
title: Размер Иажентнотифисинк
description: Размер Иажентнотифисинк
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532291"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="87c9a-103">Иажентнотифисинк:: size</span><span class="sxs-lookup"><span data-stu-id="87c9a-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="87c9a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="87c9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="87c9a-105">Уведомляет клиентское приложение об изменении размера символа.</span><span class="sxs-lookup"><span data-stu-id="87c9a-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="87c9a-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="87c9a-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="87c9a-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="87c9a-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="87c9a-108">Идентификатор символа, размер которого был изменен.</span><span class="sxs-lookup"><span data-stu-id="87c9a-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="87c9a-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*лвидс*</span><span class="sxs-lookup"><span data-stu-id="87c9a-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="87c9a-110">Ширина кадра анимации символа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="87c9a-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="87c9a-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*лхеигхт*</span><span class="sxs-lookup"><span data-stu-id="87c9a-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="87c9a-112">Высота кадра анимации символа (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="87c9a-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="87c9a-113">Это событие отправляется всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="87c9a-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="87c9a-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="87c9a-114">See Also</span></span>

<span data-ttu-id="87c9a-115">[**Иажентчарактер:: DataSize**](iagentcharacter--getsize.md), [ **иажентчарактер:: SetSize**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="87c9a-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




