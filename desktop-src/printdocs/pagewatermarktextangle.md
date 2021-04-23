---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: пажеватермарктекстангле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916e409040f0c7163f1168d48581270f077aaa3a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273340"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="884aa-104">пажеватермарктекстангле</span><span class="sxs-lookup"><span data-stu-id="884aa-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="884aa-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="884aa-105">This topic is not current.</span></span> <span data-ttu-id="884aa-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="884aa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="884aa-107">Задает угол текста водяного знака относительно направления Пажеимажеаблесизевидс.</span><span class="sxs-lookup"><span data-stu-id="884aa-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="884aa-108">Угол измеряется в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="884aa-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="884aa-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="884aa-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="884aa-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="884aa-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="884aa-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="884aa-111">Element Information</span></span>



| <span data-ttu-id="884aa-112">Имя</span><span class="sxs-lookup"><span data-stu-id="884aa-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="884aa-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="884aa-113">Element Type</span></span> <br/>   | <span data-ttu-id="884aa-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="884aa-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="884aa-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="884aa-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="884aa-116">Страница</span><span class="sxs-lookup"><span data-stu-id="884aa-116">Page</span></span><br/>                            |
| <span data-ttu-id="884aa-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="884aa-117">Notes</span></span> <br/>          | <span data-ttu-id="884aa-118">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="884aa-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="884aa-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="884aa-119">Structure Content</span></span>

<span data-ttu-id="884aa-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="884aa-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="884aa-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="884aa-121">Structure Properties</span></span>

<span data-ttu-id="884aa-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="884aa-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="884aa-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="884aa-123">Property</span></span>                | <span data-ttu-id="884aa-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="884aa-124">xsi:type</span></span>           | <span data-ttu-id="884aa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="884aa-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="884aa-126">DataType</span><span class="sxs-lookup"><span data-stu-id="884aa-126">DataType</span></span><br/>     | <span data-ttu-id="884aa-127">строка</span><span class="sxs-lookup"><span data-stu-id="884aa-127">string</span></span><br/>  | <span data-ttu-id="884aa-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="884aa-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="884aa-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="884aa-129">DefaultValue</span></span><br/> | <span data-ttu-id="884aa-130">целое число</span><span class="sxs-lookup"><span data-stu-id="884aa-130">integer</span></span><br/> | <span data-ttu-id="884aa-131">0</span><span class="sxs-lookup"><span data-stu-id="884aa-131">0</span></span><br/>               |
| <span data-ttu-id="884aa-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="884aa-132">MaxValue</span></span><br/>     | <span data-ttu-id="884aa-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="884aa-133">integer</span></span><br/> | <span data-ttu-id="884aa-134">359</span><span class="sxs-lookup"><span data-stu-id="884aa-134">359</span></span><br/>             |
| <span data-ttu-id="884aa-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="884aa-135">MinValue</span></span><br/>     | <span data-ttu-id="884aa-136">целое число</span><span class="sxs-lookup"><span data-stu-id="884aa-136">integer</span></span><br/> | <span data-ttu-id="884aa-137">0</span><span class="sxs-lookup"><span data-stu-id="884aa-137">0</span></span><br/>               |
| <span data-ttu-id="884aa-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="884aa-138">Multiple</span></span><br/>     | <span data-ttu-id="884aa-139">целое число</span><span class="sxs-lookup"><span data-stu-id="884aa-139">integer</span></span><br/> | <span data-ttu-id="884aa-140">1</span><span class="sxs-lookup"><span data-stu-id="884aa-140">1</span></span><br/>               |
| <span data-ttu-id="884aa-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="884aa-141">Mandatory</span></span><br/>    | <span data-ttu-id="884aa-142">строка</span><span class="sxs-lookup"><span data-stu-id="884aa-142">string</span></span><br/>  | <span data-ttu-id="884aa-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="884aa-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="884aa-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="884aa-144">UnitType</span></span><br/>     | <span data-ttu-id="884aa-145">строка</span><span class="sxs-lookup"><span data-stu-id="884aa-145">string</span></span><br/>  | <span data-ttu-id="884aa-146">градусы</span><span class="sxs-lookup"><span data-stu-id="884aa-146">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="884aa-147">См. также</span><span class="sxs-lookup"><span data-stu-id="884aa-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="884aa-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="884aa-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




