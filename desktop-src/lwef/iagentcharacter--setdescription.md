---
title: Иажентчарактер SetDescription
description: Иажентчарактер SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411447"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="fb6e2-103">Иажентчарактер:: SetDescription</span><span class="sxs-lookup"><span data-stu-id="fb6e2-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="fb6e2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb6e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="fb6e2-105">Задает описание символа.</span><span class="sxs-lookup"><span data-stu-id="fb6e2-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="fb6e2-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fb6e2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fb6e2-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*бсздескриптион*</span><span class="sxs-lookup"><span data-stu-id="fb6e2-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="fb6e2-108">Значение типа BSTR, которое задает описание символа.</span><span class="sxs-lookup"><span data-stu-id="fb6e2-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="fb6e2-109">Описание символа по умолчанию определяется при его компиляции с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fb6e2-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fb6e2-110">Параметр description является необязательным и не может быть указан для всех символов.</span><span class="sxs-lookup"><span data-stu-id="fb6e2-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="fb6e2-111">Описание символа можно изменить с помощью **иажентчарактер:: setDescription**; Однако это значение не является постоянным (постоянно хранится).</span><span class="sxs-lookup"><span data-stu-id="fb6e2-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="fb6e2-112">Описание символа возвращается к значению по умолчанию при первой загрузке символа клиентом.</span><span class="sxs-lookup"><span data-stu-id="fb6e2-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fb6e2-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="fb6e2-113">See Also</span></span>

[<span data-ttu-id="fb6e2-114">**Иажентчарактер::, описание**</span><span class="sxs-lookup"><span data-stu-id="fb6e2-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 




