---
description: Чтобы клиент конструирует PrintTicket, документ PrintCapabilities должен предоставлять свойства экземпляров компонента и экземпляров параметров в функции.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Важные экземпляры свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409127"
---
# <a name="important-property-instances"></a><span data-ttu-id="93639-103">Важные экземпляры свойств</span><span class="sxs-lookup"><span data-stu-id="93639-103">Important Property Instances</span></span>

<span data-ttu-id="93639-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="93639-104">This topic is not current.</span></span> <span data-ttu-id="93639-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="93639-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="93639-106">Чтобы клиент PrintCapabilities мог создать разумное значение PrintTicket, документ PrintCapabilities должен предоставлять определенные свойства экземпляров компонентов, а также экземпляры параметров в этой функции.</span><span class="sxs-lookup"><span data-stu-id="93639-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="93639-107">Универсальный модуль пользовательского интерфейса требует такой информации для создания пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="93639-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="93639-108">Это, в свою очередь, требует, чтобы ключевые слова схемы Print определяли несколько экземпляров свойств, которые отображаются как дочерние элементы функций и элементов Option.</span><span class="sxs-lookup"><span data-stu-id="93639-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="93639-109">Элементы компонента могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="93639-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="93639-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="93639-110">Property</span></span>                  | <span data-ttu-id="93639-111">Значения</span><span class="sxs-lookup"><span data-stu-id="93639-111">Values</span></span>                                 | <span data-ttu-id="93639-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="93639-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93639-113">селектионтипе</span><span class="sxs-lookup"><span data-stu-id="93639-113">SelectionType</span></span> <br/> | <span data-ttu-id="93639-114">пикконе</span><span class="sxs-lookup"><span data-stu-id="93639-114">PickOne</span></span><br/> <span data-ttu-id="93639-115">пиккмани</span><span class="sxs-lookup"><span data-stu-id="93639-115">PickMany</span></span><br/> | <span data-ttu-id="93639-116">Указывает количество параметров, которые могут быть выбраны для этой функции в определенный момент времени (Пикконе) или несколько (Пиккмани).</span><span class="sxs-lookup"><span data-stu-id="93639-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="93639-117">Клиент может использовать эти сведения для создания PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="93639-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="93639-118">Эта информация влияет на поведение пользовательского интерфейса, а также на проверку PrintTicket поставщиком.</span><span class="sxs-lookup"><span data-stu-id="93639-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="93639-119">Элементы Option могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="93639-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="93639-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="93639-120">Property</span></span>                   | <span data-ttu-id="93639-121">Значения</span><span class="sxs-lookup"><span data-stu-id="93639-121">Values</span></span>                           | <span data-ttu-id="93639-122">Назначение</span><span class="sxs-lookup"><span data-stu-id="93639-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93639-123">идентитйоптион</span><span class="sxs-lookup"><span data-stu-id="93639-123">IdentityOption</span></span> <br/> | <span data-ttu-id="93639-124">True</span><span class="sxs-lookup"><span data-stu-id="93639-124">True</span></span><br/> <span data-ttu-id="93639-125">Неверно</span><span class="sxs-lookup"><span data-stu-id="93639-125">False</span></span><br/> | <span data-ttu-id="93639-126">Выбор свойства Идентитйоптион интерпретируется как "отключить эту функцию".</span><span class="sxs-lookup"><span data-stu-id="93639-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="93639-127">Функция, которая содержит свойство Селектионтипе, значение которого равно Пиккмани, также должно содержать параметр, имеющий свойство Идентитйоптион.</span><span class="sxs-lookup"><span data-stu-id="93639-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="93639-128">Код пользовательского интерфейса (или клиент, создающий PrintTicket) должен отменить выбор любого другого параметра, если выбрано свойство Идентитйоптион.</span><span class="sxs-lookup"><span data-stu-id="93639-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="93639-129">Элементы feature, Option и Параметердеф могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="93639-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="93639-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="93639-130">Property</span></span>              | <span data-ttu-id="93639-131">Значения</span><span class="sxs-lookup"><span data-stu-id="93639-131">Values</span></span>                          | <span data-ttu-id="93639-132">Назначение</span><span class="sxs-lookup"><span data-stu-id="93639-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93639-133">дисплайуи</span><span class="sxs-lookup"><span data-stu-id="93639-133">DisplayUI</span></span> <br/> | <span data-ttu-id="93639-134">Показать</span><span class="sxs-lookup"><span data-stu-id="93639-134">Show</span></span><br/> <span data-ttu-id="93639-135">Скрыть</span><span class="sxs-lookup"><span data-stu-id="93639-135">Hide</span></span><br/> | <span data-ttu-id="93639-136">Указывает, должен ли родительский элемент отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93639-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="93639-137">Показать указывает, что элемент должен отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93639-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="93639-138">Скрыть указывает, что элемент не должен отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93639-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="93639-139">Если это свойство не определено для элемента, то интерпретация по умолчанию показывает, что элемент отображается.</span><span class="sxs-lookup"><span data-stu-id="93639-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="93639-140">Элементы feature, Option и Параметердеф могут содержать следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="93639-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="93639-141">Свойство</span><span class="sxs-lookup"><span data-stu-id="93639-141">Property</span></span>                | <span data-ttu-id="93639-142">Значение</span><span class="sxs-lookup"><span data-stu-id="93639-142">Value</span></span>             | <span data-ttu-id="93639-143">Назначение</span><span class="sxs-lookup"><span data-stu-id="93639-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93639-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="93639-144">DisplayName</span></span> <br/> | <span data-ttu-id="93639-145">Строка</span><span class="sxs-lookup"><span data-stu-id="93639-145">String</span></span><br/> | <span data-ttu-id="93639-146">Задает отображаемую строку для родительского элемента, переопределяя отображаемое имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93639-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="93639-147">Может использоваться поставщиками PrintCapabilities для представления локализованного и понятного отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="93639-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="93639-148">Значение отображаемого имени по умолчанию — это атрибут имени для родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="93639-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="93639-149">В случае использования элементов Option, если атрибут name не указан, должно присутствовать свойство DisplayName.</span><span class="sxs-lookup"><span data-stu-id="93639-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="93639-150">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="93639-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93639-151">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="93639-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




