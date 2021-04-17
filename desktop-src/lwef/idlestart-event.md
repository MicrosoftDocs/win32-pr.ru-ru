---
title: Событие Идлестарт
description: Событие Идлестарт
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710081"
---
# <a name="idlestart-event"></a><span data-ttu-id="8f874-103">Событие Идлестарт</span><span class="sxs-lookup"><span data-stu-id="8f874-103">IdleStart Event</span></span>

<span data-ttu-id="8f874-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f874-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8f874-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="8f874-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8f874-106">Происходит, когда сервер устанавливает символ в состояние **состояние простоя** .</span><span class="sxs-lookup"><span data-stu-id="8f874-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="8f874-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8f874-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8f874-108"> *Подагент\ *\ *\ * \_ идлестарт*\ *  **(ByVal** *чарактерид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="8f874-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="8f874-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="8f874-109">Part</span></span>          | <span data-ttu-id="8f874-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8f874-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="8f874-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="8f874-111">*CharacterID*</span></span> | <span data-ttu-id="8f874-112">Возвращает идентификатор состояние простоя символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="8f874-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8f874-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f874-113">Remarks</span></span>

<span data-ttu-id="8f874-114">Сервер отправляет это событие всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="8f874-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="8f874-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="8f874-115">See Also</span></span>

[<span data-ttu-id="8f874-116">**Событие Идлекомплете**</span><span class="sxs-lookup"><span data-stu-id="8f874-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




