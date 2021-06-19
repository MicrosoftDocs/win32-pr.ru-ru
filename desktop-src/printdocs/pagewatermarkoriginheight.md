---
description: Получение сведений о параметре Пажеватермаркоригинхеигхт. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: пажеватермаркоригинхеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59e9336088d44cef1941df03319519ae69af1c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395989"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="63ae6-105">пажеватермаркоригинхеигхт</span><span class="sxs-lookup"><span data-stu-id="63ae6-105">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="63ae6-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="63ae6-106">This topic is not current.</span></span> <span data-ttu-id="63ae6-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63ae6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63ae6-108">Задает источник водяного знака относительно источника Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="63ae6-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="63ae6-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63ae6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63ae6-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="63ae6-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="63ae6-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63ae6-111">Element Information</span></span>



| <span data-ttu-id="63ae6-112">Имя</span><span class="sxs-lookup"><span data-stu-id="63ae6-112">Name</span></span> | <span data-ttu-id="63ae6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="63ae6-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="63ae6-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="63ae6-114">Element Type</span></span> <br/>   | <span data-ttu-id="63ae6-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="63ae6-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="63ae6-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="63ae6-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63ae6-117">Страница</span><span class="sxs-lookup"><span data-stu-id="63ae6-117">Page</span></span><br/>                            |
| <span data-ttu-id="63ae6-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="63ae6-118">Notes</span></span> <br/>          | <span data-ttu-id="63ae6-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="63ae6-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="63ae6-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="63ae6-120">Structure Content</span></span>

<span data-ttu-id="63ae6-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="63ae6-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="63ae6-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="63ae6-122">Structure Properties</span></span>

<span data-ttu-id="63ae6-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="63ae6-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63ae6-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="63ae6-124">Property</span></span>                | <span data-ttu-id="63ae6-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="63ae6-125">xsi:type</span></span>           | <span data-ttu-id="63ae6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="63ae6-126">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="63ae6-127">DataType</span><span class="sxs-lookup"><span data-stu-id="63ae6-127">DataType</span></span><br/>     | <span data-ttu-id="63ae6-128">строка</span><span class="sxs-lookup"><span data-stu-id="63ae6-128">string</span></span><br/>  | <span data-ttu-id="63ae6-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="63ae6-129">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="63ae6-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="63ae6-130">DefaultValue</span></span><br/> | <span data-ttu-id="63ae6-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="63ae6-131">integer</span></span><br/> | <span data-ttu-id="63ae6-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="63ae6-132">undefined</span></span><br/>                                                    |
| <span data-ttu-id="63ae6-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="63ae6-133">MaxValue</span></span><br/>     | <span data-ttu-id="63ae6-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="63ae6-134">integer</span></span><br/> | <span data-ttu-id="63ae6-135">Меньше или равно Пажеимажеаблесизе-Екстенсеигхт значение</span><span class="sxs-lookup"><span data-stu-id="63ae6-135">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="63ae6-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="63ae6-136">MinValue</span></span><br/>     | <span data-ttu-id="63ae6-137">целое число</span><span class="sxs-lookup"><span data-stu-id="63ae6-137">integer</span></span><br/> | <span data-ttu-id="63ae6-138">0</span><span class="sxs-lookup"><span data-stu-id="63ae6-138">0</span></span><br/>                                                            |
| <span data-ttu-id="63ae6-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="63ae6-139">Multiple</span></span><br/>     | <span data-ttu-id="63ae6-140">целое число</span><span class="sxs-lookup"><span data-stu-id="63ae6-140">integer</span></span><br/> | <span data-ttu-id="63ae6-141">1</span><span class="sxs-lookup"><span data-stu-id="63ae6-141">1</span></span><br/>                                                            |
| <span data-ttu-id="63ae6-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="63ae6-142">Mandatory</span></span><br/>    | <span data-ttu-id="63ae6-143">строка</span><span class="sxs-lookup"><span data-stu-id="63ae6-143">string</span></span><br/>  | <span data-ttu-id="63ae6-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="63ae6-144">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="63ae6-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="63ae6-145">UnitType</span></span><br/>     | <span data-ttu-id="63ae6-146">строка</span><span class="sxs-lookup"><span data-stu-id="63ae6-146">string</span></span><br/>  | <span data-ttu-id="63ae6-147">мкм</span><span class="sxs-lookup"><span data-stu-id="63ae6-147">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="63ae6-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="63ae6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63ae6-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="63ae6-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




