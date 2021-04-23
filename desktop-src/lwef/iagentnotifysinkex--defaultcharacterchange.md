---
title: Иажентнотифисинкекс Дефаултчарактерчанже
description: Иажентнотифисинкекс Дефаултчарактерчанже
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700611"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="f4de7-103">Иажентнотифисинкекс::D Ефаултчарактерчанже</span><span class="sxs-lookup"><span data-stu-id="f4de7-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="f4de7-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f4de7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="f4de7-105">Уведомляет клиентское приложение об изменении символа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4de7-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="f4de7-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f4de7-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="f4de7-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*бсзгуид*</span><span class="sxs-lookup"><span data-stu-id="f4de7-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="f4de7-108">Уникальный идентификатор для символа.</span><span class="sxs-lookup"><span data-stu-id="f4de7-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="f4de7-109">Когда пользователь изменяет символ, назначенный в качестве символа по умолчанию для пользователя, сервер отправляет это событие клиентам, которые загрузили символ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4de7-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="f4de7-110">Событие возвращает уникальный идентификатор (GUID) символа, отформатированный с помощью фигурных скобок и дефисов, который определяется при построении символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f4de7-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="f4de7-111">Когда появляется новый символ, он предполагает тот же размер, что и любой уже загруженный экземпляр символа или предыдущий символ по умолчанию (в указанном порядке).</span><span class="sxs-lookup"><span data-stu-id="f4de7-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="f4de7-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="f4de7-112">See Also</span></span>

[<span data-ttu-id="f4de7-113">**Иажент:: Load**</span><span class="sxs-lookup"><span data-stu-id="f4de7-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




