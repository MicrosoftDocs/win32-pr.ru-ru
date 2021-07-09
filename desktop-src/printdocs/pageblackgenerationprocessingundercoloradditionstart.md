---
title: пажеблаккженератионпроцессингундерколораддитионстарт
description: Проверьте параметр Пажеблаккженератионпроцессингундерколораддитионстарт. Этот раздел не является актуальным. Текущие сведения см. в спецификации печати схемы.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549352"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="66c96-105">пажеблаккженератионпроцессингундерколораддитионстарт</span><span class="sxs-lookup"><span data-stu-id="66c96-105">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="66c96-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="66c96-106">This topic is not current.</span></span> <span data-ttu-id="66c96-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="66c96-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="66c96-108">Описывает уровень тени, к которому будет применен ука.</span><span class="sxs-lookup"><span data-stu-id="66c96-108">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="66c96-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66c96-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="66c96-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="66c96-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="66c96-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66c96-111">Element Information</span></span>



| <span data-ttu-id="66c96-112">Имя</span><span class="sxs-lookup"><span data-stu-id="66c96-112">Name</span></span> | <span data-ttu-id="66c96-113">Значение</span><span class="sxs-lookup"><span data-stu-id="66c96-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="66c96-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="66c96-114">Element Type</span></span> <br/>   | <span data-ttu-id="66c96-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="66c96-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="66c96-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="66c96-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="66c96-117">Страница</span><span class="sxs-lookup"><span data-stu-id="66c96-117">Page</span></span><br/>                                            |
| <span data-ttu-id="66c96-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="66c96-118">Notes</span></span> <br/>          | <span data-ttu-id="66c96-119">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="66c96-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="66c96-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="66c96-120">Structure Content</span></span>

<span data-ttu-id="66c96-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="66c96-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
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

## <a name="structure-properties"></a><span data-ttu-id="66c96-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="66c96-122">Structure Properties</span></span>

<span data-ttu-id="66c96-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="66c96-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="66c96-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="66c96-124">Property</span></span>                | <span data-ttu-id="66c96-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="66c96-125">xsi:type</span></span>           | <span data-ttu-id="66c96-126">Значение</span><span class="sxs-lookup"><span data-stu-id="66c96-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="66c96-127">DataType</span><span class="sxs-lookup"><span data-stu-id="66c96-127">DataType</span></span><br/>     | <span data-ttu-id="66c96-128">строка</span><span class="sxs-lookup"><span data-stu-id="66c96-128">string</span></span><br/>  | <span data-ttu-id="66c96-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="66c96-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="66c96-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="66c96-130">DefaultValue</span></span><br/> | <span data-ttu-id="66c96-131">строка</span><span class="sxs-lookup"><span data-stu-id="66c96-131">string</span></span><br/>  | <span data-ttu-id="66c96-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="66c96-132">undefined</span></span><br/>       |
| <span data-ttu-id="66c96-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="66c96-133">MaxValue</span></span><br/>     | <span data-ttu-id="66c96-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="66c96-134">integer</span></span><br/> | <span data-ttu-id="66c96-135">100</span><span class="sxs-lookup"><span data-stu-id="66c96-135">100</span></span><br/>             |
| <span data-ttu-id="66c96-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="66c96-136">MinValue</span></span><br/>     | <span data-ttu-id="66c96-137">целое число</span><span class="sxs-lookup"><span data-stu-id="66c96-137">integer</span></span><br/> | <span data-ttu-id="66c96-138">0</span><span class="sxs-lookup"><span data-stu-id="66c96-138">0</span></span><br/>               |
| <span data-ttu-id="66c96-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="66c96-139">Multiple</span></span><br/>     | <span data-ttu-id="66c96-140">целое число</span><span class="sxs-lookup"><span data-stu-id="66c96-140">integer</span></span><br/> | <span data-ttu-id="66c96-141">1</span><span class="sxs-lookup"><span data-stu-id="66c96-141">1</span></span><br/>               |
| <span data-ttu-id="66c96-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="66c96-142">Mandatory</span></span><br/>    | <span data-ttu-id="66c96-143">строка</span><span class="sxs-lookup"><span data-stu-id="66c96-143">string</span></span><br/>  | <span data-ttu-id="66c96-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="66c96-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="66c96-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="66c96-145">UnitType</span></span><br/>     | <span data-ttu-id="66c96-146">строка</span><span class="sxs-lookup"><span data-stu-id="66c96-146">string</span></span><br/>  | <span data-ttu-id="66c96-147">percent</span><span class="sxs-lookup"><span data-stu-id="66c96-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="66c96-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="66c96-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66c96-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="66c96-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




