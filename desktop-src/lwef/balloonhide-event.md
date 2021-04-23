---
title: Событие Баллунхиде
description: Событие Баллунхиде
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258940"
---
# <a name="balloonhide-event"></a><span data-ttu-id="01248-103">Событие Баллунхиде</span><span class="sxs-lookup"><span data-stu-id="01248-103">BalloonHide Event</span></span>

<span data-ttu-id="01248-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01248-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="01248-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="01248-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="01248-106">Происходит при скрытии всплывающего окна символа.</span><span class="sxs-lookup"><span data-stu-id="01248-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="01248-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="01248-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="01248-108"> *Подагент* \_ **баллунхиде** **(ByVal** *чарактерид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="01248-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="01248-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="01248-109">Part</span></span>          | <span data-ttu-id="01248-110">Описание</span><span class="sxs-lookup"><span data-stu-id="01248-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="01248-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="01248-111">*CharacterID*</span></span> | <span data-ttu-id="01248-112">Возвращает идентификатор символа, связанного со всплывающей подсказкой.</span><span class="sxs-lookup"><span data-stu-id="01248-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="01248-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01248-113">Remarks</span></span>

<span data-ttu-id="01248-114">Сервер отправляет это событие только клиентам символа (приложения, которые загрузили символ), который использует всплывающую подсказку Word.</span><span class="sxs-lookup"><span data-stu-id="01248-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="01248-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="01248-115">See Also</span></span>

[<span data-ttu-id="01248-116">**Событие Баллуншов**</span><span class="sxs-lookup"><span data-stu-id="01248-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




