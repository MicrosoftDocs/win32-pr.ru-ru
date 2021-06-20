---
description: Параметр Пажеблаккженератионпроцессингграйкомпонентреплацементекстент описывает экстенты, которые выходят за рамки нейтральных цветов, к цветам цвета, которые применяются ГКР.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: пажеблаккженератионпроцессингграйкомпонентреплацементекстент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3bd5e4fdbafba97884a7aed608b23e4c26ce1c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408507"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="5b0b8-103">пажеблаккженератионпроцессингграйкомпонентреплацементекстент</span><span class="sxs-lookup"><span data-stu-id="5b0b8-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="5b0b8-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5b0b8-104">This topic is not current.</span></span> <span data-ttu-id="5b0b8-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5b0b8-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5b0b8-106">Описывает экстенты, превышающие нейтральные (в цветах цветов), к которым применяется ГКР.</span><span class="sxs-lookup"><span data-stu-id="5b0b8-106">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="5b0b8-107">0% = замена универсальных компонентов, 100% = серая замена компонентов.</span><span class="sxs-lookup"><span data-stu-id="5b0b8-107">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="5b0b8-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5b0b8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5b0b8-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="5b0b8-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5b0b8-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5b0b8-110">Element Information</span></span>



| <span data-ttu-id="5b0b8-111">Имя</span><span class="sxs-lookup"><span data-stu-id="5b0b8-111">Name</span></span> | <span data-ttu-id="5b0b8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5b0b8-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5b0b8-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5b0b8-113">Element Type</span></span> <br/>   | <span data-ttu-id="5b0b8-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="5b0b8-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5b0b8-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5b0b8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5b0b8-116">Страница</span><span class="sxs-lookup"><span data-stu-id="5b0b8-116">Page</span></span><br/>                                            |
| <span data-ttu-id="5b0b8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b0b8-117">Notes</span></span> <br/>          | <span data-ttu-id="5b0b8-118">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="5b0b8-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5b0b8-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="5b0b8-119">Structure Content</span></span>

<span data-ttu-id="5b0b8-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="5b0b8-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5b0b8-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="5b0b8-121">Structure Properties</span></span>

<span data-ttu-id="5b0b8-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5b0b8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5b0b8-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="5b0b8-123">Property</span></span>                | <span data-ttu-id="5b0b8-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5b0b8-124">xsi:type</span></span>           | <span data-ttu-id="5b0b8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5b0b8-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5b0b8-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5b0b8-126">DataType</span></span><br/>     | <span data-ttu-id="5b0b8-127">строка</span><span class="sxs-lookup"><span data-stu-id="5b0b8-127">string</span></span><br/>  | <span data-ttu-id="5b0b8-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b0b8-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5b0b8-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5b0b8-129">DefaultValue</span></span><br/> | <span data-ttu-id="5b0b8-130">строка</span><span class="sxs-lookup"><span data-stu-id="5b0b8-130">string</span></span><br/>  | <span data-ttu-id="5b0b8-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="5b0b8-131">undefined</span></span><br/>       |
| <span data-ttu-id="5b0b8-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5b0b8-132">MaxValue</span></span><br/>     | <span data-ttu-id="5b0b8-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="5b0b8-133">integer</span></span><br/> | <span data-ttu-id="5b0b8-134">100</span><span class="sxs-lookup"><span data-stu-id="5b0b8-134">100</span></span><br/>             |
| <span data-ttu-id="5b0b8-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5b0b8-135">MinValue</span></span><br/>     | <span data-ttu-id="5b0b8-136">целое число</span><span class="sxs-lookup"><span data-stu-id="5b0b8-136">integer</span></span><br/> | <span data-ttu-id="5b0b8-137">0</span><span class="sxs-lookup"><span data-stu-id="5b0b8-137">0</span></span><br/>               |
| <span data-ttu-id="5b0b8-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="5b0b8-138">Multiple</span></span><br/>     | <span data-ttu-id="5b0b8-139">целое число</span><span class="sxs-lookup"><span data-stu-id="5b0b8-139">integer</span></span><br/> | <span data-ttu-id="5b0b8-140">1</span><span class="sxs-lookup"><span data-stu-id="5b0b8-140">1</span></span><br/>               |
| <span data-ttu-id="5b0b8-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5b0b8-141">Mandatory</span></span><br/>    | <span data-ttu-id="5b0b8-142">строка</span><span class="sxs-lookup"><span data-stu-id="5b0b8-142">string</span></span><br/>  | <span data-ttu-id="5b0b8-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="5b0b8-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5b0b8-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="5b0b8-144">UnitType</span></span><br/>     | <span data-ttu-id="5b0b8-145">строка</span><span class="sxs-lookup"><span data-stu-id="5b0b8-145">string</span></span><br/>  | <span data-ttu-id="5b0b8-146">percent</span><span class="sxs-lookup"><span data-stu-id="5b0b8-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5b0b8-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5b0b8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b0b8-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5b0b8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




