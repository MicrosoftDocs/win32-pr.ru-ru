---
title: Иаженткоммандсекс Сеселпконтекстид
description: Иаженткоммандсекс Сеселпконтекстид
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790591"
---
# <a name="iagentcommandsexsethelpcontextid"></a><span data-ttu-id="38993-103">Иаженткоммандсекс:: Сеселпконтекстид</span><span class="sxs-lookup"><span data-stu-id="38993-103">IAgentCommandsEx::SetHelpContextID</span></span>

<span data-ttu-id="38993-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38993-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="38993-105">Задает [**хелпконтекстид**](helpcontextid-property.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="38993-105">Sets the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="38993-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="38993-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="38993-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*улхелпид*</span><span class="sxs-lookup"><span data-stu-id="38993-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="38993-108">Контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) ; используется для предоставления контекстной справки для команды.</span><span class="sxs-lookup"><span data-stu-id="38993-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="38993-109">Если вы создали файл справки Windows для своего приложения и установили его в свойстве [**HelpFile**](helpfile-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="38993-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="38993-110">Агент автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду.</span><span class="sxs-lookup"><span data-stu-id="38993-110">Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="38993-111">Если в [**хелпконтекстид**](helpcontextid-property.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="38993-111">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="38993-112">Текущий контекстный номер — это значение **хелпконтекстид** для команды.</span><span class="sxs-lookup"><span data-stu-id="38993-112">The current context number is the value of **HelpContextID** for the command.</span></span> <span data-ttu-id="38993-113">Если в свойстве **хелпконтекстид** выбранной команды имеется контекстный номер, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".</span><span class="sxs-lookup"><span data-stu-id="38993-113">If there is a context number in the selected command's **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="38993-114">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="38993-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="38993-115">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="38993-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="38993-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="38993-116">See Also</span></span>

<span data-ttu-id="38993-117">[**Иаженткоммандсекс:: жеселпконтекстид**](iagentcommandsex--gethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="38993-117">[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 