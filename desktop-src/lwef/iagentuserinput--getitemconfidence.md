---
title: Иажентусеринпут Жетитемконфиденце
description: Иажентусеринпут Жетитемконфиденце
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328200"
---
# <a name="iagentuserinputgetitemconfidence"></a><span data-ttu-id="eb06f-103">Иажентусеринпут:: Жетитемконфиденце</span><span class="sxs-lookup"><span data-stu-id="eb06f-103">IAgentUserInput::GetItemConfidence</span></span>

<span data-ttu-id="eb06f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb06f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

<span data-ttu-id="eb06f-105">Получает значение достоверности для [**команды**](command-event.md) , передаваемой в обратный вызов [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="eb06f-105">Retrieves the confidence value for a [**Command**](command-event.md) passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="eb06f-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="eb06f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="eb06f-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*двитеминдекс*</span><span class="sxs-lookup"><span data-stu-id="eb06f-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="eb06f-108">Индекс альтернативы [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="eb06f-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="eb06f-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*плконфиденце*</span><span class="sxs-lookup"><span data-stu-id="eb06f-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="eb06f-110">Адрес переменной, получающей оценку достоверности для альтернативы [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="eb06f-110">Address of a variable that receives the confidence score for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="eb06f-111">Если речевой ввод не является источником команды, например, если пользователь выбрал команду во всплывающем меню символа, сервер Microsoft Agent возвращает значение достоверности наилучшего соответствия, равное 100, и значения достоверности для всех остальных альтернатив в виде нуля (0).</span><span class="sxs-lookup"><span data-stu-id="eb06f-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the confidence value of the best match as 100 and the confidence values for all other alternatives as zero (0).</span></span>

## <a name="see-also"></a><span data-ttu-id="eb06f-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="eb06f-112">See Also</span></span>

<span data-ttu-id="eb06f-113">[**Иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md), [**Иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md), [**иажентусеринпут:: жетитемтекст**](iagentuserinput--getitemtext.md)</span><span class="sxs-lookup"><span data-stu-id="eb06f-113">[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)</span></span>


 

 




