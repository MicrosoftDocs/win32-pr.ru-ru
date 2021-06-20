---
description: Сведения об элементе Пажеблаккженератионпроцессингграйкомпонентреплацементстарт, описывающем точку, в которой должно начаться ГКР.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: пажеблаккженератионпроцессингграйкомпонентреплацементстарт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e7e5a7e22c20b15dc373a2cce2bfe19e3417d4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408467"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="7affd-103">пажеблаккженератионпроцессингграйкомпонентреплацементстарт</span><span class="sxs-lookup"><span data-stu-id="7affd-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="7affd-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7affd-104">This topic is not current.</span></span> <span data-ttu-id="7affd-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7affd-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7affd-106">Описывает точку в диапазоне "выделить в тень", где должно запускаться ГКР (100% темно-темная тень).</span><span class="sxs-lookup"><span data-stu-id="7affd-106">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="7affd-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7affd-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7affd-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7affd-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7affd-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7affd-109">Element Information</span></span>



| <span data-ttu-id="7affd-110">Имя</span><span class="sxs-lookup"><span data-stu-id="7affd-110">Name</span></span> | <span data-ttu-id="7affd-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7affd-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="7affd-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7affd-112">Element Type</span></span> <br/>   | <span data-ttu-id="7affd-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="7affd-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="7affd-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7affd-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7affd-115">Страница</span><span class="sxs-lookup"><span data-stu-id="7affd-115">Page</span></span><br/>                                            |
| <span data-ttu-id="7affd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="7affd-116">Notes</span></span> <br/>          | <span data-ttu-id="7affd-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="7affd-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7affd-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7affd-118">Structure Content</span></span>

<span data-ttu-id="7affd-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7affd-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7affd-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="7affd-120">Structure Properties</span></span>

<span data-ttu-id="7affd-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7affd-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7affd-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="7affd-122">Property</span></span>                | <span data-ttu-id="7affd-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7affd-123">xsi:type</span></span>           | <span data-ttu-id="7affd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7affd-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7affd-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7affd-125">DataType</span></span><br/>     | <span data-ttu-id="7affd-126">строка</span><span class="sxs-lookup"><span data-stu-id="7affd-126">string</span></span><br/>  | <span data-ttu-id="7affd-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7affd-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="7affd-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7affd-128">DefaultValue</span></span><br/> | <span data-ttu-id="7affd-129">строка</span><span class="sxs-lookup"><span data-stu-id="7affd-129">string</span></span><br/>  | <span data-ttu-id="7affd-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="7affd-130">undefined</span></span><br/>       |
| <span data-ttu-id="7affd-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7affd-131">MaxValue</span></span><br/>     | <span data-ttu-id="7affd-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="7affd-132">integer</span></span><br/> | <span data-ttu-id="7affd-133">100</span><span class="sxs-lookup"><span data-stu-id="7affd-133">100</span></span><br/>             |
| <span data-ttu-id="7affd-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7affd-134">MinValue</span></span><br/>     | <span data-ttu-id="7affd-135">целое число</span><span class="sxs-lookup"><span data-stu-id="7affd-135">integer</span></span><br/> | <span data-ttu-id="7affd-136">0</span><span class="sxs-lookup"><span data-stu-id="7affd-136">0</span></span><br/>               |
| <span data-ttu-id="7affd-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="7affd-137">Multiple</span></span><br/>     | <span data-ttu-id="7affd-138">целое число</span><span class="sxs-lookup"><span data-stu-id="7affd-138">integer</span></span><br/> | <span data-ttu-id="7affd-139">1</span><span class="sxs-lookup"><span data-stu-id="7affd-139">1</span></span><br/>               |
| <span data-ttu-id="7affd-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7affd-140">Mandatory</span></span><br/>    | <span data-ttu-id="7affd-141">строка</span><span class="sxs-lookup"><span data-stu-id="7affd-141">string</span></span><br/>  | <span data-ttu-id="7affd-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="7affd-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7affd-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="7affd-143">UnitType</span></span><br/>     | <span data-ttu-id="7affd-144">строка</span><span class="sxs-lookup"><span data-stu-id="7affd-144">string</span></span><br/>  | <span data-ttu-id="7affd-145">percent</span><span class="sxs-lookup"><span data-stu-id="7affd-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7affd-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7affd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7affd-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7affd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




