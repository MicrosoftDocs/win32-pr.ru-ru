---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: пажеблаккженератионпроцессингграйкомпонентреплацементекстент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9a790d66d1f7806a7ef86ee4a85f62225aa836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997711"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="e71f7-104">пажеблаккженератионпроцессингграйкомпонентреплацементекстент</span><span class="sxs-lookup"><span data-stu-id="e71f7-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="e71f7-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e71f7-105">This topic is not current.</span></span> <span data-ttu-id="e71f7-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e71f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e71f7-107">Описывает экстенты, превышающие нейтральные (в цветах цветов), к которым применяется ГКР.</span><span class="sxs-lookup"><span data-stu-id="e71f7-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="e71f7-108">0% = замена универсальных компонентов, 100% = серая замена компонентов.</span><span class="sxs-lookup"><span data-stu-id="e71f7-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="e71f7-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e71f7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e71f7-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e71f7-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e71f7-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e71f7-111">Element Information</span></span>



| <span data-ttu-id="e71f7-112">Имя</span><span class="sxs-lookup"><span data-stu-id="e71f7-112">Name</span></span> | <span data-ttu-id="e71f7-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e71f7-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e71f7-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e71f7-114">Element Type</span></span> <br/>   | <span data-ttu-id="e71f7-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="e71f7-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="e71f7-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e71f7-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e71f7-117">Страница</span><span class="sxs-lookup"><span data-stu-id="e71f7-117">Page</span></span><br/>                                            |
| <span data-ttu-id="e71f7-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="e71f7-118">Notes</span></span> <br/>          | <span data-ttu-id="e71f7-119">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="e71f7-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e71f7-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e71f7-120">Structure Content</span></span>

<span data-ttu-id="e71f7-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e71f7-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e71f7-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="e71f7-122">Structure Properties</span></span>

<span data-ttu-id="e71f7-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e71f7-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e71f7-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="e71f7-124">Property</span></span>                | <span data-ttu-id="e71f7-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e71f7-125">xsi:type</span></span>           | <span data-ttu-id="e71f7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e71f7-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e71f7-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e71f7-127">DataType</span></span><br/>     | <span data-ttu-id="e71f7-128">строка</span><span class="sxs-lookup"><span data-stu-id="e71f7-128">string</span></span><br/>  | <span data-ttu-id="e71f7-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e71f7-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="e71f7-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e71f7-130">DefaultValue</span></span><br/> | <span data-ttu-id="e71f7-131">строка</span><span class="sxs-lookup"><span data-stu-id="e71f7-131">string</span></span><br/>  | <span data-ttu-id="e71f7-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e71f7-132">undefined</span></span><br/>       |
| <span data-ttu-id="e71f7-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e71f7-133">MaxValue</span></span><br/>     | <span data-ttu-id="e71f7-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="e71f7-134">integer</span></span><br/> | <span data-ttu-id="e71f7-135">100</span><span class="sxs-lookup"><span data-stu-id="e71f7-135">100</span></span><br/>             |
| <span data-ttu-id="e71f7-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="e71f7-136">MinValue</span></span><br/>     | <span data-ttu-id="e71f7-137">целое число</span><span class="sxs-lookup"><span data-stu-id="e71f7-137">integer</span></span><br/> | <span data-ttu-id="e71f7-138">0</span><span class="sxs-lookup"><span data-stu-id="e71f7-138">0</span></span><br/>               |
| <span data-ttu-id="e71f7-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="e71f7-139">Multiple</span></span><br/>     | <span data-ttu-id="e71f7-140">целое число</span><span class="sxs-lookup"><span data-stu-id="e71f7-140">integer</span></span><br/> | <span data-ttu-id="e71f7-141">1</span><span class="sxs-lookup"><span data-stu-id="e71f7-141">1</span></span><br/>               |
| <span data-ttu-id="e71f7-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e71f7-142">Mandatory</span></span><br/>    | <span data-ttu-id="e71f7-143">строка</span><span class="sxs-lookup"><span data-stu-id="e71f7-143">string</span></span><br/>  | <span data-ttu-id="e71f7-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="e71f7-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e71f7-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="e71f7-145">UnitType</span></span><br/>     | <span data-ttu-id="e71f7-146">строка</span><span class="sxs-lookup"><span data-stu-id="e71f7-146">string</span></span><br/>  | <span data-ttu-id="e71f7-147">percent</span><span class="sxs-lookup"><span data-stu-id="e71f7-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e71f7-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e71f7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e71f7-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e71f7-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




