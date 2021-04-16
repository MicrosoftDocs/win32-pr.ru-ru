---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: пажеблаккженератионпроцессингграйкомпонентреплацементлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c0d55c2150f5a2299672ebf95d6656b238acc1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351885"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="94ff3-104">пажеблаккженератионпроцессингграйкомпонентреплацементлевел</span><span class="sxs-lookup"><span data-stu-id="94ff3-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="94ff3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="94ff3-105">This topic is not current.</span></span> <span data-ttu-id="94ff3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="94ff3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="94ff3-107">Указывает процент заменяющей серого компонента для выполнения.</span><span class="sxs-lookup"><span data-stu-id="94ff3-107">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="94ff3-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="94ff3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="94ff3-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="94ff3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="94ff3-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="94ff3-110">Element Information</span></span>



| <span data-ttu-id="94ff3-111">Имя</span><span class="sxs-lookup"><span data-stu-id="94ff3-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="94ff3-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="94ff3-112">Element Type</span></span> <br/>   | <span data-ttu-id="94ff3-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="94ff3-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="94ff3-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="94ff3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="94ff3-115">Страница</span><span class="sxs-lookup"><span data-stu-id="94ff3-115">Page</span></span><br/>                                            |
| <span data-ttu-id="94ff3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="94ff3-116">Notes</span></span> <br/>          | <span data-ttu-id="94ff3-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="94ff3-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="94ff3-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="94ff3-118">Structure Content</span></span>

<span data-ttu-id="94ff3-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="94ff3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="94ff3-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="94ff3-120">Structure Properties</span></span>

<span data-ttu-id="94ff3-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="94ff3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="94ff3-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="94ff3-122">Property</span></span>                | <span data-ttu-id="94ff3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="94ff3-123">xsi:type</span></span>           | <span data-ttu-id="94ff3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="94ff3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="94ff3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="94ff3-125">DataType</span></span><br/>     | <span data-ttu-id="94ff3-126">строка</span><span class="sxs-lookup"><span data-stu-id="94ff3-126">string</span></span><br/>  | <span data-ttu-id="94ff3-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94ff3-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="94ff3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="94ff3-128">DefaultValue</span></span><br/> | <span data-ttu-id="94ff3-129">строка</span><span class="sxs-lookup"><span data-stu-id="94ff3-129">string</span></span><br/>  | <span data-ttu-id="94ff3-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="94ff3-130">undefined</span></span><br/>       |
| <span data-ttu-id="94ff3-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="94ff3-131">MaxValue</span></span><br/>     | <span data-ttu-id="94ff3-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="94ff3-132">integer</span></span><br/> | <span data-ttu-id="94ff3-133">100</span><span class="sxs-lookup"><span data-stu-id="94ff3-133">100</span></span><br/>             |
| <span data-ttu-id="94ff3-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="94ff3-134">MinValue</span></span><br/>     | <span data-ttu-id="94ff3-135">целое число</span><span class="sxs-lookup"><span data-stu-id="94ff3-135">integer</span></span><br/> | <span data-ttu-id="94ff3-136">0</span><span class="sxs-lookup"><span data-stu-id="94ff3-136">0</span></span><br/>               |
| <span data-ttu-id="94ff3-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="94ff3-137">Multiple</span></span><br/>     | <span data-ttu-id="94ff3-138">целое число</span><span class="sxs-lookup"><span data-stu-id="94ff3-138">integer</span></span><br/> | <span data-ttu-id="94ff3-139">1</span><span class="sxs-lookup"><span data-stu-id="94ff3-139">1</span></span><br/>               |
| <span data-ttu-id="94ff3-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94ff3-140">Mandatory</span></span><br/>    | <span data-ttu-id="94ff3-141">строка</span><span class="sxs-lookup"><span data-stu-id="94ff3-141">string</span></span><br/>  | <span data-ttu-id="94ff3-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="94ff3-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="94ff3-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="94ff3-143">UnitType</span></span><br/>     | <span data-ttu-id="94ff3-144">строка</span><span class="sxs-lookup"><span data-stu-id="94ff3-144">string</span></span><br/>  | <span data-ttu-id="94ff3-145">percent</span><span class="sxs-lookup"><span data-stu-id="94ff3-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="94ff3-146">См. также</span><span class="sxs-lookup"><span data-stu-id="94ff3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94ff3-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="94ff3-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




