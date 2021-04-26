---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: пажеватермарктекстколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996891"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="9dcef-104">пажеватермарктекстколор</span><span class="sxs-lookup"><span data-stu-id="9dcef-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="9dcef-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="9dcef-105">This topic is not current.</span></span> <span data-ttu-id="9dcef-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9dcef-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9dcef-107">Определяет цвет sRGB для текста водяного знака.</span><span class="sxs-lookup"><span data-stu-id="9dcef-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="9dcef-108">Формат — ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="9dcef-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="9dcef-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9dcef-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9dcef-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="9dcef-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9dcef-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9dcef-111">Element Information</span></span>



| <span data-ttu-id="9dcef-112">Имя</span><span class="sxs-lookup"><span data-stu-id="9dcef-112">Name</span></span> | <span data-ttu-id="9dcef-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9dcef-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="9dcef-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="9dcef-114">Element Type</span></span> <br/>   | <span data-ttu-id="9dcef-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="9dcef-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="9dcef-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="9dcef-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9dcef-117">Страница</span><span class="sxs-lookup"><span data-stu-id="9dcef-117">Page</span></span><br/>                            |
| <span data-ttu-id="9dcef-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="9dcef-118">Notes</span></span> <br/>          | <span data-ttu-id="9dcef-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="9dcef-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9dcef-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="9dcef-120">Structure Content</span></span>

<span data-ttu-id="9dcef-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9dcef-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="9dcef-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="9dcef-122">Structure Properties</span></span>

<span data-ttu-id="9dcef-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="9dcef-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9dcef-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="9dcef-124">Property</span></span>                | <span data-ttu-id="9dcef-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9dcef-125">xsi:type</span></span>           | <span data-ttu-id="9dcef-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9dcef-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9dcef-127">DataType</span><span class="sxs-lookup"><span data-stu-id="9dcef-127">DataType</span></span><br/>     | <span data-ttu-id="9dcef-128">строка</span><span class="sxs-lookup"><span data-stu-id="9dcef-128">string</span></span><br/>  | <span data-ttu-id="9dcef-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="9dcef-129">xs:string</span></span><br/>       |
| <span data-ttu-id="9dcef-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9dcef-130">DefaultValue</span></span><br/> | <span data-ttu-id="9dcef-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="9dcef-131">integer</span></span><br/> | <span data-ttu-id="9dcef-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="9dcef-132">undefined</span></span><br/>       |
| <span data-ttu-id="9dcef-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9dcef-133">MaxValue</span></span><br/>     | <span data-ttu-id="9dcef-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="9dcef-134">integer</span></span><br/> | <span data-ttu-id="9dcef-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="9dcef-135">undefined</span></span><br/>       |
| <span data-ttu-id="9dcef-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="9dcef-136">MinValue</span></span><br/>     | <span data-ttu-id="9dcef-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="9dcef-137">integer</span></span><br/> | <span data-ttu-id="9dcef-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="9dcef-138">undefined</span></span><br/>       |
| <span data-ttu-id="9dcef-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9dcef-139">Mandatory</span></span><br/>    | <span data-ttu-id="9dcef-140">строка</span><span class="sxs-lookup"><span data-stu-id="9dcef-140">string</span></span><br/>  | <span data-ttu-id="9dcef-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="9dcef-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9dcef-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="9dcef-142">UnitType</span></span><br/>     | <span data-ttu-id="9dcef-143">строка</span><span class="sxs-lookup"><span data-stu-id="9dcef-143">string</span></span><br/>  | <span data-ttu-id="9dcef-144">sRGB</span><span class="sxs-lookup"><span data-stu-id="9dcef-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="9dcef-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9dcef-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dcef-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="9dcef-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




