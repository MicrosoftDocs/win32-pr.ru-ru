---
description: Содержит список внутрипроцессного серверов, зарегистрированных в системе. Он содержит объект для каждого компонента, зарегистрированного как внутрипроцессный сервер.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Коллекция Инпроксерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710701"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="ba334-104">Коллекция Инпроксерверс</span><span class="sxs-lookup"><span data-stu-id="ba334-104">InprocServers collection</span></span>

<span data-ttu-id="ba334-105">Содержит список внутрипроцессного серверов, зарегистрированных в системе.</span><span class="sxs-lookup"><span data-stu-id="ba334-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="ba334-106">Он содержит объект для каждого компонента, зарегистрированного как внутрипроцессный сервер.</span><span class="sxs-lookup"><span data-stu-id="ba334-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="ba334-107">Эта коллекция поддерживает метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , но не метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="ba334-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="ba334-108">Чтобы установить или импортировать компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="ba334-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ba334-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ba334-109">Members</span></span>

<span data-ttu-id="ba334-110">Коллекция **инпроксерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="ba334-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ba334-111">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="ba334-111">Related Collections</span></span>

<span data-ttu-id="ba334-112">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="ba334-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ba334-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ba334-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ba334-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="ba334-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ba334-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="ba334-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ba334-116">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="ba334-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ba334-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba334-117">Properties</span></span>

<span data-ttu-id="ba334-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ba334-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ba334-119">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="ba334-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="ba334-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ba334-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="ba334-121">ProgID:</span><span class="sxs-lookup"><span data-stu-id="ba334-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="ba334-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="ba334-122">CLSID</span></span>



| <span data-ttu-id="ba334-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba334-123">Entry</span></span> | <span data-ttu-id="ba334-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ba334-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba334-125">Описание</span><span class="sxs-lookup"><span data-stu-id="ba334-125">Description</span></span>    | <span data-ttu-id="ba334-126">Идентификатор GUID для компонента.</span><span class="sxs-lookup"><span data-stu-id="ba334-126">A GUID for the component.</span></span> <span data-ttu-id="ba334-127">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="ba334-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ba334-128">Access</span><span class="sxs-lookup"><span data-stu-id="ba334-128">Access</span></span>         | <span data-ttu-id="ba334-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ba334-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba334-130">Тип</span><span class="sxs-lookup"><span data-stu-id="ba334-130">Type</span></span>           | <span data-ttu-id="ba334-131">Строка</span><span class="sxs-lookup"><span data-stu-id="ba334-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="ba334-132">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba334-132">Default</span></span>        | <span data-ttu-id="ba334-133">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ba334-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="ba334-134">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ba334-134">Minimum system</span></span> | <span data-ttu-id="ba334-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ba334-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="ba334-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ba334-136">InprocServer32</span></span>



| <span data-ttu-id="ba334-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba334-137">Entry</span></span> | <span data-ttu-id="ba334-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ba334-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="ba334-139">Описание</span><span class="sxs-lookup"><span data-stu-id="ba334-139">Description</span></span>    | <span data-ttu-id="ba334-140">Путь к файлу для компонента.</span><span class="sxs-lookup"><span data-stu-id="ba334-140">The file path for the component.</span></span> |
| <span data-ttu-id="ba334-141">Access</span><span class="sxs-lookup"><span data-stu-id="ba334-141">Access</span></span>         | <span data-ttu-id="ba334-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ba334-142">ReadOnly</span></span>                         |
| <span data-ttu-id="ba334-143">Тип</span><span class="sxs-lookup"><span data-stu-id="ba334-143">Type</span></span>           | <span data-ttu-id="ba334-144">Строка</span><span class="sxs-lookup"><span data-stu-id="ba334-144">String</span></span>                           |
| <span data-ttu-id="ba334-145">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba334-145">Default</span></span>        | <span data-ttu-id="ba334-146">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ba334-146">N/A</span></span>                              |
| <span data-ttu-id="ba334-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ba334-147">Minimum system</span></span> | <span data-ttu-id="ba334-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ba334-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="ba334-149">ProgID:</span><span class="sxs-lookup"><span data-stu-id="ba334-149">ProgID</span></span>



| <span data-ttu-id="ba334-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="ba334-150">Entry</span></span> | <span data-ttu-id="ba334-151">Значение</span><span class="sxs-lookup"><span data-stu-id="ba334-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba334-152">Описание</span><span class="sxs-lookup"><span data-stu-id="ba334-152">Description</span></span>    | <span data-ttu-id="ba334-153">Имя, идентифицирующее компонент.</span><span class="sxs-lookup"><span data-stu-id="ba334-153">A name identifying the component.</span></span> <span data-ttu-id="ba334-154">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="ba334-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ba334-155">Access</span><span class="sxs-lookup"><span data-stu-id="ba334-155">Access</span></span>         | <span data-ttu-id="ba334-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ba334-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="ba334-157">Тип</span><span class="sxs-lookup"><span data-stu-id="ba334-157">Type</span></span>           | <span data-ttu-id="ba334-158">Строка</span><span class="sxs-lookup"><span data-stu-id="ba334-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="ba334-159">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba334-159">Default</span></span>        | <span data-ttu-id="ba334-160">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ba334-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="ba334-161">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ba334-161">Minimum system</span></span> | <span data-ttu-id="ba334-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ba334-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="ba334-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba334-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba334-164">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="ba334-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
