---
title: Иажентчарактерекс Жеселпфиленаме
description: Иажентчарактерекс Жеселпфиленаме
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986677"
---
# <a name="iagentcharacterexgethelpfilename"></a><span data-ttu-id="e9f47-103">Иажентчарактерекс:: Жеселпфиленаме</span><span class="sxs-lookup"><span data-stu-id="e9f47-103">IAgentCharacterEx::GetHelpFileName</span></span>

<span data-ttu-id="e9f47-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9f47-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

<span data-ttu-id="e9f47-105">Возвращает Хелпфиленаме для символа.</span><span class="sxs-lookup"><span data-stu-id="e9f47-105">Retrieves the HelpFileName for a character.</span></span>

-   <span data-ttu-id="e9f47-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e9f47-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e9f47-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*пбсзнаме*</span><span class="sxs-lookup"><span data-stu-id="e9f47-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="e9f47-108">Адрес переменной, которая получает имя файла справки для символа.</span><span class="sxs-lookup"><span data-stu-id="e9f47-108">Address of a variable that receives the Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e9f47-109">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** , а пользователь щелкает символ или выбирает команду во всплывающем меню.</span><span class="sxs-lookup"><span data-stu-id="e9f47-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="e9f47-110">Если в свойстве [**хелпконтекстид**](helpcontextid-property.md) выбранной команды имеется контекстный номер, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".</span><span class="sxs-lookup"><span data-stu-id="e9f47-110">If there is a context number in the selected command's [**HelpContextID**](helpcontextid-property.md) property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="e9f47-111">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e9f47-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="e9f47-112">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e9f47-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e9f47-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="e9f47-113">See Also</span></span>

<span data-ttu-id="e9f47-114">[**Иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="e9f47-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




