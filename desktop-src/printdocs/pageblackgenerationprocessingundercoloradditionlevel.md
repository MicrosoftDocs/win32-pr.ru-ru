---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: пажеблаккженератионпроцессингундерколораддитионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b43d8d9ee366fc742dc3d7b1617f6297fc96e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995671"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="24418-104">пажеблаккженератионпроцессингундерколораддитионлевел</span><span class="sxs-lookup"><span data-stu-id="24418-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="24418-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="24418-105">This topic is not current.</span></span> <span data-ttu-id="24418-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="24418-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="24418-107">Описывает объемные чернила (в соотношении серых компонентов) для добавления в области, где ГКР/укр создал "Блаккинклимит" (или Укастарт, если он указан) в темных нейтральных и почти нейтральных областях.</span><span class="sxs-lookup"><span data-stu-id="24418-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="24418-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="24418-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="24418-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="24418-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="24418-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="24418-110">Element Information</span></span>



| <span data-ttu-id="24418-111">Имя</span><span class="sxs-lookup"><span data-stu-id="24418-111">Name</span></span> | <span data-ttu-id="24418-112">Значение</span><span class="sxs-lookup"><span data-stu-id="24418-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="24418-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="24418-113">Element Type</span></span> <br/>   | <span data-ttu-id="24418-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="24418-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="24418-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="24418-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="24418-116">Страница</span><span class="sxs-lookup"><span data-stu-id="24418-116">Page</span></span><br/>                                            |
| <span data-ttu-id="24418-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="24418-117">Notes</span></span> <br/>          | <span data-ttu-id="24418-118">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="24418-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="24418-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="24418-119">Structure Content</span></span>

<span data-ttu-id="24418-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="24418-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="24418-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="24418-121">Structure Properties</span></span>

<span data-ttu-id="24418-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="24418-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="24418-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="24418-123">Property</span></span>                | <span data-ttu-id="24418-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="24418-124">xsi:type</span></span>           | <span data-ttu-id="24418-125">Значение</span><span class="sxs-lookup"><span data-stu-id="24418-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="24418-126">DataType</span><span class="sxs-lookup"><span data-stu-id="24418-126">DataType</span></span><br/>     | <span data-ttu-id="24418-127">строка</span><span class="sxs-lookup"><span data-stu-id="24418-127">string</span></span><br/>  | <span data-ttu-id="24418-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="24418-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="24418-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="24418-129">DefaultValue</span></span><br/> | <span data-ttu-id="24418-130">строка</span><span class="sxs-lookup"><span data-stu-id="24418-130">string</span></span><br/>  | <span data-ttu-id="24418-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="24418-131">undefined</span></span><br/>       |
| <span data-ttu-id="24418-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="24418-132">MaxValue</span></span><br/>     | <span data-ttu-id="24418-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="24418-133">integer</span></span><br/> | <span data-ttu-id="24418-134">100</span><span class="sxs-lookup"><span data-stu-id="24418-134">100</span></span><br/>             |
| <span data-ttu-id="24418-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="24418-135">MinValue</span></span><br/>     | <span data-ttu-id="24418-136">целое число</span><span class="sxs-lookup"><span data-stu-id="24418-136">integer</span></span><br/> | <span data-ttu-id="24418-137">0</span><span class="sxs-lookup"><span data-stu-id="24418-137">0</span></span><br/>               |
| <span data-ttu-id="24418-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="24418-138">Multiple</span></span><br/>     | <span data-ttu-id="24418-139">целое число</span><span class="sxs-lookup"><span data-stu-id="24418-139">integer</span></span><br/> | <span data-ttu-id="24418-140">1</span><span class="sxs-lookup"><span data-stu-id="24418-140">1</span></span><br/>               |
| <span data-ttu-id="24418-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="24418-141">Mandatory</span></span><br/>    | <span data-ttu-id="24418-142">строка</span><span class="sxs-lookup"><span data-stu-id="24418-142">string</span></span><br/>  | <span data-ttu-id="24418-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="24418-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="24418-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="24418-144">UnitType</span></span><br/>     | <span data-ttu-id="24418-145">строка</span><span class="sxs-lookup"><span data-stu-id="24418-145">string</span></span><br/>  | <span data-ttu-id="24418-146">percent</span><span class="sxs-lookup"><span data-stu-id="24418-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="24418-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="24418-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24418-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="24418-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




