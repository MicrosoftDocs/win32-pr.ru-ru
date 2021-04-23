---
title: Иажентчарактерекс Сеселпфиленаме
description: Иажентчарактерекс Сеселпфиленаме
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132943"
---
# <a name="iagentcharacterexsethelpfilename"></a><span data-ttu-id="9406f-103">Иажентчарактерекс:: Сеселпфиленаме</span><span class="sxs-lookup"><span data-stu-id="9406f-103">IAgentCharacterEx::SetHelpFileName</span></span>

<span data-ttu-id="9406f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9406f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

<span data-ttu-id="9406f-105">Задает Хелпфиленаме для символа.</span><span class="sxs-lookup"><span data-stu-id="9406f-105">Sets the HelpFileName for a character.</span></span>

-   <span data-ttu-id="9406f-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9406f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9406f-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*бсзнаме*</span><span class="sxs-lookup"><span data-stu-id="9406f-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="9406f-108">Имя файла справки для символа.</span><span class="sxs-lookup"><span data-stu-id="9406f-108">The Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="9406f-109">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** , а пользователь щелкает символ или выбирает команду во всплывающем меню.</span><span class="sxs-lookup"><span data-stu-id="9406f-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="9406f-110">Если в свойстве [**хелпконтекстид**](helpcontextid-property.md) выбранной команды имеется контекстный номер, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".</span><span class="sxs-lookup"><span data-stu-id="9406f-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="9406f-111">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="9406f-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="9406f-112">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9406f-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="9406f-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="9406f-113">See Also</span></span>

<span data-ttu-id="9406f-114">[**Иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="9406f-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span></span>


 

 




