---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: пажеватермарктранспаренци
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713321"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="5f9d8-104">пажеватермарктранспаренци</span><span class="sxs-lookup"><span data-stu-id="5f9d8-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="5f9d8-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5f9d8-105">This topic is not current.</span></span> <span data-ttu-id="5f9d8-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5f9d8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5f9d8-107">Задает прозрачность для водяного знака.</span><span class="sxs-lookup"><span data-stu-id="5f9d8-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="5f9d8-108">Полностью непрозрачное значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="5f9d8-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="5f9d8-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5f9d8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5f9d8-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="5f9d8-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5f9d8-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5f9d8-111">Element Information</span></span>



| <span data-ttu-id="5f9d8-112">Имя</span><span class="sxs-lookup"><span data-stu-id="5f9d8-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="5f9d8-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5f9d8-113">Element Type</span></span> <br/>   | <span data-ttu-id="5f9d8-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="5f9d8-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="5f9d8-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5f9d8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5f9d8-116">Страница</span><span class="sxs-lookup"><span data-stu-id="5f9d8-116">Page</span></span><br/>                            |
| <span data-ttu-id="5f9d8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f9d8-117">Notes</span></span> <br/>          | <span data-ttu-id="5f9d8-118">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="5f9d8-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5f9d8-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="5f9d8-119">Structure Content</span></span>

<span data-ttu-id="5f9d8-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5f9d8-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="5f9d8-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="5f9d8-121">Structure Properties</span></span>

<span data-ttu-id="5f9d8-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5f9d8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5f9d8-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="5f9d8-123">Property</span></span>                | <span data-ttu-id="5f9d8-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5f9d8-124">xsi:type</span></span>           | <span data-ttu-id="5f9d8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5f9d8-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5f9d8-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5f9d8-126">DataType</span></span><br/>     | <span data-ttu-id="5f9d8-127">строка</span><span class="sxs-lookup"><span data-stu-id="5f9d8-127">string</span></span><br/>  | <span data-ttu-id="5f9d8-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f9d8-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5f9d8-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5f9d8-129">DefaultValue</span></span><br/> | <span data-ttu-id="5f9d8-130">целое число</span><span class="sxs-lookup"><span data-stu-id="5f9d8-130">integer</span></span><br/> | <span data-ttu-id="5f9d8-131">0</span><span class="sxs-lookup"><span data-stu-id="5f9d8-131">0</span></span><br/>               |
| <span data-ttu-id="5f9d8-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5f9d8-132">MaxValue</span></span><br/>     | <span data-ttu-id="5f9d8-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="5f9d8-133">integer</span></span><br/> | <span data-ttu-id="5f9d8-134">100</span><span class="sxs-lookup"><span data-stu-id="5f9d8-134">100</span></span><br/>             |
| <span data-ttu-id="5f9d8-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5f9d8-135">MinValue</span></span><br/>     | <span data-ttu-id="5f9d8-136">целое число</span><span class="sxs-lookup"><span data-stu-id="5f9d8-136">integer</span></span><br/> | <span data-ttu-id="5f9d8-137">0</span><span class="sxs-lookup"><span data-stu-id="5f9d8-137">0</span></span><br/>               |
| <span data-ttu-id="5f9d8-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="5f9d8-138">Multiple</span></span><br/>     | <span data-ttu-id="5f9d8-139">целое число</span><span class="sxs-lookup"><span data-stu-id="5f9d8-139">integer</span></span><br/> | <span data-ttu-id="5f9d8-140">1</span><span class="sxs-lookup"><span data-stu-id="5f9d8-140">1</span></span><br/>               |
| <span data-ttu-id="5f9d8-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5f9d8-141">Mandatory</span></span><br/>    | <span data-ttu-id="5f9d8-142">строка</span><span class="sxs-lookup"><span data-stu-id="5f9d8-142">string</span></span><br/>  | <span data-ttu-id="5f9d8-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="5f9d8-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5f9d8-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="5f9d8-144">UnitType</span></span><br/>     | <span data-ttu-id="5f9d8-145">строка</span><span class="sxs-lookup"><span data-stu-id="5f9d8-145">string</span></span><br/>  | <span data-ttu-id="5f9d8-146">percent</span><span class="sxs-lookup"><span data-stu-id="5f9d8-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5f9d8-147">См. также</span><span class="sxs-lookup"><span data-stu-id="5f9d8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f9d8-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5f9d8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




