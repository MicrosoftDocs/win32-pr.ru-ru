---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: пажеблаккженератионпроцессингграйкомпонентреплацементекстент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914275"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="ccaed-104">пажеблаккженератионпроцессингграйкомпонентреплацементекстент</span><span class="sxs-lookup"><span data-stu-id="ccaed-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="ccaed-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ccaed-105">This topic is not current.</span></span> <span data-ttu-id="ccaed-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ccaed-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ccaed-107">Описывает экстенты, превышающие нейтральные (в цветах цветов), к которым применяется ГКР.</span><span class="sxs-lookup"><span data-stu-id="ccaed-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="ccaed-108">0% = замена универсальных компонентов, 100% = серая замена компонентов.</span><span class="sxs-lookup"><span data-stu-id="ccaed-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="ccaed-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ccaed-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ccaed-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ccaed-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ccaed-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ccaed-111">Element Information</span></span>



| <span data-ttu-id="ccaed-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ccaed-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="ccaed-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ccaed-113">Element Type</span></span> <br/>   | <span data-ttu-id="ccaed-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="ccaed-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="ccaed-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ccaed-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ccaed-116">Страница</span><span class="sxs-lookup"><span data-stu-id="ccaed-116">Page</span></span><br/>                                            |
| <span data-ttu-id="ccaed-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccaed-117">Notes</span></span> <br/>          | <span data-ttu-id="ccaed-118">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="ccaed-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ccaed-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ccaed-119">Structure Content</span></span>

<span data-ttu-id="ccaed-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ccaed-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="ccaed-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="ccaed-121">Structure Properties</span></span>

<span data-ttu-id="ccaed-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ccaed-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ccaed-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="ccaed-123">Property</span></span>                | <span data-ttu-id="ccaed-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ccaed-124">xsi:type</span></span>           | <span data-ttu-id="ccaed-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ccaed-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ccaed-126">DataType</span><span class="sxs-lookup"><span data-stu-id="ccaed-126">DataType</span></span><br/>     | <span data-ttu-id="ccaed-127">строка</span><span class="sxs-lookup"><span data-stu-id="ccaed-127">string</span></span><br/>  | <span data-ttu-id="ccaed-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ccaed-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="ccaed-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ccaed-129">DefaultValue</span></span><br/> | <span data-ttu-id="ccaed-130">строка</span><span class="sxs-lookup"><span data-stu-id="ccaed-130">string</span></span><br/>  | <span data-ttu-id="ccaed-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ccaed-131">undefined</span></span><br/>       |
| <span data-ttu-id="ccaed-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ccaed-132">MaxValue</span></span><br/>     | <span data-ttu-id="ccaed-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="ccaed-133">integer</span></span><br/> | <span data-ttu-id="ccaed-134">100</span><span class="sxs-lookup"><span data-stu-id="ccaed-134">100</span></span><br/>             |
| <span data-ttu-id="ccaed-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="ccaed-135">MinValue</span></span><br/>     | <span data-ttu-id="ccaed-136">целое число</span><span class="sxs-lookup"><span data-stu-id="ccaed-136">integer</span></span><br/> | <span data-ttu-id="ccaed-137">0</span><span class="sxs-lookup"><span data-stu-id="ccaed-137">0</span></span><br/>               |
| <span data-ttu-id="ccaed-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="ccaed-138">Multiple</span></span><br/>     | <span data-ttu-id="ccaed-139">целое число</span><span class="sxs-lookup"><span data-stu-id="ccaed-139">integer</span></span><br/> | <span data-ttu-id="ccaed-140">1</span><span class="sxs-lookup"><span data-stu-id="ccaed-140">1</span></span><br/>               |
| <span data-ttu-id="ccaed-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ccaed-141">Mandatory</span></span><br/>    | <span data-ttu-id="ccaed-142">строка</span><span class="sxs-lookup"><span data-stu-id="ccaed-142">string</span></span><br/>  | <span data-ttu-id="ccaed-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="ccaed-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ccaed-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="ccaed-144">UnitType</span></span><br/>     | <span data-ttu-id="ccaed-145">строка</span><span class="sxs-lookup"><span data-stu-id="ccaed-145">string</span></span><br/>  | <span data-ttu-id="ccaed-146">percent</span><span class="sxs-lookup"><span data-stu-id="ccaed-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ccaed-147">См. также</span><span class="sxs-lookup"><span data-stu-id="ccaed-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccaed-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ccaed-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




