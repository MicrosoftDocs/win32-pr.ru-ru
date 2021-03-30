---
description: Содержит объект для каждой временной подписки. Временные подписки можно создавать на лету для запуска экземпляров объектов, и они исчезают при уничтожении объекта.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Коллекция Трансиентсубскриптионс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896053"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="da667-104">Коллекция Трансиентсубскриптионс</span><span class="sxs-lookup"><span data-stu-id="da667-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="da667-105">Содержит объект для каждой временной подписки.</span><span class="sxs-lookup"><span data-stu-id="da667-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="da667-106">Временные подписки можно создавать на лету для запуска экземпляров объектов, и они исчезают при уничтожении объекта.</span><span class="sxs-lookup"><span data-stu-id="da667-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="da667-107">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="da667-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="da667-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="da667-108">Members</span></span>

<span data-ttu-id="da667-109">Коллекция **трансиентсубскриптионс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="da667-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="da667-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="da667-110">Related Collections</span></span>

<span data-ttu-id="da667-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="da667-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="da667-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="da667-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="da667-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="da667-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="da667-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="da667-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="da667-115">**трансиентпублишерпропертиес**</span><span class="sxs-lookup"><span data-stu-id="da667-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="da667-116">**трансиентсубскриберпропертиес**</span><span class="sxs-lookup"><span data-stu-id="da667-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="da667-117">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="da667-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="da667-118">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="da667-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="da667-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="da667-119">Properties</span></span>

<span data-ttu-id="da667-120">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="da667-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="da667-121">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-121">Description</span></span>](#description)
-   [<span data-ttu-id="da667-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="da667-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="da667-123">евенткласспартитионид</span><span class="sxs-lookup"><span data-stu-id="da667-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="da667-124">евентклсид</span><span class="sxs-lookup"><span data-stu-id="da667-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="da667-125">Параметром filterCriteria</span><span class="sxs-lookup"><span data-stu-id="da667-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="da667-126">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="da667-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="da667-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="da667-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="da667-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="da667-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="da667-129">Name</span><span class="sxs-lookup"><span data-stu-id="da667-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="da667-130">Изучение</span><span class="sxs-lookup"><span data-stu-id="da667-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="da667-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="da667-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="da667-132">субскриберинтерфаце</span><span class="sxs-lookup"><span data-stu-id="da667-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="da667-133">субскриберпартитионид</span><span class="sxs-lookup"><span data-stu-id="da667-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="da667-134">UserName</span><span class="sxs-lookup"><span data-stu-id="da667-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="da667-135">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-135">Description</span></span>



| <span data-ttu-id="da667-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-136">Entry</span></span> | <span data-ttu-id="da667-137">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="da667-138">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-138">Description</span></span>    | <span data-ttu-id="da667-139">Описание подписки.</span><span class="sxs-lookup"><span data-stu-id="da667-139">A description for the subscription.</span></span> |
| <span data-ttu-id="da667-140">Access</span><span class="sxs-lookup"><span data-stu-id="da667-140">Access</span></span>         | <span data-ttu-id="da667-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-141">ReadWrite</span></span>                           |
| <span data-ttu-id="da667-142">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-142">Type</span></span>           | <span data-ttu-id="da667-143">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-143">String</span></span>                              |
| <span data-ttu-id="da667-144">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-144">Default</span></span>        | <span data-ttu-id="da667-145">""</span><span class="sxs-lookup"><span data-stu-id="da667-145">""</span></span>                                  |
| <span data-ttu-id="da667-146">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-146">Minimum system</span></span> | <span data-ttu-id="da667-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="da667-148">Активировано</span><span class="sxs-lookup"><span data-stu-id="da667-148">Enabled</span></span>



| <span data-ttu-id="da667-149">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-149">Entry</span></span> | <span data-ttu-id="da667-150">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="da667-151">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-151">Description</span></span>    | <span data-ttu-id="da667-152">Указывает, включена ли подписка в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="da667-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="da667-153">Access</span><span class="sxs-lookup"><span data-stu-id="da667-153">Access</span></span>         | <span data-ttu-id="da667-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="da667-155">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-155">Type</span></span>           | <span data-ttu-id="da667-156">Bool</span><span class="sxs-lookup"><span data-stu-id="da667-156">Bool</span></span>                                                     |
| <span data-ttu-id="da667-157">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-157">Default</span></span>        | <span data-ttu-id="da667-158">True</span><span class="sxs-lookup"><span data-stu-id="da667-158">True</span></span>                                                     |
| <span data-ttu-id="da667-159">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-159">Minimum system</span></span> | <span data-ttu-id="da667-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="da667-161">евенткласспартитионид</span><span class="sxs-lookup"><span data-stu-id="da667-161">EventClassPartitionID</span></span>



| <span data-ttu-id="da667-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-162">Entry</span></span> | <span data-ttu-id="da667-163">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-164">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-164">Description</span></span>    | <span data-ttu-id="da667-165">При подписке на класс событий используется для представления идентификатора GUID идентификатора секции, содержащего класс событий.</span><span class="sxs-lookup"><span data-stu-id="da667-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="da667-166">При подписке на классы событий подписчик имеет возможность подписаться на класс событий в той же или другой секции.</span><span class="sxs-lookup"><span data-stu-id="da667-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="da667-167">Access</span><span class="sxs-lookup"><span data-stu-id="da667-167">Access</span></span>         | <span data-ttu-id="da667-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="da667-169">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-169">Type</span></span>           | <span data-ttu-id="da667-170">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="da667-171">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-171">Default</span></span>        | <span data-ttu-id="da667-172">NULL</span><span class="sxs-lookup"><span data-stu-id="da667-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="da667-173">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-173">Minimum system</span></span> | <span data-ttu-id="da667-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da667-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="da667-175">евентклсид</span><span class="sxs-lookup"><span data-stu-id="da667-175">EventCLSID</span></span>



| <span data-ttu-id="da667-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-176">Entry</span></span> | <span data-ttu-id="da667-177">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-178">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-178">Description</span></span>    | <span data-ttu-id="da667-179">Идентификатор CLSID для класса событий.</span><span class="sxs-lookup"><span data-stu-id="da667-179">The CLSID for the event class.</span></span> <span data-ttu-id="da667-180">Можно указать Евентклсид или PublisherID, но не оба.</span><span class="sxs-lookup"><span data-stu-id="da667-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="da667-181">Access</span><span class="sxs-lookup"><span data-stu-id="da667-181">Access</span></span>         | <span data-ttu-id="da667-182">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="da667-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="da667-183">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-183">Type</span></span>           | <span data-ttu-id="da667-184">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-184">String</span></span>                                                                                       |
| <span data-ttu-id="da667-185">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-185">Default</span></span>        | <span data-ttu-id="da667-186">Н/Д</span><span class="sxs-lookup"><span data-stu-id="da667-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="da667-187">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-187">Minimum system</span></span> | <span data-ttu-id="da667-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="da667-189">Параметром filterCriteria</span><span class="sxs-lookup"><span data-stu-id="da667-189">FilterCriteria</span></span>



| <span data-ttu-id="da667-190">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-190">Entry</span></span> | <span data-ttu-id="da667-191">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-192">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-192">Description</span></span>    | <span data-ttu-id="da667-193">Строка, указывающая условия фильтра.</span><span class="sxs-lookup"><span data-stu-id="da667-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="da667-194">Может быть идентификатором CLSID для класса [**публишерфилтер**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="da667-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="da667-195">Access</span><span class="sxs-lookup"><span data-stu-id="da667-195">Access</span></span>         | <span data-ttu-id="da667-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="da667-197">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-197">Type</span></span>           | <span data-ttu-id="da667-198">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-198">String</span></span>                                                                                                               |
| <span data-ttu-id="da667-199">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-199">Default</span></span>        | <span data-ttu-id="da667-200">Н/Д</span><span class="sxs-lookup"><span data-stu-id="da667-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="da667-201">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-201">Minimum system</span></span> | <span data-ttu-id="da667-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="da667-203">ID</span><span class="sxs-lookup"><span data-stu-id="da667-203">ID</span></span>



| <span data-ttu-id="da667-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-204">Entry</span></span> | <span data-ttu-id="da667-205">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-206">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-206">Description</span></span>    | <span data-ttu-id="da667-207">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="da667-207">Identifier for the subscription.</span></span> <span data-ttu-id="da667-208">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="da667-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="da667-209">Access</span><span class="sxs-lookup"><span data-stu-id="da667-209">Access</span></span>         | <span data-ttu-id="da667-210">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="da667-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="da667-211">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-211">Type</span></span>           | <span data-ttu-id="da667-212">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="da667-213">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="da667-214">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-214">Minimum system</span></span> | <span data-ttu-id="da667-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="da667-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="da667-216">InterfaceID</span></span>



| <span data-ttu-id="da667-217">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-217">Entry</span></span> | <span data-ttu-id="da667-218">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="da667-219">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-219">Description</span></span>    | <span data-ttu-id="da667-220">IID для интерфейса, на который оформлена подписка.</span><span class="sxs-lookup"><span data-stu-id="da667-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="da667-221">Access</span><span class="sxs-lookup"><span data-stu-id="da667-221">Access</span></span>         | <span data-ttu-id="da667-222">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="da667-222">WriteOnce</span></span>                        |
| <span data-ttu-id="da667-223">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-223">Type</span></span>           | <span data-ttu-id="da667-224">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-224">String</span></span>                           |
| <span data-ttu-id="da667-225">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-225">Default</span></span>        | <span data-ttu-id="da667-226">Н/Д</span><span class="sxs-lookup"><span data-stu-id="da667-226">N/A</span></span>                              |
| <span data-ttu-id="da667-227">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-227">Minimum system</span></span> | <span data-ttu-id="da667-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="da667-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="da667-229">MethodName</span></span>



| <span data-ttu-id="da667-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-230">Entry</span></span> | <span data-ttu-id="da667-231">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="da667-232">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-232">Description</span></span>    | <span data-ttu-id="da667-233">Метод для интерфейса, на который оформлена подписка.</span><span class="sxs-lookup"><span data-stu-id="da667-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="da667-234">Access</span><span class="sxs-lookup"><span data-stu-id="da667-234">Access</span></span>         | <span data-ttu-id="da667-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="da667-236">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-236">Type</span></span>           | <span data-ttu-id="da667-237">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-237">String</span></span>                                       |
| <span data-ttu-id="da667-238">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-238">Default</span></span>        | <span data-ttu-id="da667-239">Н/Д</span><span class="sxs-lookup"><span data-stu-id="da667-239">N/A</span></span>                                          |
| <span data-ttu-id="da667-240">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-240">Minimum system</span></span> | <span data-ttu-id="da667-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="da667-242">Имя</span><span class="sxs-lookup"><span data-stu-id="da667-242">Name</span></span>



| <span data-ttu-id="da667-243">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-243">Entry</span></span> | <span data-ttu-id="da667-244">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-245">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-245">Description</span></span>    | <span data-ttu-id="da667-246">Имя подписки.</span><span class="sxs-lookup"><span data-stu-id="da667-246">The name for the subscription.</span></span> <span data-ttu-id="da667-247">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="da667-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="da667-248">Access</span><span class="sxs-lookup"><span data-stu-id="da667-248">Access</span></span>         | <span data-ttu-id="da667-249">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="da667-250">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-250">Type</span></span>           | <span data-ttu-id="da667-251">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="da667-252">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-252">Default</span></span>        | <span data-ttu-id="da667-253">"Создать подписку"</span><span class="sxs-lookup"><span data-stu-id="da667-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="da667-254">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-254">Minimum system</span></span> | <span data-ttu-id="da667-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="da667-256">Изучение</span><span class="sxs-lookup"><span data-stu-id="da667-256">PerUser</span></span>



| <span data-ttu-id="da667-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-257">Entry</span></span> | <span data-ttu-id="da667-258">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-259">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-259">Description</span></span>    | <span data-ttu-id="da667-260">Указывает, применяется ли подписка только для данного пользователя, представленного свойством UserName.</span><span class="sxs-lookup"><span data-stu-id="da667-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="da667-261">Access</span><span class="sxs-lookup"><span data-stu-id="da667-261">Access</span></span>         | <span data-ttu-id="da667-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="da667-263">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-263">Type</span></span>           | <span data-ttu-id="da667-264">Bool</span><span class="sxs-lookup"><span data-stu-id="da667-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="da667-265">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-265">Default</span></span>        | <span data-ttu-id="da667-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="da667-266">False</span></span>                                                                                                   |
| <span data-ttu-id="da667-267">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-267">Minimum system</span></span> | <span data-ttu-id="da667-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="da667-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="da667-269">PublisherID</span></span>



| <span data-ttu-id="da667-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-270">Entry</span></span> | <span data-ttu-id="da667-271">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-272">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-272">Description</span></span>    | <span data-ttu-id="da667-273">Идентификатор издателя.</span><span class="sxs-lookup"><span data-stu-id="da667-273">ID for the publisher.</span></span> <span data-ttu-id="da667-274">Можно указать Евентклсид или PublisherID, но не оба.</span><span class="sxs-lookup"><span data-stu-id="da667-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="da667-275">Access</span><span class="sxs-lookup"><span data-stu-id="da667-275">Access</span></span>         | <span data-ttu-id="da667-276">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="da667-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="da667-277">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-277">Type</span></span>           | <span data-ttu-id="da667-278">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-278">String</span></span>                                                                              |
| <span data-ttu-id="da667-279">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-279">Default</span></span>        | <span data-ttu-id="da667-280">""</span><span class="sxs-lookup"><span data-stu-id="da667-280">""</span></span>                                                                                  |
| <span data-ttu-id="da667-281">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-281">Minimum system</span></span> | <span data-ttu-id="da667-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="da667-283">субскриберинтерфаце</span><span class="sxs-lookup"><span data-stu-id="da667-283">SubscriberInterface</span></span>



| <span data-ttu-id="da667-284">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-284">Entry</span></span> | <span data-ttu-id="da667-285">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="da667-286">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-286">Description</span></span>    | <span data-ttu-id="da667-287">Указатель на интерфейс подписчика.</span><span class="sxs-lookup"><span data-stu-id="da667-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="da667-288">Access</span><span class="sxs-lookup"><span data-stu-id="da667-288">Access</span></span>         | <span data-ttu-id="da667-289">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-289">ReadWrite</span></span>                                |
| <span data-ttu-id="da667-290">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-290">Type</span></span>           | <span data-ttu-id="da667-291">Variant</span><span class="sxs-lookup"><span data-stu-id="da667-291">Variant</span></span>                                  |
| <span data-ttu-id="da667-292">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-292">Default</span></span>        | <span data-ttu-id="da667-293">Н/Д</span><span class="sxs-lookup"><span data-stu-id="da667-293">N/A</span></span>                                      |
| <span data-ttu-id="da667-294">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-294">Minimum system</span></span> | <span data-ttu-id="da667-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="da667-296">субскриберпартитионид</span><span class="sxs-lookup"><span data-stu-id="da667-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="da667-297">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-297">Entry</span></span> | <span data-ttu-id="da667-298">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da667-299">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-299">Description</span></span>    | <span data-ttu-id="da667-300">При подписке на класс событий в той же секции используется для представления идентификатора GUID идентификатора секции подписчика.</span><span class="sxs-lookup"><span data-stu-id="da667-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="da667-301">При подписке на классы событий подписчик имеет возможность подписаться на класс событий в той же или другой секции.</span><span class="sxs-lookup"><span data-stu-id="da667-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="da667-302">Access</span><span class="sxs-lookup"><span data-stu-id="da667-302">Access</span></span>         | <span data-ttu-id="da667-303">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="da667-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="da667-304">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-304">Type</span></span>           | <span data-ttu-id="da667-305">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="da667-306">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="da667-307">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-307">Minimum system</span></span> | <span data-ttu-id="da667-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da667-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="da667-309">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="da667-309">UserName</span></span>



| <span data-ttu-id="da667-310">Ввод</span><span class="sxs-lookup"><span data-stu-id="da667-310">Entry</span></span> | <span data-ttu-id="da667-311">Значение</span><span class="sxs-lookup"><span data-stu-id="da667-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="da667-312">Описание</span><span class="sxs-lookup"><span data-stu-id="da667-312">Description</span></span>    | <span data-ttu-id="da667-313">Имя пользователя, к которому применяется подписка, если для параметра «изучение» задано значение true.</span><span class="sxs-lookup"><span data-stu-id="da667-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="da667-314">Access</span><span class="sxs-lookup"><span data-stu-id="da667-314">Access</span></span>         | <span data-ttu-id="da667-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da667-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="da667-316">Тип</span><span class="sxs-lookup"><span data-stu-id="da667-316">Type</span></span>           | <span data-ttu-id="da667-317">Строка</span><span class="sxs-lookup"><span data-stu-id="da667-317">String</span></span>                                                                  |
| <span data-ttu-id="da667-318">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="da667-318">Default</span></span>        | <span data-ttu-id="da667-319">Н/Д</span><span class="sxs-lookup"><span data-stu-id="da667-319">N/A</span></span>                                                                     |
| <span data-ttu-id="da667-320">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="da667-320">Minimum system</span></span> | <span data-ttu-id="da667-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="da667-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="da667-322">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da667-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da667-323">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="da667-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
