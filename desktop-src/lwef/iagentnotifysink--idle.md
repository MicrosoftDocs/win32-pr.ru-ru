---
title: Иажентнотифисинк бездействие
description: Иажентнотифисинк бездействие
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700681"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="2f958-103">Иажентнотифисинк:: Idle</span><span class="sxs-lookup"><span data-stu-id="2f958-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="2f958-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f958-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="2f958-105">Уведомляет клиентское приложение, когда изменилось состояние **состояние простояа** символа.</span><span class="sxs-lookup"><span data-stu-id="2f958-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="2f958-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2f958-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="2f958-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="2f958-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="2f958-108">Идентификатор запущенного запроса.</span><span class="sxs-lookup"><span data-stu-id="2f958-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="2f958-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*Откройте*</span><span class="sxs-lookup"><span data-stu-id="2f958-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="2f958-110">Начальный флаг.</span><span class="sxs-lookup"><span data-stu-id="2f958-110">Start flag.</span></span> <span data-ttu-id="2f958-111">Это логическое значение имеет **значение true** , если символ начинается состояние простоя и **false** при остановке состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="2f958-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="2f958-112">Это событие позволяет контролировать, когда сервер Microsoft Agent запускает или останавливает обработку символа в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="2f958-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f958-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="2f958-113">See Also</span></span>

<span data-ttu-id="2f958-114">[**Иажентчарактер:: жетидлеон**](iagentcharacter--getidleon.md), [ **иажентчарактер:: сетидлеон**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="2f958-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 




