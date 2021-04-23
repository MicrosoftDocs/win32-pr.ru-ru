---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: пажеблаккженератионпроцессингтоталинкковеражелимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07566926c2115855ea7321af90e7d1caebcd0a82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664849"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="f3e83-104">пажеблаккженератионпроцессингтоталинкковеражелимит</span><span class="sxs-lookup"><span data-stu-id="f3e83-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="f3e83-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f3e83-105">This topic is not current.</span></span> <span data-ttu-id="f3e83-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f3e83-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f3e83-107">Указывает максимально допустимую сумму четырех объемов рукописного ввода в любом месте изображения.</span><span class="sxs-lookup"><span data-stu-id="f3e83-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="f3e83-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f3e83-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f3e83-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f3e83-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f3e83-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f3e83-110">Element Information</span></span>



| <span data-ttu-id="f3e83-111">Имя</span><span class="sxs-lookup"><span data-stu-id="f3e83-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="f3e83-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f3e83-112">Element Type</span></span> <br/>   | <span data-ttu-id="f3e83-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="f3e83-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="f3e83-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f3e83-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f3e83-115">Страница</span><span class="sxs-lookup"><span data-stu-id="f3e83-115">Page</span></span><br/>                                            |
| <span data-ttu-id="f3e83-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3e83-116">Notes</span></span> <br/>          | <span data-ttu-id="f3e83-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="f3e83-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f3e83-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f3e83-118">Structure Content</span></span>

<span data-ttu-id="f3e83-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f3e83-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="f3e83-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="f3e83-120">Structure Properties</span></span>

<span data-ttu-id="f3e83-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f3e83-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f3e83-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="f3e83-122">Property</span></span>                | <span data-ttu-id="f3e83-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f3e83-123">xsi:type</span></span>           | <span data-ttu-id="f3e83-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f3e83-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f3e83-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f3e83-125">DataType</span></span><br/>     | <span data-ttu-id="f3e83-126">строка</span><span class="sxs-lookup"><span data-stu-id="f3e83-126">string</span></span><br/>  | <span data-ttu-id="f3e83-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f3e83-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f3e83-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f3e83-128">DefaultValue</span></span><br/> | <span data-ttu-id="f3e83-129">строка</span><span class="sxs-lookup"><span data-stu-id="f3e83-129">string</span></span><br/>  | <span data-ttu-id="f3e83-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="f3e83-130">undefined</span></span><br/>       |
| <span data-ttu-id="f3e83-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f3e83-131">MaxValue</span></span><br/>     | <span data-ttu-id="f3e83-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="f3e83-132">integer</span></span><br/> | <span data-ttu-id="f3e83-133">400</span><span class="sxs-lookup"><span data-stu-id="f3e83-133">400</span></span><br/>             |
| <span data-ttu-id="f3e83-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f3e83-134">MinValue</span></span><br/>     | <span data-ttu-id="f3e83-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="f3e83-135">integer</span></span><br/> | <span data-ttu-id="f3e83-136">200</span><span class="sxs-lookup"><span data-stu-id="f3e83-136">200</span></span><br/>             |
| <span data-ttu-id="f3e83-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="f3e83-137">Multiple</span></span><br/>     | <span data-ttu-id="f3e83-138">целое число</span><span class="sxs-lookup"><span data-stu-id="f3e83-138">integer</span></span><br/> | <span data-ttu-id="f3e83-139">1</span><span class="sxs-lookup"><span data-stu-id="f3e83-139">1</span></span><br/>               |
| <span data-ttu-id="f3e83-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f3e83-140">Mandatory</span></span><br/>    | <span data-ttu-id="f3e83-141">строка</span><span class="sxs-lookup"><span data-stu-id="f3e83-141">string</span></span><br/>  | <span data-ttu-id="f3e83-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="f3e83-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f3e83-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="f3e83-143">UnitType</span></span><br/>     | <span data-ttu-id="f3e83-144">строка</span><span class="sxs-lookup"><span data-stu-id="f3e83-144">string</span></span><br/>  | <span data-ttu-id="f3e83-145">percent</span><span class="sxs-lookup"><span data-stu-id="f3e83-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f3e83-146">См. также</span><span class="sxs-lookup"><span data-stu-id="f3e83-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3e83-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f3e83-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




