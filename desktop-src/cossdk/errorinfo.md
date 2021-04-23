---
description: Извлекает расширенные сведения об ошибках для методов, связанных с несколькими объектами, таких как заполнение и SaveChanges в объекте Комадминкаталогколлектион, а также методы установки, импорта или экспорта приложений или компонентов в объекте Комадминкаталог.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Коллекция ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496458"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="ee7e1-103">Коллекция ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ee7e1-103">ErrorInfo collection</span></span>

<span data-ttu-id="ee7e1-104">Извлекает расширенные сведения об ошибках для методов, связанных с несколькими объектами, таких как [**Заполнение**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) и [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в объекте [**комадминкаталогколлектион**](comadmincatalogcollection.md) , а также методы установки, импорта или экспорта приложений или компонентов в объекте [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="ee7e1-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="ee7e1-105">Используйте метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) для [**комадминкаталогколлектион**](comadmincatalogcollection.md) , чтобы получить доступ к коллекции **errorInfo** , связанной с исходной коллекцией, которая содержит ошибку.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="ee7e1-106">Метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) следует вызывать в **errorInfo** сразу после возникновения ошибки. в противном случае сведения об ошибке теряются.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="ee7e1-107">Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ee7e1-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ee7e1-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="ee7e1-108">Members</span></span>

<span data-ttu-id="ee7e1-109">Коллекция **errorInfo** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ee7e1-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="ee7e1-110">Related Collections</span></span>

<span data-ttu-id="ee7e1-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="ee7e1-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ee7e1-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ee7e1-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ee7e1-113">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="ee7e1-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ee7e1-114">Можно переходить к этой коллекции из каждой коллекции, за исключением **errorInfo**, [**инпроксерверс**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**релатедколлектионинфо**](relatedcollectioninfo.md), [**root**](root.md)и [**вовинпроксерверс**](wowinprocservers.md).</span><span class="sxs-lookup"><span data-stu-id="ee7e1-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ee7e1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="ee7e1-115">Properties</span></span>

<span data-ttu-id="ee7e1-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ee7e1-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ee7e1-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ee7e1-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="ee7e1-118">мажорреф</span><span class="sxs-lookup"><span data-stu-id="ee7e1-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="ee7e1-119">минорреф</span><span class="sxs-lookup"><span data-stu-id="ee7e1-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="ee7e1-120">Name</span><span class="sxs-lookup"><span data-stu-id="ee7e1-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="ee7e1-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ee7e1-121">ErrorCode</span></span>



| <span data-ttu-id="ee7e1-122">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee7e1-122">Entry</span></span> | <span data-ttu-id="ee7e1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ee7e1-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="ee7e1-124">Описание</span><span class="sxs-lookup"><span data-stu-id="ee7e1-124">Description</span></span>    | <span data-ttu-id="ee7e1-125">Код ошибки для объекта или файла.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="ee7e1-126">Access</span><span class="sxs-lookup"><span data-stu-id="ee7e1-126">Access</span></span>         | <span data-ttu-id="ee7e1-127">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee7e1-127">ReadOnly</span></span>                               |
| <span data-ttu-id="ee7e1-128">Тип</span><span class="sxs-lookup"><span data-stu-id="ee7e1-128">Type</span></span>           | <span data-ttu-id="ee7e1-129">Строка</span><span class="sxs-lookup"><span data-stu-id="ee7e1-129">String</span></span>                                 |
| <span data-ttu-id="ee7e1-130">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee7e1-130">Default</span></span>        | <span data-ttu-id="ee7e1-131">None</span><span class="sxs-lookup"><span data-stu-id="ee7e1-131">None</span></span>                                   |
| <span data-ttu-id="ee7e1-132">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ee7e1-132">Minimum system</span></span> | <span data-ttu-id="ee7e1-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee7e1-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="ee7e1-134">мажорреф</span><span class="sxs-lookup"><span data-stu-id="ee7e1-134">MajorRef</span></span>



| <span data-ttu-id="ee7e1-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee7e1-135">Entry</span></span> | <span data-ttu-id="ee7e1-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ee7e1-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7e1-137">Описание</span><span class="sxs-lookup"><span data-stu-id="ee7e1-137">Description</span></span>    | <span data-ttu-id="ee7e1-138">Значение [**ключевого**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) свойства для объекта, который содержит ошибку.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="ee7e1-139">Например, если вызов [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) для коллекции завершается ошибкой для определенного объекта в коллекции, значение **ключевого** свойства для этого объекта указывается как значение мажорреф.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="ee7e1-140">Это свойство используется для просмотра элемента, который не удается обновить, или для поиска компонента или библиотеки DLL, которые не удается установить.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="ee7e1-141">Access</span><span class="sxs-lookup"><span data-stu-id="ee7e1-141">Access</span></span>         | <span data-ttu-id="ee7e1-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee7e1-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ee7e1-143">Тип</span><span class="sxs-lookup"><span data-stu-id="ee7e1-143">Type</span></span>           | <span data-ttu-id="ee7e1-144">Строка</span><span class="sxs-lookup"><span data-stu-id="ee7e1-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ee7e1-145">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee7e1-145">Default</span></span>        | <span data-ttu-id="ee7e1-146">None</span><span class="sxs-lookup"><span data-stu-id="ee7e1-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ee7e1-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ee7e1-147">Minimum system</span></span> | <span data-ttu-id="ee7e1-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee7e1-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="ee7e1-149">минорреф</span><span class="sxs-lookup"><span data-stu-id="ee7e1-149">MinorRef</span></span>



| <span data-ttu-id="ee7e1-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee7e1-150">Entry</span></span> | <span data-ttu-id="ee7e1-151">Значение</span><span class="sxs-lookup"><span data-stu-id="ee7e1-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7e1-152">Описание</span><span class="sxs-lookup"><span data-stu-id="ee7e1-152">Description</span></span>    | <span data-ttu-id="ee7e1-153">Точная спецификация элемента, имеющего ошибку, например имя свойства.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="ee7e1-154">Если возникает несколько ошибок или в контекстах, в которых это не применимо, Минорреф имеет значение <Invalid> .</span><span class="sxs-lookup"><span data-stu-id="ee7e1-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="ee7e1-155">Access</span><span class="sxs-lookup"><span data-stu-id="ee7e1-155">Access</span></span>         | <span data-ttu-id="ee7e1-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee7e1-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ee7e1-157">Тип</span><span class="sxs-lookup"><span data-stu-id="ee7e1-157">Type</span></span>           | <span data-ttu-id="ee7e1-158">Строка</span><span class="sxs-lookup"><span data-stu-id="ee7e1-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="ee7e1-159">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee7e1-159">Default</span></span>        | <span data-ttu-id="ee7e1-160">None</span><span class="sxs-lookup"><span data-stu-id="ee7e1-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="ee7e1-161">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ee7e1-161">Minimum system</span></span> | <span data-ttu-id="ee7e1-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee7e1-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="ee7e1-163">Имя</span><span class="sxs-lookup"><span data-stu-id="ee7e1-163">Name</span></span>



| <span data-ttu-id="ee7e1-164">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee7e1-164">Entry</span></span> | <span data-ttu-id="ee7e1-165">Значение</span><span class="sxs-lookup"><span data-stu-id="ee7e1-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7e1-166">Описание</span><span class="sxs-lookup"><span data-stu-id="ee7e1-166">Description</span></span>    | <span data-ttu-id="ee7e1-167">Имя объекта или файла с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="ee7e1-168">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="ee7e1-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ee7e1-169">Access</span><span class="sxs-lookup"><span data-stu-id="ee7e1-169">Access</span></span>         | <span data-ttu-id="ee7e1-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee7e1-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="ee7e1-171">Тип</span><span class="sxs-lookup"><span data-stu-id="ee7e1-171">Type</span></span>           | <span data-ttu-id="ee7e1-172">Строка</span><span class="sxs-lookup"><span data-stu-id="ee7e1-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="ee7e1-173">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee7e1-173">Default</span></span>        | <span data-ttu-id="ee7e1-174">None</span><span class="sxs-lookup"><span data-stu-id="ee7e1-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="ee7e1-175">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ee7e1-175">Minimum system</span></span> | <span data-ttu-id="ee7e1-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee7e1-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="ee7e1-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee7e1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7e1-178">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="ee7e1-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
