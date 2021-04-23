---
title: Иажентусеринпут Жетитемтекст
description: Иажентусеринпут Жетитемтекст
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067236"
---
# <a name="iagentuserinputgetitemtext"></a><span data-ttu-id="e1a53-103">Иажентусеринпут:: Жетитемтекст</span><span class="sxs-lookup"><span data-stu-id="e1a53-103">IAgentUserInput::GetItemText</span></span>

<span data-ttu-id="e1a53-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1a53-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

<span data-ttu-id="e1a53-105">Получает текст голоса для альтернативной [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="e1a53-105">Retrieves the voice text for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="e1a53-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e1a53-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e1a53-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*двитеминдекс*</span><span class="sxs-lookup"><span data-stu-id="e1a53-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="e1a53-108">Индекс альтернативы [**команды**](command-event.md) , передаваемой обратному вызову [**Иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="e1a53-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="e1a53-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*пбсзтекст*</span><span class="sxs-lookup"><span data-stu-id="e1a53-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="e1a53-110">Адрес строки BSTR, которая получает значение текста голоса для [**команды**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="e1a53-110">Address of a BSTR that receives the value of the voice text for the [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="e1a53-111">Если речевой ввод не является источником команды, например, если пользователь выбрал команду во всплывающем меню символа, сервер возвращает **значение NULL** для текста голоса [**команды**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="e1a53-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the server returns **NULL** for the [**Command**](command-event.md)'s voice text.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1a53-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="e1a53-112">See Also</span></span>

<span data-ttu-id="e1a53-113">[**Иажентусеринпут:: жетитемконфиденце**](iagentuserinput--getitemconfidence.md), [**Иажентусеринпут:: жетитемид**](iagentuserinput--getitemid.md), [**иажентусеринпут:: жеталлитемдата**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="e1a53-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




