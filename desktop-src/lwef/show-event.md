---
title: Отобразить событие
description: Отобразить событие
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888007"
---
# <a name="show-event"></a><span data-ttu-id="bc305-103">Отобразить событие</span><span class="sxs-lookup"><span data-stu-id="bc305-103">Show Event</span></span>

<span data-ttu-id="bc305-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc305-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bc305-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="bc305-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bc305-106">Происходит при отображении символа.</span><span class="sxs-lookup"><span data-stu-id="bc305-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="bc305-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bc305-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bc305-108"> *Подагент\ *\ *\ * \_ Показывать (ByVal*\ *  *чарактерид*, **ByVal** , *Причина\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="bc305-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="bc305-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="bc305-109">Part</span></span>          | <span data-ttu-id="bc305-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bc305-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc305-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="bc305-111">*CharacterID*</span></span> | <span data-ttu-id="bc305-112">Возвращает идентификатор символа, показанного в виде строки.</span><span class="sxs-lookup"><span data-stu-id="bc305-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="bc305-113">*Причина*</span><span class="sxs-lookup"><span data-stu-id="bc305-113">*Cause*</span></span>       | <span data-ttu-id="bc305-114">Возвращает значение, указывающее, что привело к отображению символа.</span><span class="sxs-lookup"><span data-stu-id="bc305-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="bc305-115">2 пользователь показал символ (с помощью меню или команды Voice).</span><span class="sxs-lookup"><span data-stu-id="bc305-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="bc305-116">4 клиентское приложение показало этот символ.</span><span class="sxs-lookup"><span data-stu-id="bc305-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="bc305-117">6 другое клиентское приложение показало этот символ.</span><span class="sxs-lookup"><span data-stu-id="bc305-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="bc305-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc305-118">Remarks</span></span>

<span data-ttu-id="bc305-119">Сервер отправляет это событие всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="bc305-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="bc305-120">Чтобы запросить текущее состояние символа, используйте свойство [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="bc305-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="bc305-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="bc305-121">See Also</span></span>

<span data-ttu-id="bc305-122">[**Скрыть событие**](hide-event.md), [ **висибилитикаусе**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="bc305-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





