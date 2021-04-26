---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: пажеблаккженератионпроцессингграйкомпонентреплацементстарт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2608535c65cbde04005334ed970c0d27cb1feffb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996181"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="fcddf-104">пажеблаккженератионпроцессингграйкомпонентреплацементстарт</span><span class="sxs-lookup"><span data-stu-id="fcddf-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="fcddf-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="fcddf-105">This topic is not current.</span></span> <span data-ttu-id="fcddf-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fcddf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fcddf-107">Описывает точку в диапазоне "выделить в тень", где должно запускаться ГКР (100% темно-темная тень).</span><span class="sxs-lookup"><span data-stu-id="fcddf-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="fcddf-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fcddf-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fcddf-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="fcddf-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fcddf-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fcddf-110">Element Information</span></span>



| <span data-ttu-id="fcddf-111">Имя</span><span class="sxs-lookup"><span data-stu-id="fcddf-111">Name</span></span> | <span data-ttu-id="fcddf-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fcddf-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="fcddf-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="fcddf-113">Element Type</span></span> <br/>   | <span data-ttu-id="fcddf-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="fcddf-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="fcddf-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="fcddf-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fcddf-116">Страница</span><span class="sxs-lookup"><span data-stu-id="fcddf-116">Page</span></span><br/>                                            |
| <span data-ttu-id="fcddf-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="fcddf-117">Notes</span></span> <br/>          | <span data-ttu-id="fcddf-118">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="fcddf-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fcddf-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="fcddf-119">Structure Content</span></span>

<span data-ttu-id="fcddf-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="fcddf-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fcddf-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="fcddf-121">Structure Properties</span></span>

<span data-ttu-id="fcddf-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="fcddf-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fcddf-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="fcddf-123">Property</span></span>                | <span data-ttu-id="fcddf-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fcddf-124">xsi:type</span></span>           | <span data-ttu-id="fcddf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fcddf-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fcddf-126">DataType</span><span class="sxs-lookup"><span data-stu-id="fcddf-126">DataType</span></span><br/>     | <span data-ttu-id="fcddf-127">строка</span><span class="sxs-lookup"><span data-stu-id="fcddf-127">string</span></span><br/>  | <span data-ttu-id="fcddf-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fcddf-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="fcddf-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fcddf-129">DefaultValue</span></span><br/> | <span data-ttu-id="fcddf-130">строка</span><span class="sxs-lookup"><span data-stu-id="fcddf-130">string</span></span><br/>  | <span data-ttu-id="fcddf-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="fcddf-131">undefined</span></span><br/>       |
| <span data-ttu-id="fcddf-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fcddf-132">MaxValue</span></span><br/>     | <span data-ttu-id="fcddf-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="fcddf-133">integer</span></span><br/> | <span data-ttu-id="fcddf-134">100</span><span class="sxs-lookup"><span data-stu-id="fcddf-134">100</span></span><br/>             |
| <span data-ttu-id="fcddf-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="fcddf-135">MinValue</span></span><br/>     | <span data-ttu-id="fcddf-136">целое число</span><span class="sxs-lookup"><span data-stu-id="fcddf-136">integer</span></span><br/> | <span data-ttu-id="fcddf-137">0</span><span class="sxs-lookup"><span data-stu-id="fcddf-137">0</span></span><br/>               |
| <span data-ttu-id="fcddf-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="fcddf-138">Multiple</span></span><br/>     | <span data-ttu-id="fcddf-139">целое число</span><span class="sxs-lookup"><span data-stu-id="fcddf-139">integer</span></span><br/> | <span data-ttu-id="fcddf-140">1</span><span class="sxs-lookup"><span data-stu-id="fcddf-140">1</span></span><br/>               |
| <span data-ttu-id="fcddf-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fcddf-141">Mandatory</span></span><br/>    | <span data-ttu-id="fcddf-142">строка</span><span class="sxs-lookup"><span data-stu-id="fcddf-142">string</span></span><br/>  | <span data-ttu-id="fcddf-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="fcddf-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fcddf-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="fcddf-144">UnitType</span></span><br/>     | <span data-ttu-id="fcddf-145">строка</span><span class="sxs-lookup"><span data-stu-id="fcddf-145">string</span></span><br/>  | <span data-ttu-id="fcddf-146">percent</span><span class="sxs-lookup"><span data-stu-id="fcddf-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fcddf-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fcddf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcddf-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="fcddf-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




