---
description: Предоставляемые свойства для коллекции Вовлегацисерверс должны быть идентичны коллекции Легацисерверс, за исключением того, что коллекция Вовлегацисерверс отрисовывается из 32-разрядного реестра на 64-разрядных компьютерах.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Коллекция Вовлегацисерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701191"
---
# <a name="wowlegacyservers-collection"></a><span data-ttu-id="60805-103">Коллекция Вовлегацисерверс</span><span class="sxs-lookup"><span data-stu-id="60805-103">WOWLegacyServers collection</span></span>

<span data-ttu-id="60805-104">Предоставляемые свойства для коллекции **вовлегацисерверс** должны быть идентичны коллекции [**легацисерверс**](legacyservers.md) , за исключением того, что коллекция **вовлегацисерверс** отрисовывается из 32-разрядного реестра на 64-разрядных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="60805-104">Exposed properties for the **WOWLegacyServers** collection are intended to be identical to the [**LegacyServers**](legacyservers.md) collection except that the **WOWLegacyServers** collection is drawn from the 32-bit registry on 64-bit computers.</span></span>

<span data-ttu-id="60805-105">Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="60805-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="60805-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="60805-106">Members</span></span>

<span data-ttu-id="60805-107">Коллекция **вовлегацисерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="60805-107">The **WOWLegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="60805-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="60805-108">Related Collections</span></span>

<span data-ttu-id="60805-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="60805-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="60805-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="60805-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="60805-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="60805-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="60805-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="60805-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="60805-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="60805-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="60805-114">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="60805-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="60805-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="60805-115">Properties</span></span>

<span data-ttu-id="60805-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="60805-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="60805-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="60805-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="60805-118">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="60805-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="60805-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="60805-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="60805-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="60805-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="60805-121">ProgID:</span><span class="sxs-lookup"><span data-stu-id="60805-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="60805-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="60805-122">ClassName</span></span>



| <span data-ttu-id="60805-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="60805-123">Entry</span></span> | <span data-ttu-id="60805-124">Значение</span><span class="sxs-lookup"><span data-stu-id="60805-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="60805-125">Описание</span><span class="sxs-lookup"><span data-stu-id="60805-125">Description</span></span>    | <span data-ttu-id="60805-126">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="60805-126">The name of the class.</span></span> |
| <span data-ttu-id="60805-127">Access</span><span class="sxs-lookup"><span data-stu-id="60805-127">Access</span></span>         | <span data-ttu-id="60805-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="60805-128">ReadOnly</span></span>               |
| <span data-ttu-id="60805-129">Тип</span><span class="sxs-lookup"><span data-stu-id="60805-129">Type</span></span>           | <span data-ttu-id="60805-130">Строка</span><span class="sxs-lookup"><span data-stu-id="60805-130">String</span></span>                 |
| <span data-ttu-id="60805-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="60805-131">Default</span></span>        | <span data-ttu-id="60805-132">Н/Д</span><span class="sxs-lookup"><span data-stu-id="60805-132">N/A</span></span>                    |
| <span data-ttu-id="60805-133">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="60805-133">Minimum system</span></span> | <span data-ttu-id="60805-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60805-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="60805-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="60805-135">CLSID</span></span>



| <span data-ttu-id="60805-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="60805-136">Entry</span></span> | <span data-ttu-id="60805-137">Значение</span><span class="sxs-lookup"><span data-stu-id="60805-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60805-138">Описание</span><span class="sxs-lookup"><span data-stu-id="60805-138">Description</span></span>    | <span data-ttu-id="60805-139">Идентификатор GUID для компонента.</span><span class="sxs-lookup"><span data-stu-id="60805-139">A GUID for the component.</span></span> <span data-ttu-id="60805-140">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="60805-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="60805-141">Access</span><span class="sxs-lookup"><span data-stu-id="60805-141">Access</span></span>         | <span data-ttu-id="60805-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="60805-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="60805-143">Тип</span><span class="sxs-lookup"><span data-stu-id="60805-143">Type</span></span>           | <span data-ttu-id="60805-144">Строка</span><span class="sxs-lookup"><span data-stu-id="60805-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="60805-145">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="60805-145">Default</span></span>        | <span data-ttu-id="60805-146">Н/Д</span><span class="sxs-lookup"><span data-stu-id="60805-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="60805-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="60805-147">Minimum system</span></span> | <span data-ttu-id="60805-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60805-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="60805-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="60805-149">InprocServer32</span></span>



| <span data-ttu-id="60805-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="60805-150">Entry</span></span> | <span data-ttu-id="60805-151">Значение</span><span class="sxs-lookup"><span data-stu-id="60805-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="60805-152">Описание</span><span class="sxs-lookup"><span data-stu-id="60805-152">Description</span></span>    | <span data-ttu-id="60805-153">Путь к файлу для компонента.</span><span class="sxs-lookup"><span data-stu-id="60805-153">The file path for the component.</span></span> |
| <span data-ttu-id="60805-154">Access</span><span class="sxs-lookup"><span data-stu-id="60805-154">Access</span></span>         | <span data-ttu-id="60805-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="60805-155">ReadOnly</span></span>                         |
| <span data-ttu-id="60805-156">Тип</span><span class="sxs-lookup"><span data-stu-id="60805-156">Type</span></span>           | <span data-ttu-id="60805-157">Строка</span><span class="sxs-lookup"><span data-stu-id="60805-157">String</span></span>                           |
| <span data-ttu-id="60805-158">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="60805-158">Default</span></span>        | <span data-ttu-id="60805-159">Н/Д</span><span class="sxs-lookup"><span data-stu-id="60805-159">N/A</span></span>                              |
| <span data-ttu-id="60805-160">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="60805-160">Minimum system</span></span> | <span data-ttu-id="60805-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60805-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="60805-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="60805-162">LocalServer32</span></span>



| <span data-ttu-id="60805-163">Ввод</span><span class="sxs-lookup"><span data-stu-id="60805-163">Entry</span></span> | <span data-ttu-id="60805-164">Значение</span><span class="sxs-lookup"><span data-stu-id="60805-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="60805-165">Описание</span><span class="sxs-lookup"><span data-stu-id="60805-165">Description</span></span>    | <span data-ttu-id="60805-166">Указывает полный путь к 32-битному локальному серверному приложению.</span><span class="sxs-lookup"><span data-stu-id="60805-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="60805-167">Access</span><span class="sxs-lookup"><span data-stu-id="60805-167">Access</span></span>         | <span data-ttu-id="60805-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="60805-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="60805-169">Тип</span><span class="sxs-lookup"><span data-stu-id="60805-169">Type</span></span>           | <span data-ttu-id="60805-170">Строка</span><span class="sxs-lookup"><span data-stu-id="60805-170">String</span></span>                                                        |
| <span data-ttu-id="60805-171">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="60805-171">Default</span></span>        | <span data-ttu-id="60805-172">Н/Д</span><span class="sxs-lookup"><span data-stu-id="60805-172">N/A</span></span>                                                           |
| <span data-ttu-id="60805-173">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="60805-173">Minimum system</span></span> | <span data-ttu-id="60805-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60805-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="60805-175">ProgID:</span><span class="sxs-lookup"><span data-stu-id="60805-175">ProgID</span></span>



| <span data-ttu-id="60805-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="60805-176">Entry</span></span> | <span data-ttu-id="60805-177">Значение</span><span class="sxs-lookup"><span data-stu-id="60805-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60805-178">Описание</span><span class="sxs-lookup"><span data-stu-id="60805-178">Description</span></span>    | <span data-ttu-id="60805-179">Имя, идентифицирующее компонент.</span><span class="sxs-lookup"><span data-stu-id="60805-179">A name identifying the component.</span></span> <span data-ttu-id="60805-180">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="60805-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="60805-181">Access</span><span class="sxs-lookup"><span data-stu-id="60805-181">Access</span></span>         | <span data-ttu-id="60805-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="60805-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="60805-183">Тип</span><span class="sxs-lookup"><span data-stu-id="60805-183">Type</span></span>           | <span data-ttu-id="60805-184">Строка</span><span class="sxs-lookup"><span data-stu-id="60805-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="60805-185">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="60805-185">Default</span></span>        | <span data-ttu-id="60805-186">Н/Д</span><span class="sxs-lookup"><span data-stu-id="60805-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="60805-187">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="60805-187">Minimum system</span></span> | <span data-ttu-id="60805-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60805-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="60805-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60805-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60805-190">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="60805-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
