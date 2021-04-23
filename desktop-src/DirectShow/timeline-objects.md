---
description: Объекты временной шкалы
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Объекты временной шкалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664697"
---
# <a name="timeline-objects"></a><span data-ttu-id="cd682-103">Объекты временной шкалы</span><span class="sxs-lookup"><span data-stu-id="cd682-103">Timeline Objects</span></span>

<span data-ttu-id="cd682-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="cd682-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="cd682-105">Каждый тип объекта на временной шкале — источник, трассировка, воздействие и т. д. — это отдельный COM-объект.</span><span class="sxs-lookup"><span data-stu-id="cd682-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="cd682-106">Однако приложение не создает их с помощью функции **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="cd682-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="cd682-107">Вместо этого вызывается метод [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="cd682-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="cd682-108">Этот метод создает объект запрошенного типа, инициализирует его и возвращает указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="cd682-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="cd682-109">Дополнительные сведения см. [в разделе Построение временной шкалы](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="cd682-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="cd682-110">Каждый объект временной шкалы предоставляет интерфейс [**иамтимелинеобж**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="cd682-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="cd682-111">Кроме того, различные типы объектов поддерживают собственные специализированные интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="cd682-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="cd682-112">Источник: [ **иамтимелинесрк**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="cd682-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="cd682-113">Track: [ **иамтимелинетракк**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="cd682-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="cd682-114">Композиция: [ **иамтимелинекомп**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="cd682-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="cd682-115">Группа: [**иамтимелинекомп**](iamtimelinecomp.md), [**иамтимелинеграуп**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="cd682-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="cd682-116">Результат: [ **иамтимелиниффект**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="cd682-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="cd682-117">Переход: [ **иамтимелинетранс**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="cd682-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="cd682-118">Обратите внимание, что группы являются типом композиции, поэтому они поддерживают [**иамтимелинекомп**](iamtimelinecomp.md), а также собственный интерфейс [**иамтимелинеграуп**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="cd682-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="cd682-119">В дополнение к перечисленным ранее интерфейсам объекты временной шкалы предоставляют другие дополнительные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="cd682-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="cd682-120">Эти интерфейсы определяют связи между типами объектов.</span><span class="sxs-lookup"><span data-stu-id="cd682-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="cd682-121">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="cd682-121">Interface</span></span>                                                  | <span data-ttu-id="cd682-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cd682-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="cd682-123">Предоставлено</span><span class="sxs-lookup"><span data-stu-id="cd682-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="cd682-124">**иамтимелиневиртуалтракк**</span><span class="sxs-lookup"><span data-stu-id="cd682-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="cd682-125">Объект является виртуальной дорожкой. Виртуальные дорожки могут находиться внутри композиций и хранить другие объекты временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="cd682-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="cd682-126">Композиция, Track</span><span class="sxs-lookup"><span data-stu-id="cd682-126">Composition, Track</span></span>                |
| [<span data-ttu-id="cd682-127">**иамтимелиниффектабле**</span><span class="sxs-lookup"><span data-stu-id="cd682-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="cd682-128">Объект может иметь эффекты.</span><span class="sxs-lookup"><span data-stu-id="cd682-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="cd682-129">Композиция, трассировка, источник</span><span class="sxs-lookup"><span data-stu-id="cd682-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="cd682-130">**иамтимелинетрансабле**</span><span class="sxs-lookup"><span data-stu-id="cd682-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="cd682-131">Объект может иметь переходы.</span><span class="sxs-lookup"><span data-stu-id="cd682-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="cd682-132">Композиция, Track</span><span class="sxs-lookup"><span data-stu-id="cd682-132">Composition, Track</span></span>                |
| [<span data-ttu-id="cd682-133">**иамтимелинесплиттабле**</span><span class="sxs-lookup"><span data-stu-id="cd682-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="cd682-134">Объект можно разделить на два объекта.</span><span class="sxs-lookup"><span data-stu-id="cd682-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="cd682-135">Трассировка, источник, воздействие, переход</span><span class="sxs-lookup"><span data-stu-id="cd682-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cd682-136">См. также</span><span class="sxs-lookup"><span data-stu-id="cd682-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd682-137">Общие сведения о компонентах временной шкалы</span><span class="sxs-lookup"><span data-stu-id="cd682-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



