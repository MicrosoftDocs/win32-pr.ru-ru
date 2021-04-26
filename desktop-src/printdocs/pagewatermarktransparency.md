---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: пажеватермарктранспаренци
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996881"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="7b461-104">пажеватермарктранспаренци</span><span class="sxs-lookup"><span data-stu-id="7b461-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="7b461-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7b461-105">This topic is not current.</span></span> <span data-ttu-id="7b461-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b461-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b461-107">Задает прозрачность для водяного знака.</span><span class="sxs-lookup"><span data-stu-id="7b461-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="7b461-108">Полностью непрозрачное значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="7b461-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="7b461-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7b461-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b461-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7b461-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7b461-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7b461-111">Element Information</span></span>



| <span data-ttu-id="7b461-112">Имя</span><span class="sxs-lookup"><span data-stu-id="7b461-112">Name</span></span> | <span data-ttu-id="7b461-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7b461-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="7b461-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7b461-114">Element Type</span></span> <br/>   | <span data-ttu-id="7b461-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="7b461-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="7b461-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7b461-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b461-117">Страница</span><span class="sxs-lookup"><span data-stu-id="7b461-117">Page</span></span><br/>                            |
| <span data-ttu-id="7b461-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b461-118">Notes</span></span> <br/>          | <span data-ttu-id="7b461-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="7b461-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7b461-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7b461-120">Structure Content</span></span>

<span data-ttu-id="7b461-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b461-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7b461-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="7b461-122">Structure Properties</span></span>

<span data-ttu-id="7b461-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7b461-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b461-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="7b461-124">Property</span></span>                | <span data-ttu-id="7b461-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7b461-125">xsi:type</span></span>           | <span data-ttu-id="7b461-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7b461-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7b461-127">DataType</span><span class="sxs-lookup"><span data-stu-id="7b461-127">DataType</span></span><br/>     | <span data-ttu-id="7b461-128">строка</span><span class="sxs-lookup"><span data-stu-id="7b461-128">string</span></span><br/>  | <span data-ttu-id="7b461-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7b461-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="7b461-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7b461-130">DefaultValue</span></span><br/> | <span data-ttu-id="7b461-131">целое число</span><span class="sxs-lookup"><span data-stu-id="7b461-131">integer</span></span><br/> | <span data-ttu-id="7b461-132">0</span><span class="sxs-lookup"><span data-stu-id="7b461-132">0</span></span><br/>               |
| <span data-ttu-id="7b461-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7b461-133">MaxValue</span></span><br/>     | <span data-ttu-id="7b461-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="7b461-134">integer</span></span><br/> | <span data-ttu-id="7b461-135">100</span><span class="sxs-lookup"><span data-stu-id="7b461-135">100</span></span><br/>             |
| <span data-ttu-id="7b461-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="7b461-136">MinValue</span></span><br/>     | <span data-ttu-id="7b461-137">целое число</span><span class="sxs-lookup"><span data-stu-id="7b461-137">integer</span></span><br/> | <span data-ttu-id="7b461-138">0</span><span class="sxs-lookup"><span data-stu-id="7b461-138">0</span></span><br/>               |
| <span data-ttu-id="7b461-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="7b461-139">Multiple</span></span><br/>     | <span data-ttu-id="7b461-140">целое число</span><span class="sxs-lookup"><span data-stu-id="7b461-140">integer</span></span><br/> | <span data-ttu-id="7b461-141">1</span><span class="sxs-lookup"><span data-stu-id="7b461-141">1</span></span><br/>               |
| <span data-ttu-id="7b461-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b461-142">Mandatory</span></span><br/>    | <span data-ttu-id="7b461-143">строка</span><span class="sxs-lookup"><span data-stu-id="7b461-143">string</span></span><br/>  | <span data-ttu-id="7b461-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="7b461-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7b461-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="7b461-145">UnitType</span></span><br/>     | <span data-ttu-id="7b461-146">строка</span><span class="sxs-lookup"><span data-stu-id="7b461-146">string</span></span><br/>  | <span data-ttu-id="7b461-147">percent</span><span class="sxs-lookup"><span data-stu-id="7b461-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7b461-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7b461-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b461-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7b461-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




