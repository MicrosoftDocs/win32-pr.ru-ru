---
title: Иажентчарактер SetName
description: Иажентчарактер SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710173"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="7f9a0-103">Иажентчарактер:: SetName</span><span class="sxs-lookup"><span data-stu-id="7f9a0-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="7f9a0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7f9a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="7f9a0-105">Задает имя символа.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="7f9a0-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7f9a0-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*бсзнаме*</span><span class="sxs-lookup"><span data-stu-id="7f9a0-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="7f9a0-108">Значение типа BSTR, задающее имя символа.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="7f9a0-109">Имя символа по умолчанию определяется при компиляции с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="7f9a0-110">Его можно изменить с помощью **иажентчарактер:: SetName**; Однако это изменяет имя символа для всех текущих клиентов символа.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="7f9a0-111">Это свойство не является постоянным (хранится без возможности восстановления).</span><span class="sxs-lookup"><span data-stu-id="7f9a0-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="7f9a0-112">Имя символа возвращается к имени по умолчанию при первой загрузке символа клиентом.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="7f9a0-113">Имя символа может также зависеть от идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="7f9a0-114">Символы могут быть скомпилированы с разными именами для разных языков.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="7f9a0-115">Сервер использует параметр имени символа в частях интерфейса Microsoft Agent, например, заголовок окна «Voice Commands», если символ является входным и находится во всплывающем меню Microsoft Agent панели задач.</span><span class="sxs-lookup"><span data-stu-id="7f9a0-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7f9a0-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="7f9a0-116">See Also</span></span>

[<span data-ttu-id="7f9a0-117">**Иажентчарактер:: Name**</span><span class="sxs-lookup"><span data-stu-id="7f9a0-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 




