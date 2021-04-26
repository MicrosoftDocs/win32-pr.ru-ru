---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: пажеблаккженератионпроцессингтоталинкковеражелимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993881"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="8cf09-104">пажеблаккженератионпроцессингтоталинкковеражелимит</span><span class="sxs-lookup"><span data-stu-id="8cf09-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="8cf09-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8cf09-105">This topic is not current.</span></span> <span data-ttu-id="8cf09-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8cf09-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8cf09-107">Указывает максимально допустимую сумму четырех объемов рукописного ввода в любом месте изображения.</span><span class="sxs-lookup"><span data-stu-id="8cf09-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="8cf09-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8cf09-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8cf09-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8cf09-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8cf09-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8cf09-110">Element Information</span></span>



| <span data-ttu-id="8cf09-111">Имя</span><span class="sxs-lookup"><span data-stu-id="8cf09-111">Name</span></span> | <span data-ttu-id="8cf09-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf09-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="8cf09-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8cf09-113">Element Type</span></span> <br/>   | <span data-ttu-id="8cf09-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="8cf09-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="8cf09-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8cf09-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8cf09-116">Страница</span><span class="sxs-lookup"><span data-stu-id="8cf09-116">Page</span></span><br/>                                            |
| <span data-ttu-id="8cf09-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="8cf09-117">Notes</span></span> <br/>          | <span data-ttu-id="8cf09-118">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="8cf09-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8cf09-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8cf09-119">Structure Content</span></span>

<span data-ttu-id="8cf09-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8cf09-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8cf09-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="8cf09-121">Structure Properties</span></span>

<span data-ttu-id="8cf09-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8cf09-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8cf09-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="8cf09-123">Property</span></span>                | <span data-ttu-id="8cf09-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8cf09-124">xsi:type</span></span>           | <span data-ttu-id="8cf09-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf09-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8cf09-126">DataType</span><span class="sxs-lookup"><span data-stu-id="8cf09-126">DataType</span></span><br/>     | <span data-ttu-id="8cf09-127">строка</span><span class="sxs-lookup"><span data-stu-id="8cf09-127">string</span></span><br/>  | <span data-ttu-id="8cf09-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8cf09-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="8cf09-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8cf09-129">DefaultValue</span></span><br/> | <span data-ttu-id="8cf09-130">строка</span><span class="sxs-lookup"><span data-stu-id="8cf09-130">string</span></span><br/>  | <span data-ttu-id="8cf09-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8cf09-131">undefined</span></span><br/>       |
| <span data-ttu-id="8cf09-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8cf09-132">MaxValue</span></span><br/>     | <span data-ttu-id="8cf09-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="8cf09-133">integer</span></span><br/> | <span data-ttu-id="8cf09-134">400</span><span class="sxs-lookup"><span data-stu-id="8cf09-134">400</span></span><br/>             |
| <span data-ttu-id="8cf09-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="8cf09-135">MinValue</span></span><br/>     | <span data-ttu-id="8cf09-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="8cf09-136">integer</span></span><br/> | <span data-ttu-id="8cf09-137">200</span><span class="sxs-lookup"><span data-stu-id="8cf09-137">200</span></span><br/>             |
| <span data-ttu-id="8cf09-138">Несколько</span><span class="sxs-lookup"><span data-stu-id="8cf09-138">Multiple</span></span><br/>     | <span data-ttu-id="8cf09-139">целое число</span><span class="sxs-lookup"><span data-stu-id="8cf09-139">integer</span></span><br/> | <span data-ttu-id="8cf09-140">1</span><span class="sxs-lookup"><span data-stu-id="8cf09-140">1</span></span><br/>               |
| <span data-ttu-id="8cf09-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8cf09-141">Mandatory</span></span><br/>    | <span data-ttu-id="8cf09-142">строка</span><span class="sxs-lookup"><span data-stu-id="8cf09-142">string</span></span><br/>  | <span data-ttu-id="8cf09-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="8cf09-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8cf09-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="8cf09-144">UnitType</span></span><br/>     | <span data-ttu-id="8cf09-145">строка</span><span class="sxs-lookup"><span data-stu-id="8cf09-145">string</span></span><br/>  | <span data-ttu-id="8cf09-146">percent</span><span class="sxs-lookup"><span data-stu-id="8cf09-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8cf09-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8cf09-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf09-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8cf09-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




