---
title: Иажентусеринпут Жетитемид
description: Иажентусеринпут Жетитемид
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700467"
---
# <a name="iagentuserinputgetitemid"></a><span data-ttu-id="41857-103">Иажентусеринпут:: Жетитемид</span><span class="sxs-lookup"><span data-stu-id="41857-103">IAgentUserInput::GetItemID</span></span>

<span data-ttu-id="41857-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41857-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="41857-105">Получает идентификатор альтернативной [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="41857-105">Retrieves the identifier of a [**Command**](command-event.md) alternative passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="41857-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="41857-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="41857-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*двитеминдекс*</span><span class="sxs-lookup"><span data-stu-id="41857-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="41857-108">Индекс альтернативы [**команды**](command-event.md) , переданной в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="41857-108">The index of the [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="41857-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*пдвкоммандид*</span><span class="sxs-lookup"><span data-stu-id="41857-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="41857-110">Адрес переменной, которая получает идентификатор [**команды**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="41857-110">Address of a variable that receives the ID of a [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="41857-111">Если голосовое входное значение активирует обратный вызов [**иажентнотифисинк:: Command**](iagentnotifysink--command.md) , сервер возвращает идентификаторы для всех совпадающих [**команд**](command-event.md) , определенных приложением.</span><span class="sxs-lookup"><span data-stu-id="41857-111">If voice input triggers the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback, the server returns the IDs for any matching [**Commands**](command-event.md) defined by your application.</span></span>

## <a name="see-also"></a><span data-ttu-id="41857-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="41857-112">See Also</span></span>

<span data-ttu-id="41857-113">[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемтекст**](iagentuserinput--getitemtext.md), [**иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="41857-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




