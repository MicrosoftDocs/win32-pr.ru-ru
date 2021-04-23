---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: пажеватермаркоригинхеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d3e12591f6c648e6e636e1bb72f4df694d0d13
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104000023"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="6ceec-104">пажеватермаркоригинхеигхт</span><span class="sxs-lookup"><span data-stu-id="6ceec-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="6ceec-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="6ceec-105">This topic is not current.</span></span> <span data-ttu-id="6ceec-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6ceec-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ceec-107">Задает источник водяного знака относительно источника Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="6ceec-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="6ceec-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6ceec-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6ceec-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="6ceec-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6ceec-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6ceec-110">Element Information</span></span>



| <span data-ttu-id="6ceec-111">Имя</span><span class="sxs-lookup"><span data-stu-id="6ceec-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="6ceec-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="6ceec-112">Element Type</span></span> <br/>   | <span data-ttu-id="6ceec-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="6ceec-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="6ceec-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="6ceec-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6ceec-115">Страница</span><span class="sxs-lookup"><span data-stu-id="6ceec-115">Page</span></span><br/>                            |
| <span data-ttu-id="6ceec-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ceec-116">Notes</span></span> <br/>          | <span data-ttu-id="6ceec-117">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="6ceec-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6ceec-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="6ceec-118">Structure Content</span></span>

<span data-ttu-id="6ceec-119">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ceec-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="6ceec-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="6ceec-120">Structure Properties</span></span>

<span data-ttu-id="6ceec-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="6ceec-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6ceec-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ceec-122">Property</span></span>                | <span data-ttu-id="6ceec-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6ceec-123">xsi:type</span></span>           | <span data-ttu-id="6ceec-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceec-124">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6ceec-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6ceec-125">DataType</span></span><br/>     | <span data-ttu-id="6ceec-126">строка</span><span class="sxs-lookup"><span data-stu-id="6ceec-126">string</span></span><br/>  | <span data-ttu-id="6ceec-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6ceec-127">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="6ceec-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6ceec-128">DefaultValue</span></span><br/> | <span data-ttu-id="6ceec-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="6ceec-129">integer</span></span><br/> | <span data-ttu-id="6ceec-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="6ceec-130">undefined</span></span><br/>                                                    |
| <span data-ttu-id="6ceec-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6ceec-131">MaxValue</span></span><br/>     | <span data-ttu-id="6ceec-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="6ceec-132">integer</span></span><br/> | <span data-ttu-id="6ceec-133">Меньше или равно Пажеимажеаблесизе-Екстенсеигхт значение</span><span class="sxs-lookup"><span data-stu-id="6ceec-133">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="6ceec-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="6ceec-134">MinValue</span></span><br/>     | <span data-ttu-id="6ceec-135">целое число</span><span class="sxs-lookup"><span data-stu-id="6ceec-135">integer</span></span><br/> | <span data-ttu-id="6ceec-136">0</span><span class="sxs-lookup"><span data-stu-id="6ceec-136">0</span></span><br/>                                                            |
| <span data-ttu-id="6ceec-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="6ceec-137">Multiple</span></span><br/>     | <span data-ttu-id="6ceec-138">целое число</span><span class="sxs-lookup"><span data-stu-id="6ceec-138">integer</span></span><br/> | <span data-ttu-id="6ceec-139">1</span><span class="sxs-lookup"><span data-stu-id="6ceec-139">1</span></span><br/>                                                            |
| <span data-ttu-id="6ceec-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6ceec-140">Mandatory</span></span><br/>    | <span data-ttu-id="6ceec-141">строка</span><span class="sxs-lookup"><span data-stu-id="6ceec-141">string</span></span><br/>  | <span data-ttu-id="6ceec-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="6ceec-142">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="6ceec-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="6ceec-143">UnitType</span></span><br/>     | <span data-ttu-id="6ceec-144">строка</span><span class="sxs-lookup"><span data-stu-id="6ceec-144">string</span></span><br/>  | <span data-ttu-id="6ceec-145">мкм</span><span class="sxs-lookup"><span data-stu-id="6ceec-145">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6ceec-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6ceec-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ceec-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="6ceec-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




