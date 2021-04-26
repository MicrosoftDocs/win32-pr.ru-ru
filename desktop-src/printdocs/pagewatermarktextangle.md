---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: пажеватермарктекстангле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995551"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="fbc5e-104">пажеватермарктекстангле</span><span class="sxs-lookup"><span data-stu-id="fbc5e-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="fbc5e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="fbc5e-105">This topic is not current.</span></span> <span data-ttu-id="fbc5e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fbc5e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fbc5e-107">Задает угол текста водяного знака относительно направления Пажеимажеаблесизевидс.</span><span class="sxs-lookup"><span data-stu-id="fbc5e-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="fbc5e-108">Угол измеряется в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="fbc5e-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="fbc5e-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fbc5e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fbc5e-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="fbc5e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fbc5e-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fbc5e-111">Element Information</span></span>



| <span data-ttu-id="fbc5e-112">Имя</span><span class="sxs-lookup"><span data-stu-id="fbc5e-112">Name</span></span> | <span data-ttu-id="fbc5e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fbc5e-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="fbc5e-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="fbc5e-114">Element Type</span></span> <br/>   | <span data-ttu-id="fbc5e-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="fbc5e-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="fbc5e-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="fbc5e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fbc5e-117">Страница</span><span class="sxs-lookup"><span data-stu-id="fbc5e-117">Page</span></span><br/>                            |
| <span data-ttu-id="fbc5e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbc5e-118">Notes</span></span> <br/>          | <span data-ttu-id="fbc5e-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="fbc5e-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fbc5e-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="fbc5e-120">Structure Content</span></span>

<span data-ttu-id="fbc5e-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fbc5e-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fbc5e-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="fbc5e-122">Structure Properties</span></span>

<span data-ttu-id="fbc5e-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="fbc5e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fbc5e-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="fbc5e-124">Property</span></span>                | <span data-ttu-id="fbc5e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fbc5e-125">xsi:type</span></span>           | <span data-ttu-id="fbc5e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="fbc5e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fbc5e-127">DataType</span><span class="sxs-lookup"><span data-stu-id="fbc5e-127">DataType</span></span><br/>     | <span data-ttu-id="fbc5e-128">строка</span><span class="sxs-lookup"><span data-stu-id="fbc5e-128">string</span></span><br/>  | <span data-ttu-id="fbc5e-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fbc5e-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="fbc5e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fbc5e-130">DefaultValue</span></span><br/> | <span data-ttu-id="fbc5e-131">целое число</span><span class="sxs-lookup"><span data-stu-id="fbc5e-131">integer</span></span><br/> | <span data-ttu-id="fbc5e-132">0</span><span class="sxs-lookup"><span data-stu-id="fbc5e-132">0</span></span><br/>               |
| <span data-ttu-id="fbc5e-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fbc5e-133">MaxValue</span></span><br/>     | <span data-ttu-id="fbc5e-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="fbc5e-134">integer</span></span><br/> | <span data-ttu-id="fbc5e-135">359</span><span class="sxs-lookup"><span data-stu-id="fbc5e-135">359</span></span><br/>             |
| <span data-ttu-id="fbc5e-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="fbc5e-136">MinValue</span></span><br/>     | <span data-ttu-id="fbc5e-137">целое число</span><span class="sxs-lookup"><span data-stu-id="fbc5e-137">integer</span></span><br/> | <span data-ttu-id="fbc5e-138">0</span><span class="sxs-lookup"><span data-stu-id="fbc5e-138">0</span></span><br/>               |
| <span data-ttu-id="fbc5e-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="fbc5e-139">Multiple</span></span><br/>     | <span data-ttu-id="fbc5e-140">целое число</span><span class="sxs-lookup"><span data-stu-id="fbc5e-140">integer</span></span><br/> | <span data-ttu-id="fbc5e-141">1</span><span class="sxs-lookup"><span data-stu-id="fbc5e-141">1</span></span><br/>               |
| <span data-ttu-id="fbc5e-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fbc5e-142">Mandatory</span></span><br/>    | <span data-ttu-id="fbc5e-143">строка</span><span class="sxs-lookup"><span data-stu-id="fbc5e-143">string</span></span><br/>  | <span data-ttu-id="fbc5e-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="fbc5e-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fbc5e-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="fbc5e-145">UnitType</span></span><br/>     | <span data-ttu-id="fbc5e-146">строка</span><span class="sxs-lookup"><span data-stu-id="fbc5e-146">string</span></span><br/>  | <span data-ttu-id="fbc5e-147">градусы</span><span class="sxs-lookup"><span data-stu-id="fbc5e-147">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fbc5e-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fbc5e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbc5e-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="fbc5e-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




