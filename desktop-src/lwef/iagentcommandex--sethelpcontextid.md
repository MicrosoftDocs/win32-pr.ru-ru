---
title: Иаженткоммандекс Сеселпконтекстид
description: Иаженткоммандекс Сеселпконтекстид
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691508"
---
# <a name="iagentcommandexsethelpcontextid"></a><span data-ttu-id="a5a95-103">Иаженткоммандекс:: Сеселпконтекстид</span><span class="sxs-lookup"><span data-stu-id="a5a95-103">IAgentCommandEx::SetHelpContextID</span></span>

<span data-ttu-id="a5a95-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a5a95-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

<span data-ttu-id="a5a95-105">Задает [**хелпконтекстид**](helpcontextid-property-com.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="a5a95-105">Sets the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="a5a95-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a5a95-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a5a95-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*улид*</span><span class="sxs-lookup"><span data-stu-id="a5a95-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span></span>
</dt> <dd>

<span data-ttu-id="a5a95-108">Контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) ; используется для предоставления контекстной справки для команды.</span><span class="sxs-lookup"><span data-stu-id="a5a95-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="a5a95-109">Если вы создали файл справки Windows для своего приложения и установили его в свойстве [**HelpFile**](helpfile-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="a5a95-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="a5a95-110">Microsoft Agent автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду.</span><span class="sxs-lookup"><span data-stu-id="a5a95-110">Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="a5a95-111">Если в [**хелпконтекстид**](helpcontextid-property-com.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="a5a95-111">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="a5a95-112">Текущий контекстный номер — это значение **хелпконтекстид** для команды.</span><span class="sxs-lookup"><span data-stu-id="a5a95-112">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="a5a95-113">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a5a95-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a5a95-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="a5a95-114">See Also</span></span>

<span data-ttu-id="a5a95-115">[**Иаженткоммандекс:: жеселпконтекстид**](iagentcommandex--gethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="a5a95-115">[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 