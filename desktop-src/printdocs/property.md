---
description: Сведения об элементе Property в документах и печати. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Свойство (документы и печать)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120299"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="0e787-105">Свойство (документы и печать)</span><span class="sxs-lookup"><span data-stu-id="0e787-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="0e787-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0e787-106">This topic is not current.</span></span> <span data-ttu-id="0e787-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e787-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e787-108">Элемент Property объявляет устройство, форматирование задания или другое соответствующее свойство, имя которого задается атрибутом Name.</span><span class="sxs-lookup"><span data-stu-id="0e787-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="0e787-109">Элемент value используется для присвоения значения свойству.</span><span class="sxs-lookup"><span data-stu-id="0e787-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="0e787-110">Свойство может быть сложным, возможно, содержать несколько вложенных свойств.</span><span class="sxs-lookup"><span data-stu-id="0e787-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="0e787-111">Вложенные свойства также представлены элементами свойств.</span><span class="sxs-lookup"><span data-stu-id="0e787-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="0e787-112">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="0e787-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="0e787-113">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="0e787-113">XML Attributes</span></span>

<span data-ttu-id="0e787-114">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="0e787-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="0e787-115">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="0e787-115">XML Attribute</span></span>   | <span data-ttu-id="0e787-116">Сведения</span><span class="sxs-lookup"><span data-stu-id="0e787-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e787-117">name</span><span class="sxs-lookup"><span data-stu-id="0e787-117">name</span></span><br/> | <span data-ttu-id="0e787-118">Содержит атрибут Name свойства, которое является либо стандартным свойством, либо закрытым свойством.</span><span class="sxs-lookup"><span data-stu-id="0e787-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="0e787-119">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="0e787-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="0e787-120">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0e787-120">Element Information</span></span>

<span data-ttu-id="0e787-121">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="0e787-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="0e787-122">Категория</span><span class="sxs-lookup"><span data-stu-id="0e787-122">Category</span></span>                   | <span data-ttu-id="0e787-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="0e787-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e787-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0e787-124">Parent elements</span></span><br/> | <span data-ttu-id="0e787-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="0e787-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="0e787-126">Компонент</span><span class="sxs-lookup"><span data-stu-id="0e787-126">Feature</span></span><br/> <span data-ttu-id="0e787-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="0e787-127">PrintTicket</span></span><br/> <span data-ttu-id="0e787-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="0e787-128">Option</span></span><br/> <span data-ttu-id="0e787-129">параметердеф</span><span class="sxs-lookup"><span data-stu-id="0e787-129">ParameterDef</span></span><br/> <span data-ttu-id="0e787-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="0e787-130">Property</span></span><br/> <span data-ttu-id="0e787-131">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="0e787-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="0e787-132">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0e787-132">Child elements</span></span><br/>  | <span data-ttu-id="0e787-133">Система присваивает неважность упорядочивания элементов.</span><span class="sxs-lookup"><span data-stu-id="0e787-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="0e787-134">Если клиенты ascribe некоторую важность в упорядочении элементов, они могут оказаться бесплатными.</span><span class="sxs-lookup"><span data-stu-id="0e787-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="0e787-135">*Значение* *Свойства* (одно или более) (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="0e787-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="0e787-136">или</span><span class="sxs-lookup"><span data-stu-id="0e787-136">or</span></span> <br/> <span data-ttu-id="0e787-137">*Свойство* (ноль или более) (одно или несколько *значений* )</span><span class="sxs-lookup"><span data-stu-id="0e787-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="0e787-138">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="0e787-138">This element</span></span><br/>    | <span data-ttu-id="0e787-139">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="0e787-139">No character data is permitted.</span></span><br/> <span data-ttu-id="0e787-140">Допускаются одинаковые дочерние элементы значений, являющиеся одноуровневыми элементами.</span><span class="sxs-lookup"><span data-stu-id="0e787-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="0e787-141">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="0e787-141">Configuration Dependencies</span></span>

<span data-ttu-id="0e787-142">Свойство может иметь зависимости конфигурации, кроме случаев, когда оно присутствует в элементе Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="0e787-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="0e787-143">Использование элементов</span><span class="sxs-lookup"><span data-stu-id="0e787-143">Element Usage</span></span>

<span data-ttu-id="0e787-144">В дополнение к отображению в элементах Feature и Option, элементы свойств могут отображаться на корневом уровне соответствующих базовых технологий.</span><span class="sxs-lookup"><span data-stu-id="0e787-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="0e787-145">Схема печати определяет набор элементов свойств, которые можно использовать для описания устройства переносимым способом.</span><span class="sxs-lookup"><span data-stu-id="0e787-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="0e787-146">Однако если эти свойства недостаточно для ваших потребностей в качестве поставщика PrintCapabilities (обычно потому, что поддерживаемое устройство имеет романские аспекты, не ожидаемые схемой печати), вы можете ввести собственные закрытые элементы свойств.</span><span class="sxs-lookup"><span data-stu-id="0e787-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="0e787-147">Вы можете усовершенствовать или проанализировать сведения, предоставляемые общедоступным свойством, добавив одно или несколько частных вложенных свойств в качестве содержимого элемента общего свойства.</span><span class="sxs-lookup"><span data-stu-id="0e787-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="0e787-148">Элементы свойств определяются с помощью тега XML-элемента <Property> .</span><span class="sxs-lookup"><span data-stu-id="0e787-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="0e787-149">Каждому свойству присваивается имя с помощью его атрибута Name.</span><span class="sxs-lookup"><span data-stu-id="0e787-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="0e787-150">Имя должно быть типа QName XML и должно соответствовать соглашению о пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0e787-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="0e787-151">Дополнительные сведения см. в разделе [атрибуты XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0e787-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="0e787-152">Атрибут имени свойства и его расположение в иерархии родительских элементов свойств (если оно является подсвойством) уникально идентифицируют свойство в документе PrintCapabilities или PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0e787-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="0e787-153">Свойство может содержать один или несколько элементов значения или один или несколько дочерних элементов свойств (называемых вложенными свойствами) или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="0e787-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="0e787-154">Подсвойства полезны, если само свойство состоит из нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="0e787-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="0e787-155">Например, свойство "Консумаблеколор" может иметь компоненты "C", "M" и "Y".</span><span class="sxs-lookup"><span data-stu-id="0e787-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="0e787-156">Пример</span><span class="sxs-lookup"><span data-stu-id="0e787-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="0e787-157">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0e787-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e787-158">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0e787-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




