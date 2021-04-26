---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: пажеватермарктекстфонтсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cc8c7f3c9a692ffbe180c253d448d7c4e320d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999134"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="6b61f-104">пажеватермарктекстфонтсизе</span><span class="sxs-lookup"><span data-stu-id="6b61f-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="6b61f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="6b61f-105">This topic is not current.</span></span> <span data-ttu-id="6b61f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6b61f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6b61f-107">Определяет доступные размеры шрифта для текста водяного знака.</span><span class="sxs-lookup"><span data-stu-id="6b61f-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="6b61f-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b61f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6b61f-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="6b61f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6b61f-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b61f-110">Element Information</span></span>



| <span data-ttu-id="6b61f-111">Имя</span><span class="sxs-lookup"><span data-stu-id="6b61f-111">Name</span></span> | <span data-ttu-id="6b61f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6b61f-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="6b61f-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="6b61f-113">Element Type</span></span> <br/>   | <span data-ttu-id="6b61f-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="6b61f-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="6b61f-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="6b61f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6b61f-116">Страница</span><span class="sxs-lookup"><span data-stu-id="6b61f-116">Page</span></span><br/>                            |
| <span data-ttu-id="6b61f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b61f-117">Notes</span></span> <br/>          | <span data-ttu-id="6b61f-118">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="6b61f-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6b61f-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="6b61f-119">Structure Content</span></span>

<span data-ttu-id="6b61f-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6b61f-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="6b61f-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="6b61f-121">Structure Properties</span></span>

<span data-ttu-id="6b61f-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="6b61f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6b61f-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="6b61f-123">Property</span></span>                | <span data-ttu-id="6b61f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6b61f-124">xsi:type</span></span>           | <span data-ttu-id="6b61f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6b61f-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6b61f-126">DataType</span><span class="sxs-lookup"><span data-stu-id="6b61f-126">DataType</span></span><br/>     | <span data-ttu-id="6b61f-127">строка</span><span class="sxs-lookup"><span data-stu-id="6b61f-127">string</span></span><br/>  | <span data-ttu-id="6b61f-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6b61f-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="6b61f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6b61f-129">DefaultValue</span></span><br/> | <span data-ttu-id="6b61f-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="6b61f-130">integer</span></span><br/> | <span data-ttu-id="6b61f-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="6b61f-131">undefined</span></span><br/>       |
| <span data-ttu-id="6b61f-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6b61f-132">MaxValue</span></span><br/>     | <span data-ttu-id="6b61f-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="6b61f-133">integer</span></span><br/> | <span data-ttu-id="6b61f-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="6b61f-134">undefined</span></span><br/>       |
| <span data-ttu-id="6b61f-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="6b61f-135">MinValue</span></span><br/>     | <span data-ttu-id="6b61f-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="6b61f-136">integer</span></span><br/> | <span data-ttu-id="6b61f-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="6b61f-137">undefined</span></span><br/>       |
| <span data-ttu-id="6b61f-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="6b61f-138">Multiple</span></span><br/>     | <span data-ttu-id="6b61f-139">Целое число</span><span class="sxs-lookup"><span data-stu-id="6b61f-139">integer</span></span><br/> | <span data-ttu-id="6b61f-140">неопределенный</span><span class="sxs-lookup"><span data-stu-id="6b61f-140">undefined</span></span><br/>       |
| <span data-ttu-id="6b61f-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b61f-141">Mandatory</span></span><br/>    | <span data-ttu-id="6b61f-142">строка</span><span class="sxs-lookup"><span data-stu-id="6b61f-142">string</span></span><br/>  | <span data-ttu-id="6b61f-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="6b61f-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6b61f-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="6b61f-144">UnitType</span></span><br/>     | <span data-ttu-id="6b61f-145">строка</span><span class="sxs-lookup"><span data-stu-id="6b61f-145">string</span></span><br/>  | <span data-ttu-id="6b61f-146">точки</span><span class="sxs-lookup"><span data-stu-id="6b61f-146">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="6b61f-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="6b61f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b61f-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="6b61f-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




