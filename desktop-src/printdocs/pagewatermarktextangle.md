---
description: Получите дополнительные сведения о параметре Пажеватермарктекстангле. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: пажеватермарктекстангле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395979"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="e1478-105">пажеватермарктекстангле</span><span class="sxs-lookup"><span data-stu-id="e1478-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="e1478-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e1478-106">This topic is not current.</span></span> <span data-ttu-id="e1478-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e1478-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e1478-108">Задает угол текста водяного знака относительно направления Пажеимажеаблесизевидс.</span><span class="sxs-lookup"><span data-stu-id="e1478-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="e1478-109">Угол измеряется в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="e1478-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="e1478-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1478-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e1478-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e1478-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e1478-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1478-112">Element Information</span></span>



| <span data-ttu-id="e1478-113">Имя</span><span class="sxs-lookup"><span data-stu-id="e1478-113">Name</span></span> | <span data-ttu-id="e1478-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e1478-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="e1478-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e1478-115">Element Type</span></span> <br/>   | <span data-ttu-id="e1478-116">параметердеф</span><span class="sxs-lookup"><span data-stu-id="e1478-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="e1478-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e1478-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e1478-118">Страница</span><span class="sxs-lookup"><span data-stu-id="e1478-118">Page</span></span><br/>                            |
| <span data-ttu-id="e1478-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1478-119">Notes</span></span> <br/>          | <span data-ttu-id="e1478-120">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="e1478-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e1478-121">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e1478-121">Structure Content</span></span>

<span data-ttu-id="e1478-122">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e1478-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e1478-123">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="e1478-123">Structure Properties</span></span>

<span data-ttu-id="e1478-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e1478-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e1478-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="e1478-125">Property</span></span>                | <span data-ttu-id="e1478-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e1478-126">xsi:type</span></span>           | <span data-ttu-id="e1478-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e1478-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e1478-128">DataType</span><span class="sxs-lookup"><span data-stu-id="e1478-128">DataType</span></span><br/>     | <span data-ttu-id="e1478-129">строка</span><span class="sxs-lookup"><span data-stu-id="e1478-129">string</span></span><br/>  | <span data-ttu-id="e1478-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e1478-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="e1478-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e1478-131">DefaultValue</span></span><br/> | <span data-ttu-id="e1478-132">целое число</span><span class="sxs-lookup"><span data-stu-id="e1478-132">integer</span></span><br/> | <span data-ttu-id="e1478-133">0</span><span class="sxs-lookup"><span data-stu-id="e1478-133">0</span></span><br/>               |
| <span data-ttu-id="e1478-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e1478-134">MaxValue</span></span><br/>     | <span data-ttu-id="e1478-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="e1478-135">integer</span></span><br/> | <span data-ttu-id="e1478-136">359</span><span class="sxs-lookup"><span data-stu-id="e1478-136">359</span></span><br/>             |
| <span data-ttu-id="e1478-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="e1478-137">MinValue</span></span><br/>     | <span data-ttu-id="e1478-138">целое число</span><span class="sxs-lookup"><span data-stu-id="e1478-138">integer</span></span><br/> | <span data-ttu-id="e1478-139">0</span><span class="sxs-lookup"><span data-stu-id="e1478-139">0</span></span><br/>               |
| <span data-ttu-id="e1478-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="e1478-140">Multiple</span></span><br/>     | <span data-ttu-id="e1478-141">целое число</span><span class="sxs-lookup"><span data-stu-id="e1478-141">integer</span></span><br/> | <span data-ttu-id="e1478-142">1</span><span class="sxs-lookup"><span data-stu-id="e1478-142">1</span></span><br/>               |
| <span data-ttu-id="e1478-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1478-143">Mandatory</span></span><br/>    | <span data-ttu-id="e1478-144">строка</span><span class="sxs-lookup"><span data-stu-id="e1478-144">string</span></span><br/>  | <span data-ttu-id="e1478-145">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="e1478-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e1478-146">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="e1478-146">UnitType</span></span><br/>     | <span data-ttu-id="e1478-147">строка</span><span class="sxs-lookup"><span data-stu-id="e1478-147">string</span></span><br/>  | <span data-ttu-id="e1478-148">градусы</span><span class="sxs-lookup"><span data-stu-id="e1478-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e1478-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e1478-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1478-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e1478-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




