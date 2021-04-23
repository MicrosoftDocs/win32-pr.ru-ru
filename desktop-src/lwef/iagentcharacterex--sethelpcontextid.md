---
title: Иажентчарактерекс Сеселпконтекстид
description: Иажентчарактерекс Сеселпконтекстид
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774498"
---
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="e7e71-103">Иажентчарактерекс:: Сеселпконтекстид</span><span class="sxs-lookup"><span data-stu-id="e7e71-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="e7e71-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7e71-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="e7e71-105">Задает [**хелпконтекстид**](helpcontextid-property.md) для символа.</span><span class="sxs-lookup"><span data-stu-id="e7e71-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="e7e71-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e7e71-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e7e71-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*улхелпид*</span><span class="sxs-lookup"><span data-stu-id="e7e71-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="e7e71-108">Контекстный номер раздела справки, связанного с символом; используется для предоставления контекстной справки для символа.</span><span class="sxs-lookup"><span data-stu-id="e7e71-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e7e71-109">Если вы создали файл справки Windows для приложения и установили его в свойстве [**HelpFile**](helpfile-property.md) символа, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает символ.</span><span class="sxs-lookup"><span data-stu-id="e7e71-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="e7e71-110">Если в [**хелпконтекстид**](helpcontextid-property.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="e7e71-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e7e71-111">Текущий контекстный номер — это значение **хелпконтекстид** для символа.</span><span class="sxs-lookup"><span data-stu-id="e7e71-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="e7e71-112">Если в свойстве **хелпконтекстид** имеется контекстный номер, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".</span><span class="sxs-lookup"><span data-stu-id="e7e71-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="e7e71-113">Этот параметр применяется только в том случае, если клиентское приложение является активным клиентом самого верхнего символа.</span><span class="sxs-lookup"><span data-stu-id="e7e71-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="e7e71-114">Он не влияет на других клиентов символов или других символов, которые использует клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="e7e71-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="e7e71-115">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e7e71-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e7e71-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="e7e71-116">See Also</span></span>

<span data-ttu-id="e7e71-117">[**Иажентчарактерекс:: жеселпконтекстид**](iagentcharacterex--gethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="e7e71-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




