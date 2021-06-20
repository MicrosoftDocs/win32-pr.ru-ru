---
description: Сведения об элементе Пажеблаккженератионпроцессингтоталинкковеражелимит, который указывает максимально допустимую сумму четырех объемов рукописного ввода в любом месте изображения.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: пажеблаккженератионпроцессингтоталинкковеражелимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408447"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="dcb0d-103">пажеблаккженератионпроцессингтоталинкковеражелимит</span><span class="sxs-lookup"><span data-stu-id="dcb0d-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="dcb0d-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-104">This topic is not current.</span></span> <span data-ttu-id="dcb0d-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dcb0d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dcb0d-106">Указывает максимально допустимую сумму четырех объемов рукописного ввода в любом месте изображения.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="dcb0d-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dcb0d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dcb0d-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="dcb0d-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dcb0d-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dcb0d-109">Element Information</span></span>



| <span data-ttu-id="dcb0d-110">Имя</span><span class="sxs-lookup"><span data-stu-id="dcb0d-110">Name</span></span> | <span data-ttu-id="dcb0d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb0d-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="dcb0d-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="dcb0d-112">Element Type</span></span> <br/>   | <span data-ttu-id="dcb0d-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="dcb0d-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="dcb0d-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="dcb0d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dcb0d-115">Страница</span><span class="sxs-lookup"><span data-stu-id="dcb0d-115">Page</span></span><br/>                                            |
| <span data-ttu-id="dcb0d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="dcb0d-116">Notes</span></span> <br/>          | <span data-ttu-id="dcb0d-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="dcb0d-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dcb0d-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="dcb0d-118">Structure Content</span></span>

<span data-ttu-id="dcb0d-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="dcb0d-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="dcb0d-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="dcb0d-120">Structure Properties</span></span>

<span data-ttu-id="dcb0d-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dcb0d-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="dcb0d-122">Property</span></span>                | <span data-ttu-id="dcb0d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dcb0d-123">xsi:type</span></span>           | <span data-ttu-id="dcb0d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb0d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dcb0d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="dcb0d-125">DataType</span></span><br/>     | <span data-ttu-id="dcb0d-126">строка</span><span class="sxs-lookup"><span data-stu-id="dcb0d-126">string</span></span><br/>  | <span data-ttu-id="dcb0d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dcb0d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="dcb0d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dcb0d-128">DefaultValue</span></span><br/> | <span data-ttu-id="dcb0d-129">строка</span><span class="sxs-lookup"><span data-stu-id="dcb0d-129">string</span></span><br/>  | <span data-ttu-id="dcb0d-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="dcb0d-130">undefined</span></span><br/>       |
| <span data-ttu-id="dcb0d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dcb0d-131">MaxValue</span></span><br/>     | <span data-ttu-id="dcb0d-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="dcb0d-132">integer</span></span><br/> | <span data-ttu-id="dcb0d-133">400</span><span class="sxs-lookup"><span data-stu-id="dcb0d-133">400</span></span><br/>             |
| <span data-ttu-id="dcb0d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="dcb0d-134">MinValue</span></span><br/>     | <span data-ttu-id="dcb0d-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="dcb0d-135">integer</span></span><br/> | <span data-ttu-id="dcb0d-136">200</span><span class="sxs-lookup"><span data-stu-id="dcb0d-136">200</span></span><br/>             |
| <span data-ttu-id="dcb0d-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="dcb0d-137">Multiple</span></span><br/>     | <span data-ttu-id="dcb0d-138">целое число</span><span class="sxs-lookup"><span data-stu-id="dcb0d-138">integer</span></span><br/> | <span data-ttu-id="dcb0d-139">1</span><span class="sxs-lookup"><span data-stu-id="dcb0d-139">1</span></span><br/>               |
| <span data-ttu-id="dcb0d-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dcb0d-140">Mandatory</span></span><br/>    | <span data-ttu-id="dcb0d-141">строка</span><span class="sxs-lookup"><span data-stu-id="dcb0d-141">string</span></span><br/>  | <span data-ttu-id="dcb0d-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="dcb0d-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dcb0d-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="dcb0d-143">UnitType</span></span><br/>     | <span data-ttu-id="dcb0d-144">строка</span><span class="sxs-lookup"><span data-stu-id="dcb0d-144">string</span></span><br/>  | <span data-ttu-id="dcb0d-145">percent</span><span class="sxs-lookup"><span data-stu-id="dcb0d-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dcb0d-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dcb0d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcb0d-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="dcb0d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




