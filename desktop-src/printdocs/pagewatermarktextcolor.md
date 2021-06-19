---
description: Получение сведений о параметре Пажеватермарктекстколор. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: пажеватермарктекстколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396019"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="8a699-105">пажеватермарктекстколор</span><span class="sxs-lookup"><span data-stu-id="8a699-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="8a699-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8a699-106">This topic is not current.</span></span> <span data-ttu-id="8a699-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8a699-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8a699-108">Определяет цвет sRGB для текста водяного знака.</span><span class="sxs-lookup"><span data-stu-id="8a699-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="8a699-109">Формат — ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="8a699-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="8a699-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8a699-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8a699-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8a699-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8a699-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8a699-112">Element Information</span></span>



| <span data-ttu-id="8a699-113">Имя</span><span class="sxs-lookup"><span data-stu-id="8a699-113">Name</span></span> | <span data-ttu-id="8a699-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8a699-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="8a699-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8a699-115">Element Type</span></span> <br/>   | <span data-ttu-id="8a699-116">параметердеф</span><span class="sxs-lookup"><span data-stu-id="8a699-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="8a699-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8a699-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8a699-118">Страница</span><span class="sxs-lookup"><span data-stu-id="8a699-118">Page</span></span><br/>                            |
| <span data-ttu-id="8a699-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a699-119">Notes</span></span> <br/>          | <span data-ttu-id="8a699-120">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="8a699-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8a699-121">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8a699-121">Structure Content</span></span>

<span data-ttu-id="8a699-122">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8a699-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8a699-123">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="8a699-123">Structure Properties</span></span>

<span data-ttu-id="8a699-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8a699-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8a699-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="8a699-125">Property</span></span>                | <span data-ttu-id="8a699-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8a699-126">xsi:type</span></span>           | <span data-ttu-id="8a699-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8a699-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8a699-128">DataType</span><span class="sxs-lookup"><span data-stu-id="8a699-128">DataType</span></span><br/>     | <span data-ttu-id="8a699-129">строка</span><span class="sxs-lookup"><span data-stu-id="8a699-129">string</span></span><br/>  | <span data-ttu-id="8a699-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="8a699-130">xs:string</span></span><br/>       |
| <span data-ttu-id="8a699-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8a699-131">DefaultValue</span></span><br/> | <span data-ttu-id="8a699-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="8a699-132">integer</span></span><br/> | <span data-ttu-id="8a699-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8a699-133">undefined</span></span><br/>       |
| <span data-ttu-id="8a699-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8a699-134">MaxValue</span></span><br/>     | <span data-ttu-id="8a699-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="8a699-135">integer</span></span><br/> | <span data-ttu-id="8a699-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8a699-136">undefined</span></span><br/>       |
| <span data-ttu-id="8a699-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="8a699-137">MinValue</span></span><br/>     | <span data-ttu-id="8a699-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="8a699-138">integer</span></span><br/> | <span data-ttu-id="8a699-139">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8a699-139">undefined</span></span><br/>       |
| <span data-ttu-id="8a699-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8a699-140">Mandatory</span></span><br/>    | <span data-ttu-id="8a699-141">строка</span><span class="sxs-lookup"><span data-stu-id="8a699-141">string</span></span><br/>  | <span data-ttu-id="8a699-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="8a699-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8a699-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="8a699-143">UnitType</span></span><br/>     | <span data-ttu-id="8a699-144">строка</span><span class="sxs-lookup"><span data-stu-id="8a699-144">string</span></span><br/>  | <span data-ttu-id="8a699-145">sRGB</span><span class="sxs-lookup"><span data-stu-id="8a699-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="8a699-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8a699-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a699-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8a699-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




