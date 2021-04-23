---
description: Содержит объект для каждого интерфейса, предоставляемого компонентом, к которому относится коллекция.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Коллекция Интерфацесфоркомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141815"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="a67f9-103">Коллекция Интерфацесфоркомпонент</span><span class="sxs-lookup"><span data-stu-id="a67f9-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="a67f9-104">Содержит объект для каждого интерфейса, предоставляемого компонентом, к которому относится коллекция.</span><span class="sxs-lookup"><span data-stu-id="a67f9-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="a67f9-105">Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a67f9-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a67f9-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="a67f9-106">Members</span></span>

<span data-ttu-id="a67f9-107">Коллекция **интерфацесфоркомпонент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="a67f9-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a67f9-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="a67f9-108">Related Collections</span></span>

<span data-ttu-id="a67f9-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="a67f9-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a67f9-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a67f9-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a67f9-111">**месодсфоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="a67f9-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="a67f9-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a67f9-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a67f9-113">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="a67f9-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="a67f9-114">**ролесфоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="a67f9-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="a67f9-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="a67f9-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a67f9-116">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="a67f9-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="a67f9-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="a67f9-117">Properties</span></span>

<span data-ttu-id="a67f9-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="a67f9-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a67f9-119">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="a67f9-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="a67f9-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-120">Description</span></span>](#description)
-   [<span data-ttu-id="a67f9-121">IID</span><span class="sxs-lookup"><span data-stu-id="a67f9-121">IID</span></span>](#iid)
-   [<span data-ttu-id="a67f9-122">Name</span><span class="sxs-lookup"><span data-stu-id="a67f9-122">Name</span></span>](#name)
-   [<span data-ttu-id="a67f9-123">куеуинженаблед</span><span class="sxs-lookup"><span data-stu-id="a67f9-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="a67f9-124">куеуеингсуппортед</span><span class="sxs-lookup"><span data-stu-id="a67f9-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="a67f9-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="a67f9-125">CLSID</span></span>



| <span data-ttu-id="a67f9-126">Ввод</span><span class="sxs-lookup"><span data-stu-id="a67f9-126">Entry</span></span> | <span data-ttu-id="a67f9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a67f9-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="a67f9-128">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-128">Description</span></span>    | <span data-ttu-id="a67f9-129">Идентификатор GUID для компонента.</span><span class="sxs-lookup"><span data-stu-id="a67f9-129">A GUID for the component.</span></span> |
| <span data-ttu-id="a67f9-130">Access</span><span class="sxs-lookup"><span data-stu-id="a67f9-130">Access</span></span>         | <span data-ttu-id="a67f9-131">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a67f9-131">ReadOnly</span></span>                  |
| <span data-ttu-id="a67f9-132">Тип</span><span class="sxs-lookup"><span data-stu-id="a67f9-132">Type</span></span>           | <span data-ttu-id="a67f9-133">Строка</span><span class="sxs-lookup"><span data-stu-id="a67f9-133">String</span></span>                    |
| <span data-ttu-id="a67f9-134">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a67f9-134">Default</span></span>        | <span data-ttu-id="a67f9-135">Н/Д</span><span class="sxs-lookup"><span data-stu-id="a67f9-135">N/A</span></span>                       |
| <span data-ttu-id="a67f9-136">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a67f9-136">Minimum system</span></span> | <span data-ttu-id="a67f9-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a67f9-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="a67f9-138">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-138">Description</span></span>



| <span data-ttu-id="a67f9-139">Ввод</span><span class="sxs-lookup"><span data-stu-id="a67f9-139">Entry</span></span> | <span data-ttu-id="a67f9-140">Значение</span><span class="sxs-lookup"><span data-stu-id="a67f9-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="a67f9-141">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-141">Description</span></span>    | <span data-ttu-id="a67f9-142">Описание интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a67f9-142">A description for the interface.</span></span> |
| <span data-ttu-id="a67f9-143">Access</span><span class="sxs-lookup"><span data-stu-id="a67f9-143">Access</span></span>         | <span data-ttu-id="a67f9-144">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a67f9-144">ReadWrite</span></span>                        |
| <span data-ttu-id="a67f9-145">Тип</span><span class="sxs-lookup"><span data-stu-id="a67f9-145">Type</span></span>           | <span data-ttu-id="a67f9-146">Строка</span><span class="sxs-lookup"><span data-stu-id="a67f9-146">String</span></span>                           |
| <span data-ttu-id="a67f9-147">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a67f9-147">Default</span></span>        | <span data-ttu-id="a67f9-148">""</span><span class="sxs-lookup"><span data-stu-id="a67f9-148">""</span></span>                               |
| <span data-ttu-id="a67f9-149">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a67f9-149">Minimum system</span></span> | <span data-ttu-id="a67f9-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a67f9-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="a67f9-151">IID</span><span class="sxs-lookup"><span data-stu-id="a67f9-151">IID</span></span>



| <span data-ttu-id="a67f9-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="a67f9-152">Entry</span></span> | <span data-ttu-id="a67f9-153">Значение</span><span class="sxs-lookup"><span data-stu-id="a67f9-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a67f9-154">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-154">Description</span></span>    | <span data-ttu-id="a67f9-155">Идентификатор GUID для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a67f9-155">A GUID for the interface.</span></span> <span data-ttu-id="a67f9-156">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="a67f9-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a67f9-157">Access</span><span class="sxs-lookup"><span data-stu-id="a67f9-157">Access</span></span>         | <span data-ttu-id="a67f9-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a67f9-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="a67f9-159">Тип</span><span class="sxs-lookup"><span data-stu-id="a67f9-159">Type</span></span>           | <span data-ttu-id="a67f9-160">Строка</span><span class="sxs-lookup"><span data-stu-id="a67f9-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="a67f9-161">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a67f9-161">Default</span></span>        | <span data-ttu-id="a67f9-162">Н/Д</span><span class="sxs-lookup"><span data-stu-id="a67f9-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="a67f9-163">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a67f9-163">Minimum system</span></span> | <span data-ttu-id="a67f9-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a67f9-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="a67f9-165">Имя</span><span class="sxs-lookup"><span data-stu-id="a67f9-165">Name</span></span>



| <span data-ttu-id="a67f9-166">Ввод</span><span class="sxs-lookup"><span data-stu-id="a67f9-166">Entry</span></span> | <span data-ttu-id="a67f9-167">Значение</span><span class="sxs-lookup"><span data-stu-id="a67f9-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a67f9-168">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-168">Description</span></span>    | <span data-ttu-id="a67f9-169">Имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a67f9-169">A name for the interface.</span></span> <span data-ttu-id="a67f9-170">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="a67f9-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a67f9-171">Access</span><span class="sxs-lookup"><span data-stu-id="a67f9-171">Access</span></span>         | <span data-ttu-id="a67f9-172">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a67f9-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="a67f9-173">Тип</span><span class="sxs-lookup"><span data-stu-id="a67f9-173">Type</span></span>           | <span data-ttu-id="a67f9-174">Строка</span><span class="sxs-lookup"><span data-stu-id="a67f9-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="a67f9-175">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a67f9-175">Default</span></span>        | <span data-ttu-id="a67f9-176">Н/Д</span><span class="sxs-lookup"><span data-stu-id="a67f9-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="a67f9-177">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a67f9-177">Minimum system</span></span> | <span data-ttu-id="a67f9-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a67f9-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="a67f9-179">куеуинженаблед</span><span class="sxs-lookup"><span data-stu-id="a67f9-179">QueuingEnabled</span></span>



| <span data-ttu-id="a67f9-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="a67f9-180">Entry</span></span> | <span data-ttu-id="a67f9-181">Значение</span><span class="sxs-lookup"><span data-stu-id="a67f9-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a67f9-182">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-182">Description</span></span>    | <span data-ttu-id="a67f9-183">Помечает интерфейс как куеуабле и может быть установлен с помощью средства администрирования SDK или служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="a67f9-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="a67f9-184">Однако флаг **включения очереди** может быть установлен только для интерфейса с установленным флагом " **Поддерживаемые очереди** ".</span><span class="sxs-lookup"><span data-stu-id="a67f9-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="a67f9-185">Access</span><span class="sxs-lookup"><span data-stu-id="a67f9-185">Access</span></span>         | <span data-ttu-id="a67f9-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a67f9-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="a67f9-187">Тип</span><span class="sxs-lookup"><span data-stu-id="a67f9-187">Type</span></span>           | <span data-ttu-id="a67f9-188">Bool</span><span class="sxs-lookup"><span data-stu-id="a67f9-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="a67f9-189">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a67f9-189">Default</span></span>        | <span data-ttu-id="a67f9-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="a67f9-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="a67f9-191">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a67f9-191">Minimum system</span></span> | <span data-ttu-id="a67f9-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a67f9-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="a67f9-193">куеуеингсуппортед</span><span class="sxs-lookup"><span data-stu-id="a67f9-193">QueueingSupported</span></span>



| <span data-ttu-id="a67f9-194">Ввод</span><span class="sxs-lookup"><span data-stu-id="a67f9-194">Entry</span></span> | <span data-ttu-id="a67f9-195">Значение</span><span class="sxs-lookup"><span data-stu-id="a67f9-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a67f9-196">Описание</span><span class="sxs-lookup"><span data-stu-id="a67f9-196">Description</span></span>    | <span data-ttu-id="a67f9-197">Интерфейс поддерживает очереди.</span><span class="sxs-lookup"><span data-stu-id="a67f9-197">Interface supports queuing.</span></span> <span data-ttu-id="a67f9-198">Для интерфейса, поддерживающего очереди, все методы должны иметь только параметры in.</span><span class="sxs-lookup"><span data-stu-id="a67f9-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="a67f9-199">**Поддерживаемая поддержка очередей** доступна в виде свойства, доступного только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a67f9-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="a67f9-200">Access</span><span class="sxs-lookup"><span data-stu-id="a67f9-200">Access</span></span>         | <span data-ttu-id="a67f9-201">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a67f9-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="a67f9-202">Тип</span><span class="sxs-lookup"><span data-stu-id="a67f9-202">Type</span></span>           | <span data-ttu-id="a67f9-203">Bool</span><span class="sxs-lookup"><span data-stu-id="a67f9-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a67f9-204">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a67f9-204">Default</span></span>        | <span data-ttu-id="a67f9-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="a67f9-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a67f9-206">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a67f9-206">Minimum system</span></span> | <span data-ttu-id="a67f9-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a67f9-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="a67f9-208">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a67f9-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67f9-209">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="a67f9-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
