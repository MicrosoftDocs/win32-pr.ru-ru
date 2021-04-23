---
title: Событие Идлекомплете
description: Событие Идлекомплете
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067235"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="eaa61-103">Событие Идлекомплете</span><span class="sxs-lookup"><span data-stu-id="eaa61-103">IdleComplete Event</span></span>

<span data-ttu-id="eaa61-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eaa61-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eaa61-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="eaa61-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eaa61-106">Происходит, когда сервер завершает состояние **состояние простоя** символа.</span><span class="sxs-lookup"><span data-stu-id="eaa61-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="eaa61-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="eaa61-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eaa61-108"> *Подагент\ *\ *\ * \_ идлекомплете*\ *  **(ByVal** *чарактерид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="eaa61-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="eaa61-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="eaa61-109">Part</span></span>          | <span data-ttu-id="eaa61-110">Описание</span><span class="sxs-lookup"><span data-stu-id="eaa61-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="eaa61-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="eaa61-111">*CharacterID*</span></span> | <span data-ttu-id="eaa61-112">Возвращает идентификатор состояние простоя символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="eaa61-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="eaa61-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eaa61-113">Remarks</span></span>

<span data-ttu-id="eaa61-114">Сервер отправляет это событие всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="eaa61-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="eaa61-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="eaa61-115">See Also</span></span>

[<span data-ttu-id="eaa61-116">**Событие Идлестарт**</span><span class="sxs-lookup"><span data-stu-id="eaa61-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




