---
description: Получение сведений о параметре Пажемедиасизепсвидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: пажемедиасизепсвидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe678107d2a183ee0f0bf6ce290dfe230fa8cc2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395649"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="76ea6-105">пажемедиасизепсвидс</span><span class="sxs-lookup"><span data-stu-id="76ea6-105">PageMediaSizePSWidth</span></span>

<span data-ttu-id="76ea6-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="76ea6-106">This topic is not current.</span></span> <span data-ttu-id="76ea6-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="76ea6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="76ea6-108">Задает ширину страницы, перпендикулярной направлению ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="76ea6-108">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="76ea6-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="76ea6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="76ea6-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="76ea6-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="76ea6-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="76ea6-111">Element Information</span></span>



| <span data-ttu-id="76ea6-112">Имя</span><span class="sxs-lookup"><span data-stu-id="76ea6-112">Name</span></span> | <span data-ttu-id="76ea6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="76ea6-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="76ea6-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="76ea6-114">Element Type</span></span> <br/>   | <span data-ttu-id="76ea6-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="76ea6-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="76ea6-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="76ea6-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="76ea6-117">Страница</span><span class="sxs-lookup"><span data-stu-id="76ea6-117">Page</span></span><br/>                                             |
| <span data-ttu-id="76ea6-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="76ea6-118">Notes</span></span> <br/>          | <span data-ttu-id="76ea6-119">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="76ea6-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="76ea6-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="76ea6-120">Structure Content</span></span>

<span data-ttu-id="76ea6-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="76ea6-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="76ea6-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="76ea6-122">Structure Properties</span></span>

<span data-ttu-id="76ea6-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="76ea6-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="76ea6-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="76ea6-124">Property</span></span>                | <span data-ttu-id="76ea6-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="76ea6-125">xsi:type</span></span>           | <span data-ttu-id="76ea6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="76ea6-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="76ea6-127">DataType</span><span class="sxs-lookup"><span data-stu-id="76ea6-127">DataType</span></span><br/>     | <span data-ttu-id="76ea6-128">строка</span><span class="sxs-lookup"><span data-stu-id="76ea6-128">string</span></span><br/>  | <span data-ttu-id="76ea6-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="76ea6-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="76ea6-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="76ea6-130">DefaultValue</span></span><br/> | <span data-ttu-id="76ea6-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="76ea6-131">integer</span></span><br/> | <span data-ttu-id="76ea6-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="76ea6-132">undefined</span></span><br/>       |
| <span data-ttu-id="76ea6-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="76ea6-133">MaxValue</span></span><br/>     | <span data-ttu-id="76ea6-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="76ea6-134">integer</span></span><br/> | <span data-ttu-id="76ea6-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="76ea6-135">undefined</span></span><br/>       |
| <span data-ttu-id="76ea6-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="76ea6-136">MinValue</span></span><br/>     | <span data-ttu-id="76ea6-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="76ea6-137">integer</span></span><br/> | <span data-ttu-id="76ea6-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="76ea6-138">undefined</span></span><br/>       |
| <span data-ttu-id="76ea6-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76ea6-139">Mandatory</span></span><br/>    | <span data-ttu-id="76ea6-140">строка</span><span class="sxs-lookup"><span data-stu-id="76ea6-140">string</span></span><br/>  | <span data-ttu-id="76ea6-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="76ea6-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="76ea6-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="76ea6-142">Multiple</span></span><br/>     | <span data-ttu-id="76ea6-143">целое число</span><span class="sxs-lookup"><span data-stu-id="76ea6-143">integer</span></span><br/> | <span data-ttu-id="76ea6-144">1</span><span class="sxs-lookup"><span data-stu-id="76ea6-144">1</span></span><br/>               |
| <span data-ttu-id="76ea6-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="76ea6-145">UnitType</span></span><br/>     | <span data-ttu-id="76ea6-146">строка</span><span class="sxs-lookup"><span data-stu-id="76ea6-146">string</span></span><br/>  | <span data-ttu-id="76ea6-147">мкм</span><span class="sxs-lookup"><span data-stu-id="76ea6-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="76ea6-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="76ea6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ea6-149">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="76ea6-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="76ea6-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="76ea6-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




