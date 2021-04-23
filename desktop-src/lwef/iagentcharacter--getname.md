---
title: Иажентчарактер имя
description: Иажентчарактер имя
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332763"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="7fa03-103">Иажентчарактер:: Name</span><span class="sxs-lookup"><span data-stu-id="7fa03-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="7fa03-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fa03-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="7fa03-105">Возвращает имя символа.</span><span class="sxs-lookup"><span data-stu-id="7fa03-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="7fa03-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7fa03-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7fa03-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*пбсзнаме*</span><span class="sxs-lookup"><span data-stu-id="7fa03-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="7fa03-108">Адрес объекта BSTR, который получает значение имени для символа.</span><span class="sxs-lookup"><span data-stu-id="7fa03-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="7fa03-109">Имя символа по умолчанию определяется при компиляции с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7fa03-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="7fa03-110">Имя символа может отличаться в зависимости от идентификатора языка символа.</span><span class="sxs-lookup"><span data-stu-id="7fa03-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="7fa03-111">Символы могут быть скомпилированы с разными именами для разных языков.</span><span class="sxs-lookup"><span data-stu-id="7fa03-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="7fa03-112">Можно также задать имя символа с помощью **иажентчарактер: SetName**; Однако имена всех текущих клиентов символа изменяются.</span><span class="sxs-lookup"><span data-stu-id="7fa03-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fa03-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="7fa03-113">See Also</span></span>

[<span data-ttu-id="7fa03-114">**Иажентчарактер:: SetName**</span><span class="sxs-lookup"><span data-stu-id="7fa03-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 




