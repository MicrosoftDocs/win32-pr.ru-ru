---
title: Иажентнотифисинк Рекуестстарт
description: Иажентнотифисинк Рекуестстарт
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779157"
---
# <a name="iagentnotifysinkrequeststart"></a><span data-ttu-id="b6e15-103">Иажентнотифисинк:: Рекуестстарт</span><span class="sxs-lookup"><span data-stu-id="b6e15-103">IAgentNotifySink::RequestStart</span></span>

<span data-ttu-id="b6e15-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6e15-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

<span data-ttu-id="b6e15-105">Уведомляет клиентское приложение о начале запроса.</span><span class="sxs-lookup"><span data-stu-id="b6e15-105">Notifies a client application when a request begins.</span></span>

-   <span data-ttu-id="b6e15-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b6e15-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b6e15-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*дврекуестид*</span><span class="sxs-lookup"><span data-stu-id="b6e15-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="b6e15-108">Идентификатор запущенного запроса.</span><span class="sxs-lookup"><span data-stu-id="b6e15-108">Identifier of the request that started.</span></span>

</dd> </dl>

<span data-ttu-id="b6e15-109">Это событие позволяет контролировать, когда запрос в очереди начинается с идентификатора запроса.</span><span class="sxs-lookup"><span data-stu-id="b6e15-109">This event enables you to track when a queued request begins using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6e15-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="b6e15-110">See Also</span></span>

<span data-ttu-id="b6e15-111">[**Иажентнотифисинк:: рекуесткомплете**](iagentnotifysink--requestcomplete.md), [**Иажент:: Load**](iagent--load.md), [**иажентчарактер:: Жестуреат**](iagentcharacter--gestureat.md), [**иажентчарактер:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P готовка**](iagentcharacter--prepare.md), [**IAgentCharacter::Pный макет**](iagentcharacter--play.md), [**IAgentCharacter:: Показать**](iagentcharacter--show.md), [**IAgentCharacter:: говорите**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="b6e15-111">[**IAgentNotifySink::RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




