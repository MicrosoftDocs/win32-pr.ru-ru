---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411204"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="66999-103">Иажентчарактер:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="66999-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="66999-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="66999-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="66999-105">Останавливает указанную анимацию (запрос) и удаляет ее из очереди анимации символа.</span><span class="sxs-lookup"><span data-stu-id="66999-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="66999-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="66999-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66999-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*дврекид*</span><span class="sxs-lookup"><span data-stu-id="66999-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="66999-108">Идентификатор останавливаемого запроса.</span><span class="sxs-lookup"><span data-stu-id="66999-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="66999-109">**Остановить** также можно использовать для остановки [**всех вызовов,**](iagentcharacter--prepare.md) помещенных в очередь.</span><span class="sxs-lookup"><span data-stu-id="66999-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="66999-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="66999-110">See Also</span></span>

<span data-ttu-id="66999-111">[**Иажентчарактер::P готовка**](iagentcharacter--prepare.md), [ **иажентчарактер:: стопалл**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="66999-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




