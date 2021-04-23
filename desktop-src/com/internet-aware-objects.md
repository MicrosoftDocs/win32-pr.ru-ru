---
title: Internet-Aware объекты
description: Internet-Aware объекты
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987930"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="1fb90-103">Internet-Aware объекты</span><span class="sxs-lookup"><span data-stu-id="1fb90-103">Internet-Aware Objects</span></span>

<span data-ttu-id="1fb90-104">Для покрытия интерфейсов сохраняемости определены определенные категории. они были определены в результате определения того, как элементы управления работают через Интернет.</span><span class="sxs-lookup"><span data-stu-id="1fb90-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="1fb90-105">Контейнер, который не поддерживает полный диапазон интерфейсов сохраняемости, должен обеспечить отсутствие элемента управления, который требует сочетания интерфейсов, которые он не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="1fb90-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="1fb90-106">В следующих таблицах описывается значение для различных категорий как для реализованных, так и для обязательных категорий.</span><span class="sxs-lookup"><span data-stu-id="1fb90-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="1fb90-107">Обязательные категории</span><span class="sxs-lookup"><span data-stu-id="1fb90-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="1fb90-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1fb90-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb90-109">CATID \_ персистстомоникер, CATID \_ ПЕРСИСТСТОСТРЕАМИНИТ, CATID \_ персиситстостреам, CATID \_ персистстостораже, CATID \_ ПЕРСИСТСТОМЕМОРИ, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1fb90-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="1fb90-110">Каждая из этих категорий является взаимоисключающей и используется только в том случае, если объект поддерживает только один механизм сохраняемости (следовательно, взаимное исключение).</span><span class="sxs-lookup"><span data-stu-id="1fb90-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="1fb90-111">Контейнеры, которые не поддерживают механизм сохраняемости, описанный в одной из этих категорий, должны помешать самим создавать объекты классов, помеченные как.</span><span class="sxs-lookup"><span data-stu-id="1fb90-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="1fb90-112">CATID \_ рекуиресдатапасхост</span><span class="sxs-lookup"><span data-stu-id="1fb90-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="1fb90-113">Объект требует возможность сохранения данных в один или несколько путей и требует вовлечения в контейнер, поэтому требуется поддержка контейнеров для [**ибиндхост**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1fb90-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="1fb90-114">Реализованные категории</span><span class="sxs-lookup"><span data-stu-id="1fb90-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="1fb90-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1fb90-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb90-116">CATID \_ персистстомоникер, CATID \_ ПЕРСИСТСТОСТРЕАМИНИТ, CATID \_ персистстостреам, CATID \_ персистстостораже, CATID \_ ПЕРСИСТСТОМЕМОРИ, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1fb90-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="1fb90-117">Объект поддерживает соответствующий механизм IPersist \* для категории.</span><span class="sxs-lookup"><span data-stu-id="1fb90-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="1fb90-118">В следующей таблице представлены точные CATID, назначенные каждой категории.</span><span class="sxs-lookup"><span data-stu-id="1fb90-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="1fb90-119">Категория</span><span class="sxs-lookup"><span data-stu-id="1fb90-119">Category</span></span>                                | <span data-ttu-id="1fb90-120">CATID</span><span class="sxs-lookup"><span data-stu-id="1fb90-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="1fb90-121">CATID \_ рекуиресдатапасхост</span><span class="sxs-lookup"><span data-stu-id="1fb90-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="1fb90-122">0de86a50-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-123">CATID \_ персистстомоникер</span><span class="sxs-lookup"><span data-stu-id="1fb90-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="1fb90-124">0de86a51-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-125">CATID \_ персистстостораже</span><span class="sxs-lookup"><span data-stu-id="1fb90-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="1fb90-126">0de86a52-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-127">CATID \_ персистстостреаминит</span><span class="sxs-lookup"><span data-stu-id="1fb90-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="1fb90-128">0de86a53-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-129">CATID \_ персистстостреам</span><span class="sxs-lookup"><span data-stu-id="1fb90-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="1fb90-130">0de86a54-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-131">CATID \_ персистстомемори</span><span class="sxs-lookup"><span data-stu-id="1fb90-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="1fb90-132">0de86a55-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-133">CATID \_ персистстофиле</span><span class="sxs-lookup"><span data-stu-id="1fb90-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="1fb90-134">0de86a56-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="1fb90-135">CATID \_ персистстопропертибаг</span><span class="sxs-lookup"><span data-stu-id="1fb90-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="1fb90-136">0de86a57-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="1fb90-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1fb90-137">См. также</span><span class="sxs-lookup"><span data-stu-id="1fb90-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fb90-138">Категории компонентов</span><span class="sxs-lookup"><span data-stu-id="1fb90-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

