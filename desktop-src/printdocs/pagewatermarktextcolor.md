---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: пажеватермарктекстколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104547463"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="397c0-104">пажеватермарктекстколор</span><span class="sxs-lookup"><span data-stu-id="397c0-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="397c0-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="397c0-105">This topic is not current.</span></span> <span data-ttu-id="397c0-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="397c0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="397c0-107">Определяет цвет sRGB для текста водяного знака.</span><span class="sxs-lookup"><span data-stu-id="397c0-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="397c0-108">Формат — ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="397c0-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="397c0-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="397c0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="397c0-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="397c0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="397c0-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="397c0-111">Element Information</span></span>



| <span data-ttu-id="397c0-112">Имя</span><span class="sxs-lookup"><span data-stu-id="397c0-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="397c0-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="397c0-113">Element Type</span></span> <br/>   | <span data-ttu-id="397c0-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="397c0-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="397c0-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="397c0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="397c0-116">Страница</span><span class="sxs-lookup"><span data-stu-id="397c0-116">Page</span></span><br/>                            |
| <span data-ttu-id="397c0-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="397c0-117">Notes</span></span> <br/>          | <span data-ttu-id="397c0-118">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="397c0-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="397c0-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="397c0-119">Structure Content</span></span>

<span data-ttu-id="397c0-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="397c0-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="397c0-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="397c0-121">Structure Properties</span></span>

<span data-ttu-id="397c0-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="397c0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="397c0-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="397c0-123">Property</span></span>                | <span data-ttu-id="397c0-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="397c0-124">xsi:type</span></span>           | <span data-ttu-id="397c0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="397c0-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="397c0-126">DataType</span><span class="sxs-lookup"><span data-stu-id="397c0-126">DataType</span></span><br/>     | <span data-ttu-id="397c0-127">строка</span><span class="sxs-lookup"><span data-stu-id="397c0-127">string</span></span><br/>  | <span data-ttu-id="397c0-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="397c0-128">xs:string</span></span><br/>       |
| <span data-ttu-id="397c0-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="397c0-129">DefaultValue</span></span><br/> | <span data-ttu-id="397c0-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="397c0-130">integer</span></span><br/> | <span data-ttu-id="397c0-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="397c0-131">undefined</span></span><br/>       |
| <span data-ttu-id="397c0-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="397c0-132">MaxValue</span></span><br/>     | <span data-ttu-id="397c0-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="397c0-133">integer</span></span><br/> | <span data-ttu-id="397c0-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="397c0-134">undefined</span></span><br/>       |
| <span data-ttu-id="397c0-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="397c0-135">MinValue</span></span><br/>     | <span data-ttu-id="397c0-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="397c0-136">integer</span></span><br/> | <span data-ttu-id="397c0-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="397c0-137">undefined</span></span><br/>       |
| <span data-ttu-id="397c0-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="397c0-138">Mandatory</span></span><br/>    | <span data-ttu-id="397c0-139">строка</span><span class="sxs-lookup"><span data-stu-id="397c0-139">string</span></span><br/>  | <span data-ttu-id="397c0-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="397c0-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="397c0-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="397c0-141">UnitType</span></span><br/>     | <span data-ttu-id="397c0-142">строка</span><span class="sxs-lookup"><span data-stu-id="397c0-142">string</span></span><br/>  | <span data-ttu-id="397c0-143">sRGB</span><span class="sxs-lookup"><span data-stu-id="397c0-143">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="397c0-144">См. также</span><span class="sxs-lookup"><span data-stu-id="397c0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="397c0-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="397c0-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




