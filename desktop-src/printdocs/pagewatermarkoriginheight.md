---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: пажеватермаркоригинхеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90736f8cac9c919f9d640ffc01311024ef79bc3a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994496"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="68226-104">пажеватермаркоригинхеигхт</span><span class="sxs-lookup"><span data-stu-id="68226-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="68226-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="68226-105">This topic is not current.</span></span> <span data-ttu-id="68226-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="68226-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="68226-107">Задает источник водяного знака относительно источника Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="68226-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="68226-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="68226-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="68226-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="68226-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="68226-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="68226-110">Element Information</span></span>



| <span data-ttu-id="68226-111">Имя</span><span class="sxs-lookup"><span data-stu-id="68226-111">Name</span></span> | <span data-ttu-id="68226-112">Значение</span><span class="sxs-lookup"><span data-stu-id="68226-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="68226-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="68226-113">Element Type</span></span> <br/>   | <span data-ttu-id="68226-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="68226-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="68226-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="68226-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="68226-116">Страница</span><span class="sxs-lookup"><span data-stu-id="68226-116">Page</span></span><br/>                            |
| <span data-ttu-id="68226-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="68226-117">Notes</span></span> <br/>          | <span data-ttu-id="68226-118">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="68226-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="68226-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="68226-119">Structure Content</span></span>

<span data-ttu-id="68226-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="68226-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="68226-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="68226-121">Structure Properties</span></span>

<span data-ttu-id="68226-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="68226-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="68226-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="68226-123">Property</span></span>                | <span data-ttu-id="68226-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="68226-124">xsi:type</span></span>           | <span data-ttu-id="68226-125">Значение</span><span class="sxs-lookup"><span data-stu-id="68226-125">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="68226-126">DataType</span><span class="sxs-lookup"><span data-stu-id="68226-126">DataType</span></span><br/>     | <span data-ttu-id="68226-127">строка</span><span class="sxs-lookup"><span data-stu-id="68226-127">string</span></span><br/>  | <span data-ttu-id="68226-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="68226-128">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="68226-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="68226-129">DefaultValue</span></span><br/> | <span data-ttu-id="68226-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="68226-130">integer</span></span><br/> | <span data-ttu-id="68226-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="68226-131">undefined</span></span><br/>                                                    |
| <span data-ttu-id="68226-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="68226-132">MaxValue</span></span><br/>     | <span data-ttu-id="68226-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="68226-133">integer</span></span><br/> | <span data-ttu-id="68226-134">Меньше или равно Пажеимажеаблесизе-Екстенсеигхт значение</span><span class="sxs-lookup"><span data-stu-id="68226-134">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="68226-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="68226-135">MinValue</span></span><br/>     | <span data-ttu-id="68226-136">целое число</span><span class="sxs-lookup"><span data-stu-id="68226-136">integer</span></span><br/> | <span data-ttu-id="68226-137">0</span><span class="sxs-lookup"><span data-stu-id="68226-137">0</span></span><br/>                                                            |
| <span data-ttu-id="68226-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="68226-138">Multiple</span></span><br/>     | <span data-ttu-id="68226-139">целое число</span><span class="sxs-lookup"><span data-stu-id="68226-139">integer</span></span><br/> | <span data-ttu-id="68226-140">1</span><span class="sxs-lookup"><span data-stu-id="68226-140">1</span></span><br/>                                                            |
| <span data-ttu-id="68226-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="68226-141">Mandatory</span></span><br/>    | <span data-ttu-id="68226-142">строка</span><span class="sxs-lookup"><span data-stu-id="68226-142">string</span></span><br/>  | <span data-ttu-id="68226-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="68226-143">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="68226-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="68226-144">UnitType</span></span><br/>     | <span data-ttu-id="68226-145">строка</span><span class="sxs-lookup"><span data-stu-id="68226-145">string</span></span><br/>  | <span data-ttu-id="68226-146">мкм</span><span class="sxs-lookup"><span data-stu-id="68226-146">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="68226-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="68226-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68226-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="68226-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




