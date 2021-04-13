---
title: Иаженткоммандекс Жеселпконтекстид
description: Иаженткоммандекс Жеселпконтекстид
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412939"
---
# <a name="iagentcommandexgethelpcontextid"></a><span data-ttu-id="1eae7-103">Иаженткоммандекс:: Жеселпконтекстид</span><span class="sxs-lookup"><span data-stu-id="1eae7-103">IAgentCommandEx::GetHelpContextID</span></span>

<span data-ttu-id="1eae7-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1eae7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

<span data-ttu-id="1eae7-105">Получает [**хелпконтекстид**](helpcontextid-property-com.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="1eae7-105">Retrieves the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="1eae7-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1eae7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1eae7-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*пулид*</span><span class="sxs-lookup"><span data-stu-id="1eae7-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span></span>
</dt> <dd>

<span data-ttu-id="1eae7-108">Адрес переменной, которая получает контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="1eae7-108">Address of a variable that receives the context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="1eae7-109">Если вы создали файл справки Windows для приложения и устанавливаете для свойства [**HelpFile**](helpfile-property.md) символа этот файл, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду.</span><span class="sxs-lookup"><span data-stu-id="1eae7-109">If you've created a Windows Help file for your application and set your character's [**HelpFile**](helpfile-property.md) property to this file, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="1eae7-110">Если в [**хелпконтекстид**](helpcontextid-property-com.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="1eae7-110">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="1eae7-111">Текущий контекстный номер — это значение **хелпконтекстид** для команды.</span><span class="sxs-lookup"><span data-stu-id="1eae7-111">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="1eae7-112">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1eae7-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="1eae7-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="1eae7-113">See Also</span></span>

<span data-ttu-id="1eae7-114">[**Иаженткоммандекс:: сеселпконтекстид**](iagentcommandex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="1eae7-114">[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 