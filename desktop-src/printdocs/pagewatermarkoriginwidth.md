---
description: Получение сведений о параметре Пажеватермаркоригинвидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: пажеватермаркоригинвидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe6457496972231877af2a51e03bc5109083d0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396009"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="ceb30-105">пажеватермаркоригинвидс</span><span class="sxs-lookup"><span data-stu-id="ceb30-105">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="ceb30-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ceb30-106">This topic is not current.</span></span> <span data-ttu-id="ceb30-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ceb30-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ceb30-108">Задает источник водяного знака относительно источника Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="ceb30-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="ceb30-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ceb30-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ceb30-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ceb30-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ceb30-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ceb30-111">Element Information</span></span>



| <span data-ttu-id="ceb30-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ceb30-112">Name</span></span> | <span data-ttu-id="ceb30-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ceb30-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="ceb30-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ceb30-114">Element Type</span></span> <br/>   | <span data-ttu-id="ceb30-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="ceb30-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="ceb30-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ceb30-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ceb30-117">Страница</span><span class="sxs-lookup"><span data-stu-id="ceb30-117">Page</span></span><br/>                            |
| <span data-ttu-id="ceb30-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ceb30-118">Notes</span></span> <br/>          | <span data-ttu-id="ceb30-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="ceb30-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ceb30-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ceb30-120">Structure Content</span></span>

<span data-ttu-id="ceb30-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ceb30-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="ceb30-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="ceb30-122">Structure Properties</span></span>

<span data-ttu-id="ceb30-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ceb30-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ceb30-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="ceb30-124">Property</span></span>                | <span data-ttu-id="ceb30-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ceb30-125">xsi:type</span></span>           | <span data-ttu-id="ceb30-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ceb30-126">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ceb30-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ceb30-127">DataType</span></span><br/>     | <span data-ttu-id="ceb30-128">строка</span><span class="sxs-lookup"><span data-stu-id="ceb30-128">string</span></span><br/>  | <span data-ttu-id="ceb30-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ceb30-129">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="ceb30-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ceb30-130">DefaultValue</span></span><br/> | <span data-ttu-id="ceb30-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="ceb30-131">integer</span></span><br/> | <span data-ttu-id="ceb30-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ceb30-132">undefined</span></span><br/>                                                   |
| <span data-ttu-id="ceb30-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ceb30-133">MaxValue</span></span><br/>     | <span data-ttu-id="ceb30-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="ceb30-134">integer</span></span><br/> | <span data-ttu-id="ceb30-135">Меньше или равно Пажеимажеаблесизе-ExtentWidth значение</span><span class="sxs-lookup"><span data-stu-id="ceb30-135">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="ceb30-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="ceb30-136">MinValue</span></span><br/>     | <span data-ttu-id="ceb30-137">целое число</span><span class="sxs-lookup"><span data-stu-id="ceb30-137">integer</span></span><br/> | <span data-ttu-id="ceb30-138">0</span><span class="sxs-lookup"><span data-stu-id="ceb30-138">0</span></span><br/>                                                           |
| <span data-ttu-id="ceb30-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="ceb30-139">Multiple</span></span><br/>     | <span data-ttu-id="ceb30-140">целое число</span><span class="sxs-lookup"><span data-stu-id="ceb30-140">integer</span></span><br/> | <span data-ttu-id="ceb30-141">1</span><span class="sxs-lookup"><span data-stu-id="ceb30-141">1</span></span><br/>                                                           |
| <span data-ttu-id="ceb30-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ceb30-142">Mandatory</span></span><br/>    | <span data-ttu-id="ceb30-143">строка</span><span class="sxs-lookup"><span data-stu-id="ceb30-143">string</span></span><br/>  | <span data-ttu-id="ceb30-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="ceb30-144">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="ceb30-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="ceb30-145">UnitType</span></span><br/>     | <span data-ttu-id="ceb30-146">строка</span><span class="sxs-lookup"><span data-stu-id="ceb30-146">string</span></span><br/>  | <span data-ttu-id="ceb30-147">мкм</span><span class="sxs-lookup"><span data-stu-id="ceb30-147">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="ceb30-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ceb30-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceb30-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ceb30-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




