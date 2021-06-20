---
description: Сведения об элементе Параметердеф, который определяет допустимые характеристики входных параметров. Значение вводится с помощью элемента Параметеринит.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: параметердеф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2682e3da11f471401e95e3f6515de5e18b6be895
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407297"
---
# <a name="parameterdef"></a><span data-ttu-id="99e87-104">параметердеф</span><span class="sxs-lookup"><span data-stu-id="99e87-104">ParameterDef</span></span>

<span data-ttu-id="99e87-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="99e87-105">This topic is not current.</span></span> <span data-ttu-id="99e87-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="99e87-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="99e87-107">Элемент Параметердеф определяет допустимые характеристики входных параметров.</span><span class="sxs-lookup"><span data-stu-id="99e87-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="99e87-108">Значение вводится с помощью элемента Параметеринит.</span><span class="sxs-lookup"><span data-stu-id="99e87-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="99e87-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="99e87-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="99e87-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="99e87-110">XML Attributes</span></span>

<span data-ttu-id="99e87-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="99e87-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="99e87-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="99e87-112">XML Attribute</span></span>   | <span data-ttu-id="99e87-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="99e87-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e87-114">name</span><span class="sxs-lookup"><span data-stu-id="99e87-114">name</span></span><br/> | <span data-ttu-id="99e87-115">Определяет уникальное имя для параметра в контексте текущего документа.</span><span class="sxs-lookup"><span data-stu-id="99e87-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="99e87-116">Дублирующиеся атрибуты имени Параметердеф отображают недопустимый документ PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="99e87-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="99e87-117">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="99e87-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="99e87-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="99e87-118">Element Information</span></span>

<span data-ttu-id="99e87-119">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="99e87-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99e87-120">Категория</span><span class="sxs-lookup"><span data-stu-id="99e87-120">Category</span></span></th>
<th><span data-ttu-id="99e87-121">Сведения</span><span class="sxs-lookup"><span data-stu-id="99e87-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99e87-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="99e87-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="99e87-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="99e87-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99e87-124">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="99e87-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="99e87-125">Property (один или больше)</span><span class="sxs-lookup"><span data-stu-id="99e87-125">Property (one or more)</span></span><br/> <span data-ttu-id="99e87-126">Следующие стандартные элементы свойств должны отображаться как содержимое элемента Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="99e87-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="99e87-127">DataType</span><span class="sxs-lookup"><span data-stu-id="99e87-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="99e87-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="99e87-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="99e87-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="99e87-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="99e87-130">MaxLength или MaxValue</span><span class="sxs-lookup"><span data-stu-id="99e87-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="99e87-131">MinLength или MinValue</span><span class="sxs-lookup"><span data-stu-id="99e87-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="99e87-132">Несколько</span><span class="sxs-lookup"><span data-stu-id="99e87-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="99e87-133">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="99e87-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99e87-134">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="99e87-134">This element</span></span><br/></td>
<td><span data-ttu-id="99e87-135">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="99e87-135">No character data is permitted.</span></span><br/> <span data-ttu-id="99e87-136">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="99e87-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="99e87-137">\*Требуется, если DataType имеет тип Integer или Decimal.</span><span class="sxs-lookup"><span data-stu-id="99e87-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="99e87-138">Необязательный аргумент, если DataType является строковым.</span><span class="sxs-lookup"><span data-stu-id="99e87-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="99e87-139">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="99e87-139">Configuration Dependencies</span></span>

<span data-ttu-id="99e87-140">Параметердеф и его содержимое с любым уровнем вложенности может не иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="99e87-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="99e87-141">Пример</span><span class="sxs-lookup"><span data-stu-id="99e87-141">Example</span></span>

<span data-ttu-id="99e87-142">В следующем примере задаются все обязательные элементы свойств для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="99e87-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="99e87-143">В примере в [параметеринит](parameterinit.md) показано, как инициализировать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="99e87-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="99e87-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="99e87-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99e87-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="99e87-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




