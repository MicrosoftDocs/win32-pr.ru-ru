---
description: Получение сведений о параметре Пажеватермарктекстфонтсизе. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: пажеватермарктекстфонтсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395999"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="06fe8-105">пажеватермарктекстфонтсизе</span><span class="sxs-lookup"><span data-stu-id="06fe8-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="06fe8-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="06fe8-106">This topic is not current.</span></span> <span data-ttu-id="06fe8-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="06fe8-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06fe8-108">Определяет доступные размеры шрифта для текста водяного знака.</span><span class="sxs-lookup"><span data-stu-id="06fe8-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="06fe8-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="06fe8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06fe8-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="06fe8-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="06fe8-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="06fe8-111">Element Information</span></span>



| <span data-ttu-id="06fe8-112">Имя</span><span class="sxs-lookup"><span data-stu-id="06fe8-112">Name</span></span> | <span data-ttu-id="06fe8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="06fe8-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="06fe8-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="06fe8-114">Element Type</span></span> <br/>   | <span data-ttu-id="06fe8-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="06fe8-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="06fe8-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="06fe8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06fe8-117">Страница</span><span class="sxs-lookup"><span data-stu-id="06fe8-117">Page</span></span><br/>                            |
| <span data-ttu-id="06fe8-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="06fe8-118">Notes</span></span> <br/>          | <span data-ttu-id="06fe8-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="06fe8-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="06fe8-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="06fe8-120">Structure Content</span></span>

<span data-ttu-id="06fe8-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06fe8-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="06fe8-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="06fe8-122">Structure Properties</span></span>

<span data-ttu-id="06fe8-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="06fe8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06fe8-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="06fe8-124">Property</span></span>                | <span data-ttu-id="06fe8-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="06fe8-125">xsi:type</span></span>           | <span data-ttu-id="06fe8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="06fe8-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="06fe8-127">DataType</span><span class="sxs-lookup"><span data-stu-id="06fe8-127">DataType</span></span><br/>     | <span data-ttu-id="06fe8-128">строка</span><span class="sxs-lookup"><span data-stu-id="06fe8-128">string</span></span><br/>  | <span data-ttu-id="06fe8-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06fe8-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="06fe8-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="06fe8-130">DefaultValue</span></span><br/> | <span data-ttu-id="06fe8-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="06fe8-131">integer</span></span><br/> | <span data-ttu-id="06fe8-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="06fe8-132">undefined</span></span><br/>       |
| <span data-ttu-id="06fe8-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="06fe8-133">MaxValue</span></span><br/>     | <span data-ttu-id="06fe8-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="06fe8-134">integer</span></span><br/> | <span data-ttu-id="06fe8-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="06fe8-135">undefined</span></span><br/>       |
| <span data-ttu-id="06fe8-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="06fe8-136">MinValue</span></span><br/>     | <span data-ttu-id="06fe8-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="06fe8-137">integer</span></span><br/> | <span data-ttu-id="06fe8-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="06fe8-138">undefined</span></span><br/>       |
| <span data-ttu-id="06fe8-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="06fe8-139">Multiple</span></span><br/>     | <span data-ttu-id="06fe8-140">Целое число</span><span class="sxs-lookup"><span data-stu-id="06fe8-140">integer</span></span><br/> | <span data-ttu-id="06fe8-141">неопределенный</span><span class="sxs-lookup"><span data-stu-id="06fe8-141">undefined</span></span><br/>       |
| <span data-ttu-id="06fe8-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="06fe8-142">Mandatory</span></span><br/>    | <span data-ttu-id="06fe8-143">строка</span><span class="sxs-lookup"><span data-stu-id="06fe8-143">string</span></span><br/>  | <span data-ttu-id="06fe8-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="06fe8-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="06fe8-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="06fe8-145">UnitType</span></span><br/>     | <span data-ttu-id="06fe8-146">строка</span><span class="sxs-lookup"><span data-stu-id="06fe8-146">string</span></span><br/>  | <span data-ttu-id="06fe8-147">точки</span><span class="sxs-lookup"><span data-stu-id="06fe8-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="06fe8-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="06fe8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06fe8-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="06fe8-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




