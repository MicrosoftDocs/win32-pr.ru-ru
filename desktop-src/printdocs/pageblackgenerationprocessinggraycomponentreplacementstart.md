---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: пажеблаккженератионпроцессингграйкомпонентреплацементстарт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dedf425cd31dd83bce877358c456d1cd16183fa
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693920"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="e74ea-104">пажеблаккженератионпроцессингграйкомпонентреплацементстарт</span><span class="sxs-lookup"><span data-stu-id="e74ea-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="e74ea-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e74ea-105">This topic is not current.</span></span> <span data-ttu-id="e74ea-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e74ea-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e74ea-107">Описывает точку в диапазоне "выделить в тень", где должно запускаться ГКР (100% темно-темная тень).</span><span class="sxs-lookup"><span data-stu-id="e74ea-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="e74ea-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e74ea-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e74ea-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e74ea-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e74ea-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e74ea-110">Element Information</span></span>



| <span data-ttu-id="e74ea-111">Имя</span><span class="sxs-lookup"><span data-stu-id="e74ea-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e74ea-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e74ea-112">Element Type</span></span> <br/>   | <span data-ttu-id="e74ea-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="e74ea-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="e74ea-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e74ea-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e74ea-115">Страница</span><span class="sxs-lookup"><span data-stu-id="e74ea-115">Page</span></span><br/>                                            |
| <span data-ttu-id="e74ea-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e74ea-116">Notes</span></span> <br/>          | <span data-ttu-id="e74ea-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="e74ea-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e74ea-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e74ea-118">Structure Content</span></span>

<span data-ttu-id="e74ea-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e74ea-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="e74ea-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="e74ea-120">Structure Properties</span></span>

<span data-ttu-id="e74ea-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e74ea-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e74ea-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="e74ea-122">Property</span></span>                | <span data-ttu-id="e74ea-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e74ea-123">xsi:type</span></span>           | <span data-ttu-id="e74ea-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e74ea-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e74ea-125">DataType</span><span class="sxs-lookup"><span data-stu-id="e74ea-125">DataType</span></span><br/>     | <span data-ttu-id="e74ea-126">строка</span><span class="sxs-lookup"><span data-stu-id="e74ea-126">string</span></span><br/>  | <span data-ttu-id="e74ea-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e74ea-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="e74ea-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e74ea-128">DefaultValue</span></span><br/> | <span data-ttu-id="e74ea-129">строка</span><span class="sxs-lookup"><span data-stu-id="e74ea-129">string</span></span><br/>  | <span data-ttu-id="e74ea-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e74ea-130">undefined</span></span><br/>       |
| <span data-ttu-id="e74ea-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e74ea-131">MaxValue</span></span><br/>     | <span data-ttu-id="e74ea-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="e74ea-132">integer</span></span><br/> | <span data-ttu-id="e74ea-133">100</span><span class="sxs-lookup"><span data-stu-id="e74ea-133">100</span></span><br/>             |
| <span data-ttu-id="e74ea-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="e74ea-134">MinValue</span></span><br/>     | <span data-ttu-id="e74ea-135">целое число</span><span class="sxs-lookup"><span data-stu-id="e74ea-135">integer</span></span><br/> | <span data-ttu-id="e74ea-136">0</span><span class="sxs-lookup"><span data-stu-id="e74ea-136">0</span></span><br/>               |
| <span data-ttu-id="e74ea-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="e74ea-137">Multiple</span></span><br/>     | <span data-ttu-id="e74ea-138">целое число</span><span class="sxs-lookup"><span data-stu-id="e74ea-138">integer</span></span><br/> | <span data-ttu-id="e74ea-139">1</span><span class="sxs-lookup"><span data-stu-id="e74ea-139">1</span></span><br/>               |
| <span data-ttu-id="e74ea-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e74ea-140">Mandatory</span></span><br/>    | <span data-ttu-id="e74ea-141">строка</span><span class="sxs-lookup"><span data-stu-id="e74ea-141">string</span></span><br/>  | <span data-ttu-id="e74ea-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="e74ea-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e74ea-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="e74ea-143">UnitType</span></span><br/>     | <span data-ttu-id="e74ea-144">строка</span><span class="sxs-lookup"><span data-stu-id="e74ea-144">string</span></span><br/>  | <span data-ttu-id="e74ea-145">percent</span><span class="sxs-lookup"><span data-stu-id="e74ea-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e74ea-146">См. также</span><span class="sxs-lookup"><span data-stu-id="e74ea-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74ea-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e74ea-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




