---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: пажемедиасизепсвидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4399b75f047c2705983c893075995800396120
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997551"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="94a74-104">пажемедиасизепсвидс</span><span class="sxs-lookup"><span data-stu-id="94a74-104">PageMediaSizePSWidth</span></span>

<span data-ttu-id="94a74-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="94a74-105">This topic is not current.</span></span> <span data-ttu-id="94a74-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="94a74-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="94a74-107">Задает ширину страницы, перпендикулярной направлению ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="94a74-107">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="94a74-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="94a74-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="94a74-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="94a74-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="94a74-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="94a74-110">Element Information</span></span>



| <span data-ttu-id="94a74-111">Имя</span><span class="sxs-lookup"><span data-stu-id="94a74-111">Name</span></span> | <span data-ttu-id="94a74-112">Значение</span><span class="sxs-lookup"><span data-stu-id="94a74-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="94a74-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="94a74-113">Element Type</span></span> <br/>   | <span data-ttu-id="94a74-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="94a74-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="94a74-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="94a74-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="94a74-116">Страница</span><span class="sxs-lookup"><span data-stu-id="94a74-116">Page</span></span><br/>                                             |
| <span data-ttu-id="94a74-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="94a74-117">Notes</span></span> <br/>          | <span data-ttu-id="94a74-118">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="94a74-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="94a74-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="94a74-119">Structure Content</span></span>

<span data-ttu-id="94a74-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="94a74-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="94a74-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="94a74-121">Structure Properties</span></span>

<span data-ttu-id="94a74-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="94a74-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="94a74-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="94a74-123">Property</span></span>                | <span data-ttu-id="94a74-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="94a74-124">xsi:type</span></span>           | <span data-ttu-id="94a74-125">Значение</span><span class="sxs-lookup"><span data-stu-id="94a74-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="94a74-126">DataType</span><span class="sxs-lookup"><span data-stu-id="94a74-126">DataType</span></span><br/>     | <span data-ttu-id="94a74-127">строка</span><span class="sxs-lookup"><span data-stu-id="94a74-127">string</span></span><br/>  | <span data-ttu-id="94a74-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94a74-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="94a74-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="94a74-129">DefaultValue</span></span><br/> | <span data-ttu-id="94a74-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="94a74-130">integer</span></span><br/> | <span data-ttu-id="94a74-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="94a74-131">undefined</span></span><br/>       |
| <span data-ttu-id="94a74-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="94a74-132">MaxValue</span></span><br/>     | <span data-ttu-id="94a74-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="94a74-133">integer</span></span><br/> | <span data-ttu-id="94a74-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="94a74-134">undefined</span></span><br/>       |
| <span data-ttu-id="94a74-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="94a74-135">MinValue</span></span><br/>     | <span data-ttu-id="94a74-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="94a74-136">integer</span></span><br/> | <span data-ttu-id="94a74-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="94a74-137">undefined</span></span><br/>       |
| <span data-ttu-id="94a74-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94a74-138">Mandatory</span></span><br/>    | <span data-ttu-id="94a74-139">строка</span><span class="sxs-lookup"><span data-stu-id="94a74-139">string</span></span><br/>  | <span data-ttu-id="94a74-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="94a74-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="94a74-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="94a74-141">Multiple</span></span><br/>     | <span data-ttu-id="94a74-142">целое число</span><span class="sxs-lookup"><span data-stu-id="94a74-142">integer</span></span><br/> | <span data-ttu-id="94a74-143">1</span><span class="sxs-lookup"><span data-stu-id="94a74-143">1</span></span><br/>               |
| <span data-ttu-id="94a74-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="94a74-144">UnitType</span></span><br/>     | <span data-ttu-id="94a74-145">строка</span><span class="sxs-lookup"><span data-stu-id="94a74-145">string</span></span><br/>  | <span data-ttu-id="94a74-146">мкм</span><span class="sxs-lookup"><span data-stu-id="94a74-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="94a74-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="94a74-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a74-148">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="94a74-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="94a74-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="94a74-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




