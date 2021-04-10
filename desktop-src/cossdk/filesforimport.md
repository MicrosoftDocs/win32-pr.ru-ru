---
description: Извлекает сведения о импортированных приложениях.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Коллекция Филесфоримпорт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141992"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="fe495-103">Коллекция Филесфоримпорт</span><span class="sxs-lookup"><span data-stu-id="fe495-103">FilesForImport collection</span></span>

<span data-ttu-id="fe495-104">Извлекает сведения о импортированных приложениях.</span><span class="sxs-lookup"><span data-stu-id="fe495-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="fe495-105">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fe495-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fe495-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="fe495-106">Members</span></span>

<span data-ttu-id="fe495-107">Коллекция **филесфоримпорт** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="fe495-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fe495-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="fe495-108">Related Collections</span></span>

<span data-ttu-id="fe495-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="fe495-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fe495-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fe495-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fe495-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fe495-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fe495-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="fe495-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="fe495-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="fe495-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fe495-114">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="fe495-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="fe495-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe495-115">Properties</span></span>

<span data-ttu-id="fe495-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="fe495-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fe495-117">аппликатионфиленаме</span><span class="sxs-lookup"><span data-stu-id="fe495-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="fe495-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fe495-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="fe495-119">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="fe495-120">FileName</span><span class="sxs-lookup"><span data-stu-id="fe495-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="fe495-121">хасусерс</span><span class="sxs-lookup"><span data-stu-id="fe495-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="fe495-122">IsProxy</span><span class="sxs-lookup"><span data-stu-id="fe495-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="fe495-123">Служба</span><span class="sxs-lookup"><span data-stu-id="fe495-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="fe495-124">партитиондескриптион</span><span class="sxs-lookup"><span data-stu-id="fe495-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="fe495-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="fe495-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="fe495-126">Имя раздела</span><span class="sxs-lookup"><span data-stu-id="fe495-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="fe495-127">аппликатионфиленаме</span><span class="sxs-lookup"><span data-stu-id="fe495-127">ApplicationFileName</span></span>



| <span data-ttu-id="fe495-128">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-128">Entry</span></span> | <span data-ttu-id="fe495-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fe495-130">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-130">Description</span></span>    | <span data-ttu-id="fe495-131">Имя MSI файла, содержащего приложение, которое можно импортировать.</span><span class="sxs-lookup"><span data-stu-id="fe495-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="fe495-132">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-132">Access</span></span>         | <span data-ttu-id="fe495-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="fe495-134">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-134">Type</span></span>           | <span data-ttu-id="fe495-135">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-135">String</span></span>                                                                       |
| <span data-ttu-id="fe495-136">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-136">Default</span></span>        | <span data-ttu-id="fe495-137">Н/Д</span><span class="sxs-lookup"><span data-stu-id="fe495-137">N/A</span></span>                                                                          |
| <span data-ttu-id="fe495-138">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-138">Minimum system</span></span> | <span data-ttu-id="fe495-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="fe495-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fe495-140">ApplicationName</span></span>



| <span data-ttu-id="fe495-141">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-141">Entry</span></span> | <span data-ttu-id="fe495-142">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="fe495-143">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-143">Description</span></span>    | <span data-ttu-id="fe495-144">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="fe495-144">The name of the application.</span></span> |
| <span data-ttu-id="fe495-145">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-145">Access</span></span>         | <span data-ttu-id="fe495-146">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-146">ReadOnly</span></span>                     |
| <span data-ttu-id="fe495-147">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-147">Type</span></span>           | <span data-ttu-id="fe495-148">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-148">String</span></span>                       |
| <span data-ttu-id="fe495-149">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-149">Default</span></span>        | <span data-ttu-id="fe495-150">""</span><span class="sxs-lookup"><span data-stu-id="fe495-150">""</span></span>                           |
| <span data-ttu-id="fe495-151">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-151">Minimum system</span></span> | <span data-ttu-id="fe495-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="fe495-153">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-153">Description</span></span>



| <span data-ttu-id="fe495-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-154">Entry</span></span> | <span data-ttu-id="fe495-155">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="fe495-156">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-156">Description</span></span>    | <span data-ttu-id="fe495-157">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="fe495-157">A description of the application.</span></span> |
| <span data-ttu-id="fe495-158">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-158">Access</span></span>         | <span data-ttu-id="fe495-159">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-159">ReadOnly</span></span>                          |
| <span data-ttu-id="fe495-160">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-160">Type</span></span>           | <span data-ttu-id="fe495-161">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-161">String</span></span>                            |
| <span data-ttu-id="fe495-162">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-162">Default</span></span>        | <span data-ttu-id="fe495-163">""</span><span class="sxs-lookup"><span data-stu-id="fe495-163">""</span></span>                                |
| <span data-ttu-id="fe495-164">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-164">Minimum system</span></span> | <span data-ttu-id="fe495-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="fe495-166">FileName</span><span class="sxs-lookup"><span data-stu-id="fe495-166">FileName</span></span>



| <span data-ttu-id="fe495-167">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-167">Entry</span></span> | <span data-ttu-id="fe495-168">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe495-169">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-169">Description</span></span>    | <span data-ttu-id="fe495-170">Имя файла DLL или EXE, содержащего приложение.</span><span class="sxs-lookup"><span data-stu-id="fe495-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="fe495-171">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="fe495-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fe495-172">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-172">Access</span></span>         | <span data-ttu-id="fe495-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="fe495-174">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-174">Type</span></span>           | <span data-ttu-id="fe495-175">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="fe495-176">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-176">Default</span></span>        | <span data-ttu-id="fe495-177">""</span><span class="sxs-lookup"><span data-stu-id="fe495-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="fe495-178">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-178">Minimum system</span></span> | <span data-ttu-id="fe495-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="fe495-180">хасусерс</span><span class="sxs-lookup"><span data-stu-id="fe495-180">HasUsers</span></span>



| <span data-ttu-id="fe495-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-181">Entry</span></span> | <span data-ttu-id="fe495-182">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="fe495-183">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-183">Description</span></span>    | <span data-ttu-id="fe495-184">Указывает, есть ли у приложения пользователи.</span><span class="sxs-lookup"><span data-stu-id="fe495-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="fe495-185">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-185">Access</span></span>         | <span data-ttu-id="fe495-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="fe495-187">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-187">Type</span></span>           | <span data-ttu-id="fe495-188">Bool</span><span class="sxs-lookup"><span data-stu-id="fe495-188">Bool</span></span>                                             |
| <span data-ttu-id="fe495-189">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-189">Default</span></span>        | <span data-ttu-id="fe495-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="fe495-190">False</span></span>                                            |
| <span data-ttu-id="fe495-191">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-191">Minimum system</span></span> | <span data-ttu-id="fe495-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="fe495-193">IsProxy</span><span class="sxs-lookup"><span data-stu-id="fe495-193">IsProxy</span></span>



| <span data-ttu-id="fe495-194">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-194">Entry</span></span> | <span data-ttu-id="fe495-195">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="fe495-196">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-196">Description</span></span>    | <span data-ttu-id="fe495-197">Указывает, является ли приложение прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="fe495-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="fe495-198">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-198">Access</span></span>         | <span data-ttu-id="fe495-199">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="fe495-200">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-200">Type</span></span>           | <span data-ttu-id="fe495-201">Bool</span><span class="sxs-lookup"><span data-stu-id="fe495-201">Bool</span></span>                                          |
| <span data-ttu-id="fe495-202">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-202">Default</span></span>        | <span data-ttu-id="fe495-203">Неверно</span><span class="sxs-lookup"><span data-stu-id="fe495-203">False</span></span>                                         |
| <span data-ttu-id="fe495-204">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-204">Minimum system</span></span> | <span data-ttu-id="fe495-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="fe495-206">Служба</span><span class="sxs-lookup"><span data-stu-id="fe495-206">IsService</span></span>



| <span data-ttu-id="fe495-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-207">Entry</span></span> | <span data-ttu-id="fe495-208">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="fe495-209">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-209">Description</span></span>    | <span data-ttu-id="fe495-210">Указывает, является ли приложение службой.</span><span class="sxs-lookup"><span data-stu-id="fe495-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="fe495-211">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-211">Access</span></span>         | <span data-ttu-id="fe495-212">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="fe495-213">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-213">Type</span></span>           | <span data-ttu-id="fe495-214">Bool</span><span class="sxs-lookup"><span data-stu-id="fe495-214">Bool</span></span>                                            |
| <span data-ttu-id="fe495-215">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-215">Default</span></span>        | <span data-ttu-id="fe495-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="fe495-216">False</span></span>                                           |
| <span data-ttu-id="fe495-217">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-217">Minimum system</span></span> | <span data-ttu-id="fe495-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe495-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="fe495-219">партитиондескриптион</span><span class="sxs-lookup"><span data-stu-id="fe495-219">PartitionDescription</span></span>



| <span data-ttu-id="fe495-220">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-220">Entry</span></span> | <span data-ttu-id="fe495-221">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="fe495-222">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-222">Description</span></span>    | <span data-ttu-id="fe495-223">Описание раздела приложения.</span><span class="sxs-lookup"><span data-stu-id="fe495-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="fe495-224">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-224">Access</span></span>         | <span data-ttu-id="fe495-225">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="fe495-226">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-226">Type</span></span>           | <span data-ttu-id="fe495-227">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-227">String</span></span>                                        |
| <span data-ttu-id="fe495-228">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-228">Default</span></span>        | <span data-ttu-id="fe495-229">""</span><span class="sxs-lookup"><span data-stu-id="fe495-229">""</span></span>                                            |
| <span data-ttu-id="fe495-230">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-230">Minimum system</span></span> | <span data-ttu-id="fe495-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe495-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="fe495-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="fe495-232">PartitionID</span></span>



| <span data-ttu-id="fe495-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-233">Entry</span></span> | <span data-ttu-id="fe495-234">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="fe495-235">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-235">Description</span></span>    | <span data-ttu-id="fe495-236">Идентификатор GUID раздела приложения.</span><span class="sxs-lookup"><span data-stu-id="fe495-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="fe495-237">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-237">Access</span></span>         | <span data-ttu-id="fe495-238">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="fe495-239">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-239">Type</span></span>           | <span data-ttu-id="fe495-240">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-240">String</span></span>                                   |
| <span data-ttu-id="fe495-241">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-241">Default</span></span>        | <span data-ttu-id="fe495-242">""</span><span class="sxs-lookup"><span data-stu-id="fe495-242">""</span></span>                                       |
| <span data-ttu-id="fe495-243">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-243">Minimum system</span></span> | <span data-ttu-id="fe495-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe495-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="fe495-245">Имя раздела</span><span class="sxs-lookup"><span data-stu-id="fe495-245">PartitionName</span></span>



| <span data-ttu-id="fe495-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="fe495-246">Entry</span></span> | <span data-ttu-id="fe495-247">Значение</span><span class="sxs-lookup"><span data-stu-id="fe495-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="fe495-248">Описание</span><span class="sxs-lookup"><span data-stu-id="fe495-248">Description</span></span>    | <span data-ttu-id="fe495-249">Имя раздела приложения.</span><span class="sxs-lookup"><span data-stu-id="fe495-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="fe495-250">Access</span><span class="sxs-lookup"><span data-stu-id="fe495-250">Access</span></span>         | <span data-ttu-id="fe495-251">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fe495-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="fe495-252">Тип</span><span class="sxs-lookup"><span data-stu-id="fe495-252">Type</span></span>           | <span data-ttu-id="fe495-253">Строка</span><span class="sxs-lookup"><span data-stu-id="fe495-253">String</span></span>                                   |
| <span data-ttu-id="fe495-254">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="fe495-254">Default</span></span>        | <span data-ttu-id="fe495-255">""</span><span class="sxs-lookup"><span data-stu-id="fe495-255">""</span></span>                                       |
| <span data-ttu-id="fe495-256">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="fe495-256">Minimum system</span></span> | <span data-ttu-id="fe495-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe495-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="fe495-258">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe495-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe495-259">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="fe495-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
