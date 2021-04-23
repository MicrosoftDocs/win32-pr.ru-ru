---
description: Получает сведения о выполняющихся приложениях.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Коллекция Аппликатионинстанцес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496125"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="1290d-103">Коллекция Аппликатионинстанцес</span><span class="sxs-lookup"><span data-stu-id="1290d-103">ApplicationInstances collection</span></span>

<span data-ttu-id="1290d-104">Получает сведения о выполняющихся приложениях.</span><span class="sxs-lookup"><span data-stu-id="1290d-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="1290d-105">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1290d-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1290d-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="1290d-106">Members</span></span>

<span data-ttu-id="1290d-107">Коллекция **аппликатионинстанцес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="1290d-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1290d-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="1290d-108">Related Collections</span></span>

<span data-ttu-id="1290d-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="1290d-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1290d-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1290d-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1290d-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1290d-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1290d-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="1290d-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="1290d-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="1290d-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1290d-114">**Приложения**</span><span class="sxs-lookup"><span data-stu-id="1290d-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="1290d-115">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="1290d-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="1290d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="1290d-116">Properties</span></span>

<span data-ttu-id="1290d-117">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="1290d-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1290d-118">Приложение</span><span class="sxs-lookup"><span data-stu-id="1290d-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="1290d-119">хасрециклед</span><span class="sxs-lookup"><span data-stu-id="1290d-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="1290d-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="1290d-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="1290d-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="1290d-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="1290d-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="1290d-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="1290d-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="1290d-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="1290d-124">Приложение</span><span class="sxs-lookup"><span data-stu-id="1290d-124">Application</span></span>



| <span data-ttu-id="1290d-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="1290d-125">Entry</span></span> | <span data-ttu-id="1290d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1290d-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="1290d-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1290d-127">Description</span></span>    | <span data-ttu-id="1290d-128">ИДЕНТИФИКАТОР выполняющегося приложения.</span><span class="sxs-lookup"><span data-stu-id="1290d-128">The ID for the running application.</span></span> |
| <span data-ttu-id="1290d-129">Access</span><span class="sxs-lookup"><span data-stu-id="1290d-129">Access</span></span>         | <span data-ttu-id="1290d-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1290d-130">ReadOnly</span></span>                            |
| <span data-ttu-id="1290d-131">Тип</span><span class="sxs-lookup"><span data-stu-id="1290d-131">Type</span></span>           | <span data-ttu-id="1290d-132">Строка</span><span class="sxs-lookup"><span data-stu-id="1290d-132">String</span></span>                              |
| <span data-ttu-id="1290d-133">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1290d-133">Default</span></span>        | <span data-ttu-id="1290d-134">Н/Д</span><span class="sxs-lookup"><span data-stu-id="1290d-134">N/A</span></span>                                 |
| <span data-ttu-id="1290d-135">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1290d-135">Minimum system</span></span> | <span data-ttu-id="1290d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1290d-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="1290d-137">хасрециклед</span><span class="sxs-lookup"><span data-stu-id="1290d-137">HasRecycled</span></span>



| <span data-ttu-id="1290d-138">Ввод</span><span class="sxs-lookup"><span data-stu-id="1290d-138">Entry</span></span> | <span data-ttu-id="1290d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1290d-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="1290d-140">Описание</span><span class="sxs-lookup"><span data-stu-id="1290d-140">Description</span></span>    | <span data-ttu-id="1290d-141">Указывает, был ли перезапущен экземпляр приложения.</span><span class="sxs-lookup"><span data-stu-id="1290d-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="1290d-142">Access</span><span class="sxs-lookup"><span data-stu-id="1290d-142">Access</span></span>         | <span data-ttu-id="1290d-143">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1290d-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="1290d-144">Тип</span><span class="sxs-lookup"><span data-stu-id="1290d-144">Type</span></span>           | <span data-ttu-id="1290d-145">Bool</span><span class="sxs-lookup"><span data-stu-id="1290d-145">Bool</span></span>                                                          |
| <span data-ttu-id="1290d-146">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1290d-146">Default</span></span>        | <span data-ttu-id="1290d-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="1290d-147">False</span></span>                                                         |
| <span data-ttu-id="1290d-148">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1290d-148">Minimum system</span></span> | <span data-ttu-id="1290d-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1290d-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="1290d-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="1290d-150">InstanceID</span></span>



| <span data-ttu-id="1290d-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="1290d-151">Entry</span></span> | <span data-ttu-id="1290d-152">Значение</span><span class="sxs-lookup"><span data-stu-id="1290d-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1290d-153">Описание</span><span class="sxs-lookup"><span data-stu-id="1290d-153">Description</span></span>    | <span data-ttu-id="1290d-154">Глобальный уникальный идентификатор для экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="1290d-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="1290d-155">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="1290d-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1290d-156">Access</span><span class="sxs-lookup"><span data-stu-id="1290d-156">Access</span></span>         | <span data-ttu-id="1290d-157">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1290d-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="1290d-158">Тип</span><span class="sxs-lookup"><span data-stu-id="1290d-158">Type</span></span>           | <span data-ttu-id="1290d-159">Строка</span><span class="sxs-lookup"><span data-stu-id="1290d-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="1290d-160">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1290d-160">Default</span></span>        | <span data-ttu-id="1290d-161">Н/Д</span><span class="sxs-lookup"><span data-stu-id="1290d-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="1290d-162">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1290d-162">Minimum system</span></span> | <span data-ttu-id="1290d-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1290d-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="1290d-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="1290d-164">IsPaused</span></span>



| <span data-ttu-id="1290d-165">Ввод</span><span class="sxs-lookup"><span data-stu-id="1290d-165">Entry</span></span> | <span data-ttu-id="1290d-166">Значение</span><span class="sxs-lookup"><span data-stu-id="1290d-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="1290d-167">Описание</span><span class="sxs-lookup"><span data-stu-id="1290d-167">Description</span></span>    | <span data-ttu-id="1290d-168">Указывает, приостановлен ли экземпляр приложения в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1290d-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="1290d-169">Access</span><span class="sxs-lookup"><span data-stu-id="1290d-169">Access</span></span>         | <span data-ttu-id="1290d-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1290d-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="1290d-171">Тип</span><span class="sxs-lookup"><span data-stu-id="1290d-171">Type</span></span>           | <span data-ttu-id="1290d-172">Bool</span><span class="sxs-lookup"><span data-stu-id="1290d-172">Bool</span></span>                                                            |
| <span data-ttu-id="1290d-173">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1290d-173">Default</span></span>        | <span data-ttu-id="1290d-174">Неверно</span><span class="sxs-lookup"><span data-stu-id="1290d-174">False</span></span>                                                           |
| <span data-ttu-id="1290d-175">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1290d-175">Minimum system</span></span> | <span data-ttu-id="1290d-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1290d-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="1290d-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="1290d-177">PartitionID</span></span>



| <span data-ttu-id="1290d-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="1290d-178">Entry</span></span> | <span data-ttu-id="1290d-179">Значение</span><span class="sxs-lookup"><span data-stu-id="1290d-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="1290d-180">Описание</span><span class="sxs-lookup"><span data-stu-id="1290d-180">Description</span></span>    | <span data-ttu-id="1290d-181">ИДЕНТИФИКАТОР раздела, который используется приложением.</span><span class="sxs-lookup"><span data-stu-id="1290d-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="1290d-182">Access</span><span class="sxs-lookup"><span data-stu-id="1290d-182">Access</span></span>         | <span data-ttu-id="1290d-183">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1290d-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="1290d-184">Тип</span><span class="sxs-lookup"><span data-stu-id="1290d-184">Type</span></span>           | <span data-ttu-id="1290d-185">Строка</span><span class="sxs-lookup"><span data-stu-id="1290d-185">String</span></span>                                          |
| <span data-ttu-id="1290d-186">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1290d-186">Default</span></span>        | <span data-ttu-id="1290d-187">Н/Д</span><span class="sxs-lookup"><span data-stu-id="1290d-187">N/A</span></span>                                             |
| <span data-ttu-id="1290d-188">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1290d-188">Minimum system</span></span> | <span data-ttu-id="1290d-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1290d-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="1290d-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="1290d-190">ProcessID</span></span>



| <span data-ttu-id="1290d-191">Ввод</span><span class="sxs-lookup"><span data-stu-id="1290d-191">Entry</span></span> | <span data-ttu-id="1290d-192">Значение</span><span class="sxs-lookup"><span data-stu-id="1290d-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="1290d-193">Описание</span><span class="sxs-lookup"><span data-stu-id="1290d-193">Description</span></span>    | <span data-ttu-id="1290d-194">Идентификатор процесса экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="1290d-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="1290d-195">Access</span><span class="sxs-lookup"><span data-stu-id="1290d-195">Access</span></span>         | <span data-ttu-id="1290d-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1290d-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="1290d-197">Тип</span><span class="sxs-lookup"><span data-stu-id="1290d-197">Type</span></span>           | <span data-ttu-id="1290d-198">Строка</span><span class="sxs-lookup"><span data-stu-id="1290d-198">String</span></span>                                      |
| <span data-ttu-id="1290d-199">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1290d-199">Default</span></span>        | <span data-ttu-id="1290d-200">Н/Д</span><span class="sxs-lookup"><span data-stu-id="1290d-200">N/A</span></span>                                         |
| <span data-ttu-id="1290d-201">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1290d-201">Minimum system</span></span> | <span data-ttu-id="1290d-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1290d-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="1290d-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1290d-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1290d-204">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="1290d-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
