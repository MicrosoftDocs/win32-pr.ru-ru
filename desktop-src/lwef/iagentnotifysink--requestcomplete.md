---
title: Иажентнотифисинк Рекуесткомплете
description: Иажентнотифисинк Рекуесткомплете
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332000"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="fdcf2-103">Иажентнотифисинк:: Рекуесткомплете</span><span class="sxs-lookup"><span data-stu-id="fdcf2-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="fdcf2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fdcf2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="fdcf2-105">Уведомляет клиентское приложение о завершении запроса.</span><span class="sxs-lookup"><span data-stu-id="fdcf2-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="fdcf2-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fdcf2-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="fdcf2-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*дврекуестид*</span><span class="sxs-lookup"><span data-stu-id="fdcf2-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="fdcf2-108">Идентификатор запущенного запроса.</span><span class="sxs-lookup"><span data-stu-id="fdcf2-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="fdcf2-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*хрстатус*</span><span class="sxs-lookup"><span data-stu-id="fdcf2-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="fdcf2-110">Код состояния.</span><span class="sxs-lookup"><span data-stu-id="fdcf2-110">Status code.</span></span> <span data-ttu-id="fdcf2-111">Этот параметр возвращает код состояния для запроса.</span><span class="sxs-lookup"><span data-stu-id="fdcf2-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="fdcf2-112">Это событие позволяет отслеживанию завершения метода, поставленного в очередь, с помощью идентификатора запроса.</span><span class="sxs-lookup"><span data-stu-id="fdcf2-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdcf2-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="fdcf2-113">See Also</span></span>

<span data-ttu-id="fdcf2-114">[**Иажентнотифисинк:: рекуестстарт**](iagentnotifysink--requeststart.md), [**Иажент:: Load**](iagent--load.md), [**иажентчарактер:: Жестуреат**](iagentcharacter--gestureat.md), [**иажентчарактер:: Hide**](iagentcharacter--hide.md), [**иажентчарактер:: Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P готовка**](iagentcharacter--prepare.md), [**IAgentCharacter::Pный макет**](iagentcharacter--play.md), [**IAgentCharacter:: Показать**](iagentcharacter--show.md), [**IAgentCharacter:: говорите**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="fdcf2-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




