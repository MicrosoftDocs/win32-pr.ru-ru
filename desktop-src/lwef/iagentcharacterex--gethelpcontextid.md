---
title: Иажентчарактерекс Жеселпконтекстид
description: Иажентчарактерекс Жеселпконтекстид
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778716"
---
# <a name="iagentcharacterexgethelpcontextid"></a><span data-ttu-id="e305d-103">Иажентчарактерекс:: Жеселпконтекстид</span><span class="sxs-lookup"><span data-stu-id="e305d-103">IAgentCharacterEx::GetHelpContextID</span></span>

<span data-ttu-id="e305d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e305d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

<span data-ttu-id="e305d-105">Возвращает [**хелпконтекстид**](helpcontextid-property.md) для символа.</span><span class="sxs-lookup"><span data-stu-id="e305d-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="e305d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e305d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e305d-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*пулхелпид*</span><span class="sxs-lookup"><span data-stu-id="e305d-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="e305d-108">Адрес переменной, которая получает контекстный номер раздела справки для символа.</span><span class="sxs-lookup"><span data-stu-id="e305d-108">Address of a variable that receives the context number of the help topic for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e305d-109">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает символ.</span><span class="sxs-lookup"><span data-stu-id="e305d-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="e305d-110">Если в [**хелпконтекстид**](helpcontextid-property.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="e305d-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e305d-111">Текущий контекстный номер — это значение **хелпконтекстид** для символа.</span><span class="sxs-lookup"><span data-stu-id="e305d-111">The current context number is the value of **HelpContextID** for the character.</span></span>

<span data-ttu-id="e305d-112">**Иажентчарактерекс:: жеселпконтекстид** возвращает [**хелпконтекстид**](helpcontextid-property.md) , заданное для символа.</span><span class="sxs-lookup"><span data-stu-id="e305d-112">**IAgentCharacterEx::GetHelpContextID** returns the [**HelpContextID**](helpcontextid-property.md) you set for the character.</span></span> <span data-ttu-id="e305d-113">Он не возвращает **хелпконтекстид** , заданный другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="e305d-113">It does not return the **HelpContextID** set by other clients.</span></span>

> [!Note]  
> <span data-ttu-id="e305d-114">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e305d-114">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e305d-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="e305d-115">See Also</span></span>

<span data-ttu-id="e305d-116">[**Иажентчарактерекс:: сеселпконтекстид**](iagentcharacterex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="e305d-116">[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




