---
description: Содержит список внутрипроцессного серверов, зарегистрированных в системе для 32-разрядных компонентов на 64-разрядных компьютерах. Он содержит объект для каждого компонента.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Коллекция Вовинпроксерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 43fceababaf6ced44a1ba3aef020900ed1afe4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538579"
---
# <a name="wowinprocservers-collection"></a><span data-ttu-id="2e2bc-104">Коллекция Вовинпроксерверс</span><span class="sxs-lookup"><span data-stu-id="2e2bc-104">WOWInprocServers collection</span></span>

<span data-ttu-id="2e2bc-105">Содержит список внутрипроцессного серверов, зарегистрированных в системе для 32-разрядных компонентов на 64-разрядных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-105">Contains a list of the in-process servers registered with the system for 32-bit components on 64-bit computers.</span></span> <span data-ttu-id="2e2bc-106">Он содержит объект для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-106">It contains an object for each component.</span></span>

<span data-ttu-id="2e2bc-107">Эта коллекция поддерживает метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , но не метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="2e2bc-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="2e2bc-108">Чтобы установить или импортировать компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2bc-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="2e2bc-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="2e2bc-109">Members</span></span>

<span data-ttu-id="2e2bc-110">Коллекция **вовинпроксерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-110">The **WOWInprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="2e2bc-111">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="2e2bc-111">Related Collections</span></span>

<span data-ttu-id="2e2bc-112">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="2e2bc-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="2e2bc-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="2e2bc-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="2e2bc-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="2e2bc-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="2e2bc-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="2e2bc-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="2e2bc-116">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="2e2bc-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="2e2bc-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e2bc-117">Properties</span></span>

<span data-ttu-id="2e2bc-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="2e2bc-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="2e2bc-119">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="2e2bc-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="2e2bc-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="2e2bc-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="2e2bc-121">ProgID:</span><span class="sxs-lookup"><span data-stu-id="2e2bc-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="2e2bc-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="2e2bc-122">CLSID</span></span>



| <span data-ttu-id="2e2bc-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e2bc-123">Entry</span></span> | <span data-ttu-id="2e2bc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2e2bc-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2bc-125">Описание</span><span class="sxs-lookup"><span data-stu-id="2e2bc-125">Description</span></span>    | <span data-ttu-id="2e2bc-126">Идентификатор GUID для компонента.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-126">A GUID for the component.</span></span> <span data-ttu-id="2e2bc-127">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2e2bc-128">Access</span><span class="sxs-lookup"><span data-stu-id="2e2bc-128">Access</span></span>         | <span data-ttu-id="2e2bc-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2e2bc-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="2e2bc-130">Тип</span><span class="sxs-lookup"><span data-stu-id="2e2bc-130">Type</span></span>           | <span data-ttu-id="2e2bc-131">Строка</span><span class="sxs-lookup"><span data-stu-id="2e2bc-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="2e2bc-132">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e2bc-132">Default</span></span>        | <span data-ttu-id="2e2bc-133">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2e2bc-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="2e2bc-134">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="2e2bc-134">Minimum system</span></span> | <span data-ttu-id="2e2bc-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e2bc-135">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="2e2bc-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="2e2bc-136">InprocServer32</span></span>



| <span data-ttu-id="2e2bc-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e2bc-137">Entry</span></span> | <span data-ttu-id="2e2bc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="2e2bc-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="2e2bc-139">Описание</span><span class="sxs-lookup"><span data-stu-id="2e2bc-139">Description</span></span>    | <span data-ttu-id="2e2bc-140">Путь к файлу для компонента.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-140">The file path for the component.</span></span> |
| <span data-ttu-id="2e2bc-141">Access</span><span class="sxs-lookup"><span data-stu-id="2e2bc-141">Access</span></span>         | <span data-ttu-id="2e2bc-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2e2bc-142">ReadOnly</span></span>                         |
| <span data-ttu-id="2e2bc-143">Тип</span><span class="sxs-lookup"><span data-stu-id="2e2bc-143">Type</span></span>           | <span data-ttu-id="2e2bc-144">Строка</span><span class="sxs-lookup"><span data-stu-id="2e2bc-144">String</span></span>                           |
| <span data-ttu-id="2e2bc-145">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e2bc-145">Default</span></span>        | <span data-ttu-id="2e2bc-146">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2e2bc-146">N/A</span></span>                              |
| <span data-ttu-id="2e2bc-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="2e2bc-147">Minimum system</span></span> | <span data-ttu-id="2e2bc-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e2bc-148">Windows XP</span></span>                       |



 

### <a name="progid"></a><span data-ttu-id="2e2bc-149">ProgID:</span><span class="sxs-lookup"><span data-stu-id="2e2bc-149">ProgID</span></span>



| <span data-ttu-id="2e2bc-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e2bc-150">Entry</span></span> | <span data-ttu-id="2e2bc-151">Значение</span><span class="sxs-lookup"><span data-stu-id="2e2bc-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2bc-152">Описание</span><span class="sxs-lookup"><span data-stu-id="2e2bc-152">Description</span></span>    | <span data-ttu-id="2e2bc-153">Имя, идентифицирующее компонент.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-153">A name identifying the component.</span></span> <span data-ttu-id="2e2bc-154">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="2e2bc-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="2e2bc-155">Access</span><span class="sxs-lookup"><span data-stu-id="2e2bc-155">Access</span></span>         | <span data-ttu-id="2e2bc-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2e2bc-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="2e2bc-157">Тип</span><span class="sxs-lookup"><span data-stu-id="2e2bc-157">Type</span></span>           | <span data-ttu-id="2e2bc-158">Строка</span><span class="sxs-lookup"><span data-stu-id="2e2bc-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="2e2bc-159">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e2bc-159">Default</span></span>        | <span data-ttu-id="2e2bc-160">Н/Д</span><span class="sxs-lookup"><span data-stu-id="2e2bc-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="2e2bc-161">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="2e2bc-161">Minimum system</span></span> | <span data-ttu-id="2e2bc-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e2bc-162">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="2e2bc-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e2bc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2bc-164">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="2e2bc-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
