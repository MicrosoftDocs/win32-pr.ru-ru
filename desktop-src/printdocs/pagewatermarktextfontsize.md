---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: пажеватермарктекстфонтсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104081744"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="96c6e-104">пажеватермарктекстфонтсизе</span><span class="sxs-lookup"><span data-stu-id="96c6e-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="96c6e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="96c6e-105">This topic is not current.</span></span> <span data-ttu-id="96c6e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="96c6e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="96c6e-107">Определяет доступные размеры шрифта для текста водяного знака.</span><span class="sxs-lookup"><span data-stu-id="96c6e-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="96c6e-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="96c6e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="96c6e-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="96c6e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="96c6e-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="96c6e-110">Element Information</span></span>



| <span data-ttu-id="96c6e-111">Имя</span><span class="sxs-lookup"><span data-stu-id="96c6e-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="96c6e-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="96c6e-112">Element Type</span></span> <br/>   | <span data-ttu-id="96c6e-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="96c6e-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="96c6e-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="96c6e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="96c6e-115">Страница</span><span class="sxs-lookup"><span data-stu-id="96c6e-115">Page</span></span><br/>                            |
| <span data-ttu-id="96c6e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="96c6e-116">Notes</span></span> <br/>          | <span data-ttu-id="96c6e-117">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="96c6e-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="96c6e-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="96c6e-118">Structure Content</span></span>

<span data-ttu-id="96c6e-119">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="96c6e-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="96c6e-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="96c6e-120">Structure Properties</span></span>

<span data-ttu-id="96c6e-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="96c6e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="96c6e-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="96c6e-122">Property</span></span>                | <span data-ttu-id="96c6e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="96c6e-123">xsi:type</span></span>           | <span data-ttu-id="96c6e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="96c6e-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="96c6e-125">DataType</span><span class="sxs-lookup"><span data-stu-id="96c6e-125">DataType</span></span><br/>     | <span data-ttu-id="96c6e-126">строка</span><span class="sxs-lookup"><span data-stu-id="96c6e-126">string</span></span><br/>  | <span data-ttu-id="96c6e-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96c6e-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="96c6e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="96c6e-128">DefaultValue</span></span><br/> | <span data-ttu-id="96c6e-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="96c6e-129">integer</span></span><br/> | <span data-ttu-id="96c6e-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="96c6e-130">undefined</span></span><br/>       |
| <span data-ttu-id="96c6e-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="96c6e-131">MaxValue</span></span><br/>     | <span data-ttu-id="96c6e-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="96c6e-132">integer</span></span><br/> | <span data-ttu-id="96c6e-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="96c6e-133">undefined</span></span><br/>       |
| <span data-ttu-id="96c6e-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="96c6e-134">MinValue</span></span><br/>     | <span data-ttu-id="96c6e-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="96c6e-135">integer</span></span><br/> | <span data-ttu-id="96c6e-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="96c6e-136">undefined</span></span><br/>       |
| <span data-ttu-id="96c6e-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="96c6e-137">Multiple</span></span><br/>     | <span data-ttu-id="96c6e-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="96c6e-138">integer</span></span><br/> | <span data-ttu-id="96c6e-139">неопределенный</span><span class="sxs-lookup"><span data-stu-id="96c6e-139">undefined</span></span><br/>       |
| <span data-ttu-id="96c6e-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96c6e-140">Mandatory</span></span><br/>    | <span data-ttu-id="96c6e-141">строка</span><span class="sxs-lookup"><span data-stu-id="96c6e-141">string</span></span><br/>  | <span data-ttu-id="96c6e-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="96c6e-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="96c6e-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="96c6e-143">UnitType</span></span><br/>     | <span data-ttu-id="96c6e-144">строка</span><span class="sxs-lookup"><span data-stu-id="96c6e-144">string</span></span><br/>  | <span data-ttu-id="96c6e-145">точки</span><span class="sxs-lookup"><span data-stu-id="96c6e-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="96c6e-146">См. также</span><span class="sxs-lookup"><span data-stu-id="96c6e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96c6e-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="96c6e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




