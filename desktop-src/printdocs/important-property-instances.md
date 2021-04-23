---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Важные экземпляры свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720815"
---
# <a name="important-property-instances"></a><span data-ttu-id="8d53f-104">Важные экземпляры свойств</span><span class="sxs-lookup"><span data-stu-id="8d53f-104">Important Property Instances</span></span>

<span data-ttu-id="8d53f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8d53f-105">This topic is not current.</span></span> <span data-ttu-id="8d53f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8d53f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d53f-107">Чтобы клиент PrintCapabilities мог создать разумное значение PrintTicket, документ PrintCapabilities должен предоставлять определенные свойства экземпляров компонентов, а также экземпляры параметров в этой функции.</span><span class="sxs-lookup"><span data-stu-id="8d53f-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="8d53f-108">Универсальный модуль пользовательского интерфейса требует такой информации для создания пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8d53f-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="8d53f-109">Это, в свою очередь, требует, чтобы ключевые слова схемы Print определяли несколько экземпляров свойств, которые отображаются как дочерние элементы функций и элементов Option.</span><span class="sxs-lookup"><span data-stu-id="8d53f-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="8d53f-110">Элементы компонента могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8d53f-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="8d53f-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d53f-111">Property</span></span>                  | <span data-ttu-id="8d53f-112">Значения</span><span class="sxs-lookup"><span data-stu-id="8d53f-112">Values</span></span>                                 | <span data-ttu-id="8d53f-113">Назначение</span><span class="sxs-lookup"><span data-stu-id="8d53f-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d53f-114">селектионтипе</span><span class="sxs-lookup"><span data-stu-id="8d53f-114">SelectionType</span></span> <br/> | <span data-ttu-id="8d53f-115">пикконе</span><span class="sxs-lookup"><span data-stu-id="8d53f-115">PickOne</span></span><br/> <span data-ttu-id="8d53f-116">пиккмани</span><span class="sxs-lookup"><span data-stu-id="8d53f-116">PickMany</span></span><br/> | <span data-ttu-id="8d53f-117">Указывает количество параметров, которые могут быть выбраны для этой функции в определенный момент времени (Пикконе) или несколько (Пиккмани).</span><span class="sxs-lookup"><span data-stu-id="8d53f-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="8d53f-118">Клиент может использовать эти сведения для создания PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8d53f-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="8d53f-119">Эта информация влияет на поведение пользовательского интерфейса, а также на проверку PrintTicket поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8d53f-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="8d53f-120">Элементы Option могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8d53f-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="8d53f-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d53f-121">Property</span></span>                   | <span data-ttu-id="8d53f-122">Значения</span><span class="sxs-lookup"><span data-stu-id="8d53f-122">Values</span></span>                           | <span data-ttu-id="8d53f-123">Назначение</span><span class="sxs-lookup"><span data-stu-id="8d53f-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d53f-124">идентитйоптион</span><span class="sxs-lookup"><span data-stu-id="8d53f-124">IdentityOption</span></span> <br/> | <span data-ttu-id="8d53f-125">True</span><span class="sxs-lookup"><span data-stu-id="8d53f-125">True</span></span><br/> <span data-ttu-id="8d53f-126">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d53f-126">False</span></span><br/> | <span data-ttu-id="8d53f-127">Выбор свойства Идентитйоптион интерпретируется как "отключить эту функцию".</span><span class="sxs-lookup"><span data-stu-id="8d53f-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="8d53f-128">Функция, которая содержит свойство Селектионтипе, значение которого равно Пиккмани, также должно содержать параметр, имеющий свойство Идентитйоптион.</span><span class="sxs-lookup"><span data-stu-id="8d53f-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="8d53f-129">Код пользовательского интерфейса (или клиент, создающий PrintTicket) должен отменить выбор любого другого параметра, если выбрано свойство Идентитйоптион.</span><span class="sxs-lookup"><span data-stu-id="8d53f-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="8d53f-130">Элементы feature, Option и Параметердеф могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8d53f-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="8d53f-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d53f-131">Property</span></span>              | <span data-ttu-id="8d53f-132">Значения</span><span class="sxs-lookup"><span data-stu-id="8d53f-132">Values</span></span>                          | <span data-ttu-id="8d53f-133">Назначение</span><span class="sxs-lookup"><span data-stu-id="8d53f-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d53f-134">дисплайуи</span><span class="sxs-lookup"><span data-stu-id="8d53f-134">DisplayUI</span></span> <br/> | <span data-ttu-id="8d53f-135">Показать</span><span class="sxs-lookup"><span data-stu-id="8d53f-135">Show</span></span><br/> <span data-ttu-id="8d53f-136">Скрыть</span><span class="sxs-lookup"><span data-stu-id="8d53f-136">Hide</span></span><br/> | <span data-ttu-id="8d53f-137">Указывает, должен ли родительский элемент отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8d53f-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="8d53f-138">Показать указывает, что элемент должен отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8d53f-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="8d53f-139">Скрыть указывает, что элемент не должен отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8d53f-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="8d53f-140">Если это свойство не определено для элемента, то интерпретация по умолчанию показывает, что элемент отображается.</span><span class="sxs-lookup"><span data-stu-id="8d53f-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="8d53f-141">Элементы feature, Option и Параметердеф могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8d53f-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="8d53f-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d53f-142">Property</span></span>                | <span data-ttu-id="8d53f-143">Значение</span><span class="sxs-lookup"><span data-stu-id="8d53f-143">Value</span></span>             | <span data-ttu-id="8d53f-144">Назначение</span><span class="sxs-lookup"><span data-stu-id="8d53f-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d53f-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="8d53f-145">DisplayName</span></span> <br/> | <span data-ttu-id="8d53f-146">Строка</span><span class="sxs-lookup"><span data-stu-id="8d53f-146">String</span></span><br/> | <span data-ttu-id="8d53f-147">Задает отображаемую строку для родительского элемента, переопределяя отображаемое имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d53f-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="8d53f-148">Может использоваться поставщиками PrintCapabilities для представления локализованного и понятного отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="8d53f-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="8d53f-149">Значение отображаемого имени по умолчанию — это атрибут имени для родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="8d53f-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="8d53f-150">В случае использования элементов Option, если атрибут name не указан, должно присутствовать свойство DisplayName.</span><span class="sxs-lookup"><span data-stu-id="8d53f-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8d53f-151">См. также</span><span class="sxs-lookup"><span data-stu-id="8d53f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d53f-152">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8d53f-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




