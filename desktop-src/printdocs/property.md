---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Свойство (документы и печать)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351865"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="3226a-104">Свойство (документы и печать)</span><span class="sxs-lookup"><span data-stu-id="3226a-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="3226a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="3226a-105">This topic is not current.</span></span> <span data-ttu-id="3226a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3226a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3226a-107">Элемент Property объявляет устройство, форматирование задания или другое соответствующее свойство, имя которого задается атрибутом Name.</span><span class="sxs-lookup"><span data-stu-id="3226a-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="3226a-108">Элемент value используется для присвоения значения свойству.</span><span class="sxs-lookup"><span data-stu-id="3226a-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="3226a-109">Свойство может быть сложным, возможно, содержать несколько вложенных свойств.</span><span class="sxs-lookup"><span data-stu-id="3226a-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="3226a-110">Вложенные свойства также представлены элементами свойств.</span><span class="sxs-lookup"><span data-stu-id="3226a-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="3226a-111">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="3226a-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="3226a-112">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="3226a-112">XML Attributes</span></span>

<span data-ttu-id="3226a-113">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="3226a-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="3226a-114">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="3226a-114">XML Attribute</span></span>   | <span data-ttu-id="3226a-115">Сведения</span><span class="sxs-lookup"><span data-stu-id="3226a-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3226a-116">name</span><span class="sxs-lookup"><span data-stu-id="3226a-116">name</span></span><br/> | <span data-ttu-id="3226a-117">Содержит атрибут Name свойства, которое является либо стандартным свойством, либо закрытым свойством.</span><span class="sxs-lookup"><span data-stu-id="3226a-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="3226a-118">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="3226a-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="3226a-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3226a-119">Element Information</span></span>

<span data-ttu-id="3226a-120">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="3226a-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="3226a-121">Категория</span><span class="sxs-lookup"><span data-stu-id="3226a-121">Category</span></span>                   | <span data-ttu-id="3226a-122">Сведения</span><span class="sxs-lookup"><span data-stu-id="3226a-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3226a-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3226a-123">Parent elements</span></span><br/> | <span data-ttu-id="3226a-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="3226a-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="3226a-125">Функция</span><span class="sxs-lookup"><span data-stu-id="3226a-125">Feature</span></span><br/> <span data-ttu-id="3226a-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="3226a-126">PrintTicket</span></span><br/> <span data-ttu-id="3226a-127">Параметр</span><span class="sxs-lookup"><span data-stu-id="3226a-127">Option</span></span><br/> <span data-ttu-id="3226a-128">параметердеф</span><span class="sxs-lookup"><span data-stu-id="3226a-128">ParameterDef</span></span><br/> <span data-ttu-id="3226a-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="3226a-129">Property</span></span><br/> <span data-ttu-id="3226a-130">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="3226a-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="3226a-131">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3226a-131">Child elements</span></span><br/>  | <span data-ttu-id="3226a-132">Система присваивает неважность упорядочивания элементов.</span><span class="sxs-lookup"><span data-stu-id="3226a-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="3226a-133">Если клиенты ascribe некоторую важность в упорядочении элементов, они могут оказаться бесплатными.</span><span class="sxs-lookup"><span data-stu-id="3226a-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="3226a-134">*Значение* *Свойства* (одно или более) (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="3226a-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="3226a-135">или</span><span class="sxs-lookup"><span data-stu-id="3226a-135">or</span></span> <br/> <span data-ttu-id="3226a-136">*Свойство* (ноль или более) (одно или несколько *значений* )</span><span class="sxs-lookup"><span data-stu-id="3226a-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="3226a-137">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="3226a-137">This element</span></span><br/>    | <span data-ttu-id="3226a-138">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="3226a-138">No character data is permitted.</span></span><br/> <span data-ttu-id="3226a-139">Допускаются одинаковые дочерние элементы значений, являющиеся одноуровневыми элементами.</span><span class="sxs-lookup"><span data-stu-id="3226a-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="3226a-140">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="3226a-140">Configuration Dependencies</span></span>

<span data-ttu-id="3226a-141">Свойство может иметь зависимости конфигурации, кроме случаев, когда оно присутствует в элементе Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="3226a-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="3226a-142">Использование элементов</span><span class="sxs-lookup"><span data-stu-id="3226a-142">Element Usage</span></span>

<span data-ttu-id="3226a-143">В дополнение к отображению в элементах Feature и Option, элементы свойств могут отображаться на корневом уровне соответствующих базовых технологий.</span><span class="sxs-lookup"><span data-stu-id="3226a-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="3226a-144">Схема печати определяет набор элементов свойств, которые можно использовать для описания устройства переносимым способом.</span><span class="sxs-lookup"><span data-stu-id="3226a-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="3226a-145">Однако если эти свойства недостаточно для ваших потребностей в качестве поставщика PrintCapabilities (обычно потому, что поддерживаемое устройство имеет романские аспекты, не ожидаемые схемой печати), вы можете ввести собственные закрытые элементы свойств.</span><span class="sxs-lookup"><span data-stu-id="3226a-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="3226a-146">Вы можете усовершенствовать или проанализировать сведения, предоставляемые общедоступным свойством, добавив одно или несколько частных вложенных свойств в качестве содержимого элемента общего свойства.</span><span class="sxs-lookup"><span data-stu-id="3226a-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="3226a-147">Элементы свойств определяются с помощью тега XML-элемента <Property> .</span><span class="sxs-lookup"><span data-stu-id="3226a-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="3226a-148">Каждому свойству присваивается имя с помощью его атрибута Name.</span><span class="sxs-lookup"><span data-stu-id="3226a-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="3226a-149">Имя должно быть типа QName XML и должно соответствовать соглашению о пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="3226a-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="3226a-150">Дополнительные сведения см. в разделе [атрибуты XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3226a-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="3226a-151">Атрибут имени свойства и его расположение в иерархии родительских элементов свойств (если оно является подсвойством) уникально идентифицируют свойство в документе PrintCapabilities или PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="3226a-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="3226a-152">Свойство может содержать один или несколько элементов значения или один или несколько дочерних элементов свойств (называемых вложенными свойствами) или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="3226a-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="3226a-153">Подсвойства полезны, если само свойство состоит из нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="3226a-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="3226a-154">Например, свойство "Консумаблеколор" может иметь компоненты "C", "M" и "Y".</span><span class="sxs-lookup"><span data-stu-id="3226a-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="3226a-155">Пример</span><span class="sxs-lookup"><span data-stu-id="3226a-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="3226a-156">См. также</span><span class="sxs-lookup"><span data-stu-id="3226a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3226a-157">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="3226a-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




