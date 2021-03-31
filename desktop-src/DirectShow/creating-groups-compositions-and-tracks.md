---
description: Создание групп и композиций
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Создание групп и композиций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895149"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="88c7b-103">Создание групп и композиций</span><span class="sxs-lookup"><span data-stu-id="88c7b-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="88c7b-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="88c7b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="88c7b-105">Группы, композиции и дорожки являются промежуточными слоями между временной шкалой и исходными клипами.</span><span class="sxs-lookup"><span data-stu-id="88c7b-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="88c7b-106">Они различаются по типу объекта, который они могут содержать.</span><span class="sxs-lookup"><span data-stu-id="88c7b-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="88c7b-107">Дорожки содержат объекты источника.</span><span class="sxs-lookup"><span data-stu-id="88c7b-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="88c7b-108">Композиции содержат дорожки и другие композиции, но не исходные объекты.</span><span class="sxs-lookup"><span data-stu-id="88c7b-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="88c7b-109">Группы являются композициями верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="88c7b-109">Groups are top-level compositions.</span></span> <span data-ttu-id="88c7b-110">Группы содержат композиции и композиции, но композиции не могут содержать группы.</span><span class="sxs-lookup"><span data-stu-id="88c7b-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="88c7b-111">*Виртуальная дорожка* — это любой объект, который может находиться внутри композиции или группы.</span><span class="sxs-lookup"><span data-stu-id="88c7b-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="88c7b-112">Это включает в себя отслеживание и композиций.</span><span class="sxs-lookup"><span data-stu-id="88c7b-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="88c7b-113">Эти объекты предоставляют следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="88c7b-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="88c7b-114">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="88c7b-114">Interface</span></span>                                                  | <span data-ttu-id="88c7b-115">Предоставлено</span><span class="sxs-lookup"><span data-stu-id="88c7b-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="88c7b-116">**иамтимелинетракк**</span><span class="sxs-lookup"><span data-stu-id="88c7b-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="88c7b-117">Дорожки</span><span class="sxs-lookup"><span data-stu-id="88c7b-117">Tracks</span></span>               |
| [<span data-ttu-id="88c7b-118">**иамтимелиневиртуалтракк**</span><span class="sxs-lookup"><span data-stu-id="88c7b-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="88c7b-119">Дорожки, композиции</span><span class="sxs-lookup"><span data-stu-id="88c7b-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="88c7b-120">**иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="88c7b-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="88c7b-121">Композиции, группы</span><span class="sxs-lookup"><span data-stu-id="88c7b-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="88c7b-122">**иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="88c7b-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="88c7b-123">Группы</span><span class="sxs-lookup"><span data-stu-id="88c7b-123">Groups</span></span>               |



 

<span data-ttu-id="88c7b-124">Эти интерфейсы содержат методы для добавления объектов на временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="88c7b-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="88c7b-125">[**Иамтимелине:: addgroup**](iamtimeline-addgroup.md): вставляет группу в временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="88c7b-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="88c7b-126">[**Иамтимелинекомп:: втраккинсбефоре**](iamtimelinecomp-vtrackinsbefore.md): вставляет виртуальную запись в композицию или группу.</span><span class="sxs-lookup"><span data-stu-id="88c7b-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="88c7b-127">[**Иамтимелинетракк:: сркадд**](iamtimelinetrack-srcadd.md): вставляет источник в объект Track.</span><span class="sxs-lookup"><span data-stu-id="88c7b-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="88c7b-128">Например, следующий код вставляет новую запись в группу.</span><span class="sxs-lookup"><span data-stu-id="88c7b-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="88c7b-129">Как показано в предыдущей таблице, группа считается композицией, а запись — разновидностью виртуальной записи. Таким образом, чтобы вставить объект Track в группу, необходимо запросить у группы интерфейс **иамтимелинекомп** и вызвать метод **Иамтимелинекомп:: втраккинсбефоре** .</span><span class="sxs-lookup"><span data-stu-id="88c7b-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="88c7b-130">Второй параметр для **втраккинсбефоре** указывает приоритет виртуальной записи. Уровни приоритета начинаются с нуля.</span><span class="sxs-lookup"><span data-stu-id="88c7b-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="88c7b-131">Если указать значение – 1, виртуальная дорожк вставляется в конец списка приоритетов.</span><span class="sxs-lookup"><span data-stu-id="88c7b-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="88c7b-132">Если указать значение, в котором уже есть виртуальная дорожка, все, начиная с этого момента, перемещает вниз по списку на один уровень приоритета.</span><span class="sxs-lookup"><span data-stu-id="88c7b-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="88c7b-133">Не вставляйте виртуальную дорожку с приоритетом больше, чем число виртуальных дорожек, так как это приведет к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="88c7b-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="88c7b-134">Чтобы навсегда удалить объект из временной шкалы, вызовите [**иамтимелинеобж:: RemoveAll**](iamtimelineobj-removeall.md) для объекта.</span><span class="sxs-lookup"><span data-stu-id="88c7b-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="88c7b-135">Этот метод удаляет объект и все его дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="88c7b-135">This method removes the object and all its children.</span></span> <span data-ttu-id="88c7b-136">Чтобы удалить объект с целью его повторного добавления в другое место на временной шкале, вызовите метод [**иамтимелинеобж:: reinsert**](iamtimelineobj-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="88c7b-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="88c7b-137">В отличие от **RemoveAll**, этот метод не удаляет дочерние объекты объекта.</span><span class="sxs-lookup"><span data-stu-id="88c7b-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="88c7b-138">Чтобы удалить все объекты с временной шкалы, вызовите [**иамтимелине:: клеараллграупс**](iamtimeline-clearallgroups.md).</span><span class="sxs-lookup"><span data-stu-id="88c7b-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88c7b-139">См. также</span><span class="sxs-lookup"><span data-stu-id="88c7b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c7b-140">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="88c7b-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



