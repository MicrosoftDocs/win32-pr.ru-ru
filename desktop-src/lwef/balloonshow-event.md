---
title: Событие Баллуншов
description: Событие Баллуншов
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411214"
---
# <a name="balloonshow-event"></a><span data-ttu-id="ba89a-103">Событие Баллуншов</span><span class="sxs-lookup"><span data-stu-id="ba89a-103">BalloonShow Event</span></span>

<span data-ttu-id="ba89a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ba89a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ba89a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="ba89a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ba89a-106">Происходит при отображении всплывающего окна символа.</span><span class="sxs-lookup"><span data-stu-id="ba89a-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="ba89a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ba89a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ba89a-108"> *Подагент* \_ **баллуншов** **(ByVal** *чарактерид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="ba89a-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="ba89a-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="ba89a-109">Part</span></span>          | <span data-ttu-id="ba89a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ba89a-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="ba89a-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="ba89a-111">*CharacterID*</span></span> | <span data-ttu-id="ba89a-112">Возвращает идентификатор символа, связанного со всплывающей подсказкой.</span><span class="sxs-lookup"><span data-stu-id="ba89a-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="ba89a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba89a-113">Remarks</span></span>

<span data-ttu-id="ba89a-114">Сервер отправляет это событие только клиентам символа (приложения, которые загрузили символ), который использует всплывающую подсказку Word.</span><span class="sxs-lookup"><span data-stu-id="ba89a-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="ba89a-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="ba89a-115">See Also</span></span>

[<span data-ttu-id="ba89a-116">**Событие Баллунхиде**</span><span class="sxs-lookup"><span data-stu-id="ba89a-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




