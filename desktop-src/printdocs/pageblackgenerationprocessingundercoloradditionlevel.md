---
description: Сведения об элементе Пажеблаккженератионпроцессингундерколораддитионлевел, описывающем объемную краску, добавляемую в области с помощью Блаккинклимит.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: пажеблаккженератионпроцессингундерколораддитионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b496fbe890f53d1da8d1054cc5a19fe6318811
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408417"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="56f61-103">пажеблаккженератионпроцессингундерколораддитионлевел</span><span class="sxs-lookup"><span data-stu-id="56f61-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="56f61-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="56f61-104">This topic is not current.</span></span> <span data-ttu-id="56f61-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56f61-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56f61-106">Описывает объемные чернила (в соотношении серых компонентов) для добавления в области, где ГКР/укр создал "Блаккинклимит" (или Укастарт, если он указан) в темных нейтральных и почти нейтральных областях.</span><span class="sxs-lookup"><span data-stu-id="56f61-106">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="56f61-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="56f61-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56f61-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="56f61-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="56f61-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="56f61-109">Element Information</span></span>



| <span data-ttu-id="56f61-110">Имя</span><span class="sxs-lookup"><span data-stu-id="56f61-110">Name</span></span> | <span data-ttu-id="56f61-111">Значение</span><span class="sxs-lookup"><span data-stu-id="56f61-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="56f61-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="56f61-112">Element Type</span></span> <br/>   | <span data-ttu-id="56f61-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="56f61-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="56f61-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="56f61-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56f61-115">Страница</span><span class="sxs-lookup"><span data-stu-id="56f61-115">Page</span></span><br/>                                            |
| <span data-ttu-id="56f61-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="56f61-116">Notes</span></span> <br/>          | <span data-ttu-id="56f61-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="56f61-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="56f61-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="56f61-118">Structure Content</span></span>

<span data-ttu-id="56f61-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="56f61-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="56f61-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="56f61-120">Structure Properties</span></span>

<span data-ttu-id="56f61-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="56f61-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56f61-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="56f61-122">Property</span></span>                | <span data-ttu-id="56f61-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="56f61-123">xsi:type</span></span>           | <span data-ttu-id="56f61-124">Значение</span><span class="sxs-lookup"><span data-stu-id="56f61-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="56f61-125">DataType</span><span class="sxs-lookup"><span data-stu-id="56f61-125">DataType</span></span><br/>     | <span data-ttu-id="56f61-126">строка</span><span class="sxs-lookup"><span data-stu-id="56f61-126">string</span></span><br/>  | <span data-ttu-id="56f61-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="56f61-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="56f61-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="56f61-128">DefaultValue</span></span><br/> | <span data-ttu-id="56f61-129">строка</span><span class="sxs-lookup"><span data-stu-id="56f61-129">string</span></span><br/>  | <span data-ttu-id="56f61-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="56f61-130">undefined</span></span><br/>       |
| <span data-ttu-id="56f61-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="56f61-131">MaxValue</span></span><br/>     | <span data-ttu-id="56f61-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="56f61-132">integer</span></span><br/> | <span data-ttu-id="56f61-133">100</span><span class="sxs-lookup"><span data-stu-id="56f61-133">100</span></span><br/>             |
| <span data-ttu-id="56f61-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="56f61-134">MinValue</span></span><br/>     | <span data-ttu-id="56f61-135">целое число</span><span class="sxs-lookup"><span data-stu-id="56f61-135">integer</span></span><br/> | <span data-ttu-id="56f61-136">0</span><span class="sxs-lookup"><span data-stu-id="56f61-136">0</span></span><br/>               |
| <span data-ttu-id="56f61-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="56f61-137">Multiple</span></span><br/>     | <span data-ttu-id="56f61-138">целое число</span><span class="sxs-lookup"><span data-stu-id="56f61-138">integer</span></span><br/> | <span data-ttu-id="56f61-139">1</span><span class="sxs-lookup"><span data-stu-id="56f61-139">1</span></span><br/>               |
| <span data-ttu-id="56f61-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56f61-140">Mandatory</span></span><br/>    | <span data-ttu-id="56f61-141">строка</span><span class="sxs-lookup"><span data-stu-id="56f61-141">string</span></span><br/>  | <span data-ttu-id="56f61-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="56f61-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="56f61-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="56f61-143">UnitType</span></span><br/>     | <span data-ttu-id="56f61-144">строка</span><span class="sxs-lookup"><span data-stu-id="56f61-144">string</span></span><br/>  | <span data-ttu-id="56f61-145">percent</span><span class="sxs-lookup"><span data-stu-id="56f61-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="56f61-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="56f61-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f61-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="56f61-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




