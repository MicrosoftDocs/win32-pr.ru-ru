---
description: Получает сведения о классах событий.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Коллекция Евентклассесфориид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141378"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="374f0-103">Коллекция Евентклассесфориид</span><span class="sxs-lookup"><span data-stu-id="374f0-103">EventClassesForIID collection</span></span>

<span data-ttu-id="374f0-104">Получает сведения о классах событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="374f0-105">Соединение между издателем и подписчиками управляется объектом [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , который представляет собой компонент COM+, который содержит интерфейсы и методы, используемые издателем для запуска событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="374f0-106">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="374f0-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="374f0-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="374f0-107">Members</span></span>

<span data-ttu-id="374f0-108">Коллекция **евентклассесфориид** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="374f0-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="374f0-109">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="374f0-109">Related Collections</span></span>

<span data-ttu-id="374f0-110">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="374f0-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="374f0-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="374f0-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="374f0-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="374f0-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="374f0-113">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="374f0-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="374f0-114">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="374f0-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="374f0-115">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="374f0-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="374f0-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="374f0-116">Properties</span></span>

<span data-ttu-id="374f0-117">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="374f0-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="374f0-118">Приложение</span><span class="sxs-lookup"><span data-stu-id="374f0-118">Application</span></span>](#application)
-   [<span data-ttu-id="374f0-119">Разрядность</span><span class="sxs-lookup"><span data-stu-id="374f0-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="374f0-120">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="374f0-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="374f0-121">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-121">Description</span></span>](#description)
-   [<span data-ttu-id="374f0-122">исприватекомпонент</span><span class="sxs-lookup"><span data-stu-id="374f0-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="374f0-123">ProgID:</span><span class="sxs-lookup"><span data-stu-id="374f0-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="374f0-124">Приложение</span><span class="sxs-lookup"><span data-stu-id="374f0-124">Application</span></span>



| <span data-ttu-id="374f0-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="374f0-125">Entry</span></span> | <span data-ttu-id="374f0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="374f0-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="374f0-127">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-127">Description</span></span>    | <span data-ttu-id="374f0-128">Идентификатор GUID для приложения, содержащего класс событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="374f0-129">Access</span><span class="sxs-lookup"><span data-stu-id="374f0-129">Access</span></span>         | <span data-ttu-id="374f0-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="374f0-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="374f0-131">Тип</span><span class="sxs-lookup"><span data-stu-id="374f0-131">Type</span></span>           | <span data-ttu-id="374f0-132">Строка</span><span class="sxs-lookup"><span data-stu-id="374f0-132">String</span></span>                                                   |
| <span data-ttu-id="374f0-133">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="374f0-133">Default</span></span>        | <span data-ttu-id="374f0-134">Н/Д</span><span class="sxs-lookup"><span data-stu-id="374f0-134">N/A</span></span>                                                      |
| <span data-ttu-id="374f0-135">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="374f0-135">Minimum system</span></span> | <span data-ttu-id="374f0-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="374f0-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="374f0-137">Разрядность</span><span class="sxs-lookup"><span data-stu-id="374f0-137">Bitness</span></span>



| <span data-ttu-id="374f0-138">Ввод</span><span class="sxs-lookup"><span data-stu-id="374f0-138">Entry</span></span> | <span data-ttu-id="374f0-139">Значение</span><span class="sxs-lookup"><span data-stu-id="374f0-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374f0-140">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-140">Description</span></span>    | <span data-ttu-id="374f0-141">Представляет тип разрядности двоичного файла класса событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="374f0-142">В системах, использующих 64-разрядную версию Windows, это свойство различает 64-разрядные компоненты и 32-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="374f0-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="374f0-143">Access</span><span class="sxs-lookup"><span data-stu-id="374f0-143">Access</span></span>         | <span data-ttu-id="374f0-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="374f0-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="374f0-145">Тип</span><span class="sxs-lookup"><span data-stu-id="374f0-145">Type</span></span>           | <span data-ttu-id="374f0-146">Длинные возможные значения: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="374f0-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="374f0-147">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="374f0-147">Default</span></span>        | <span data-ttu-id="374f0-148">Н/Д</span><span class="sxs-lookup"><span data-stu-id="374f0-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="374f0-149">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="374f0-149">Minimum system</span></span> | <span data-ttu-id="374f0-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="374f0-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="374f0-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="374f0-151">CLSID</span></span>



| <span data-ttu-id="374f0-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="374f0-152">Entry</span></span> | <span data-ttu-id="374f0-153">Значение</span><span class="sxs-lookup"><span data-stu-id="374f0-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374f0-154">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-154">Description</span></span>    | <span data-ttu-id="374f0-155">Идентификатор GUID для класса событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-155">The GUID for the event class.</span></span> <span data-ttu-id="374f0-156">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="374f0-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="374f0-157">Access</span><span class="sxs-lookup"><span data-stu-id="374f0-157">Access</span></span>         | <span data-ttu-id="374f0-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="374f0-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="374f0-159">Тип</span><span class="sxs-lookup"><span data-stu-id="374f0-159">Type</span></span>           | <span data-ttu-id="374f0-160">Строка</span><span class="sxs-lookup"><span data-stu-id="374f0-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="374f0-161">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="374f0-161">Default</span></span>        | <span data-ttu-id="374f0-162">Н/Д</span><span class="sxs-lookup"><span data-stu-id="374f0-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="374f0-163">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="374f0-163">Minimum system</span></span> | <span data-ttu-id="374f0-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="374f0-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="374f0-165">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-165">Description</span></span>



| <span data-ttu-id="374f0-166">Ввод</span><span class="sxs-lookup"><span data-stu-id="374f0-166">Entry</span></span> | <span data-ttu-id="374f0-167">Значение</span><span class="sxs-lookup"><span data-stu-id="374f0-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="374f0-168">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-168">Description</span></span>    | <span data-ttu-id="374f0-169">Описывает класс событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-169">Describes the event class.</span></span> |
| <span data-ttu-id="374f0-170">Access</span><span class="sxs-lookup"><span data-stu-id="374f0-170">Access</span></span>         | <span data-ttu-id="374f0-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="374f0-171">ReadOnly</span></span>                   |
| <span data-ttu-id="374f0-172">Тип</span><span class="sxs-lookup"><span data-stu-id="374f0-172">Type</span></span>           | <span data-ttu-id="374f0-173">Строка</span><span class="sxs-lookup"><span data-stu-id="374f0-173">String</span></span>                     |
| <span data-ttu-id="374f0-174">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="374f0-174">Default</span></span>        | <span data-ttu-id="374f0-175">""</span><span class="sxs-lookup"><span data-stu-id="374f0-175">""</span></span>                         |
| <span data-ttu-id="374f0-176">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="374f0-176">Minimum system</span></span> | <span data-ttu-id="374f0-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="374f0-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="374f0-178">исприватекомпонент</span><span class="sxs-lookup"><span data-stu-id="374f0-178">IsPrivateComponent</span></span>



| <span data-ttu-id="374f0-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="374f0-179">Entry</span></span> | <span data-ttu-id="374f0-180">Значение</span><span class="sxs-lookup"><span data-stu-id="374f0-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="374f0-181">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-181">Description</span></span>    | <span data-ttu-id="374f0-182">Указывает, является ли компонент класса событий закрытым.</span><span class="sxs-lookup"><span data-stu-id="374f0-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="374f0-183">Access</span><span class="sxs-lookup"><span data-stu-id="374f0-183">Access</span></span>         | <span data-ttu-id="374f0-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="374f0-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="374f0-185">Тип</span><span class="sxs-lookup"><span data-stu-id="374f0-185">Type</span></span>           | <span data-ttu-id="374f0-186">Bool</span><span class="sxs-lookup"><span data-stu-id="374f0-186">Bool</span></span>                                                    |
| <span data-ttu-id="374f0-187">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="374f0-187">Default</span></span>        | <span data-ttu-id="374f0-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="374f0-188">False</span></span>                                                   |
| <span data-ttu-id="374f0-189">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="374f0-189">Minimum system</span></span> | <span data-ttu-id="374f0-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="374f0-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="374f0-191">ProgID:</span><span class="sxs-lookup"><span data-stu-id="374f0-191">ProgID</span></span>



| <span data-ttu-id="374f0-192">Ввод</span><span class="sxs-lookup"><span data-stu-id="374f0-192">Entry</span></span> | <span data-ttu-id="374f0-193">Значение</span><span class="sxs-lookup"><span data-stu-id="374f0-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374f0-194">Описание</span><span class="sxs-lookup"><span data-stu-id="374f0-194">Description</span></span>    | <span data-ttu-id="374f0-195">Понятное имя, используемое для распознавания класса событий.</span><span class="sxs-lookup"><span data-stu-id="374f0-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="374f0-196">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="374f0-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="374f0-197">Access</span><span class="sxs-lookup"><span data-stu-id="374f0-197">Access</span></span>         | <span data-ttu-id="374f0-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="374f0-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="374f0-199">Тип</span><span class="sxs-lookup"><span data-stu-id="374f0-199">Type</span></span>           | <span data-ttu-id="374f0-200">Строка</span><span class="sxs-lookup"><span data-stu-id="374f0-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="374f0-201">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="374f0-201">Default</span></span>        | <span data-ttu-id="374f0-202">""</span><span class="sxs-lookup"><span data-stu-id="374f0-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="374f0-203">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="374f0-203">Minimum system</span></span> | <span data-ttu-id="374f0-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="374f0-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="374f0-205">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="374f0-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374f0-206">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="374f0-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
