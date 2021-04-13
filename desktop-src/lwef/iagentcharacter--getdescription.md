---
title: Иажентчарактер, описание
description: Иажентчарактер, описание
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411455"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="07fc4-103">Иажентчарактер::, описание</span><span class="sxs-lookup"><span data-stu-id="07fc4-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="07fc4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07fc4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="07fc4-105">Извлекает описание символа.</span><span class="sxs-lookup"><span data-stu-id="07fc4-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="07fc4-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="07fc4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="07fc4-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*пбсздескриптион*</span><span class="sxs-lookup"><span data-stu-id="07fc4-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="07fc4-108">Адрес объекта BSTR, который получает значение описания символа.</span><span class="sxs-lookup"><span data-stu-id="07fc4-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="07fc4-109">Описание символа определяется при его компиляции с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="07fc4-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="07fc4-110">Параметр description является необязательным и не может быть указан для всех символов.</span><span class="sxs-lookup"><span data-stu-id="07fc4-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 




