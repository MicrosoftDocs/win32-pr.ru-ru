---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: документпажеранжес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997181"
---
# <a name="documentpageranges"></a><span data-ttu-id="fa4fd-104">документпажеранжес</span><span class="sxs-lookup"><span data-stu-id="fa4fd-104">DocumentPageRanges</span></span>

<span data-ttu-id="fa4fd-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="fa4fd-105">This topic is not current.</span></span> <span data-ttu-id="fa4fd-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fa4fd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fa4fd-107">Описывает диапазон выходных данных документа на страницах.</span><span class="sxs-lookup"><span data-stu-id="fa4fd-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="fa4fd-108">Значение параметра должно соответствовать следующей структуре:</span><span class="sxs-lookup"><span data-stu-id="fa4fd-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="fa4fd-109">Пажеранжетекст: "*пажеранже*" или "*пажеранже*,*пажеранже*"</span><span class="sxs-lookup"><span data-stu-id="fa4fd-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="fa4fd-110">Пажеранже: "*PageNumber*" или "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="fa4fd-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="fa4fd-111">PageNumber: от 1 до N, где N — число страниц в документе.</span><span class="sxs-lookup"><span data-stu-id="fa4fd-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="fa4fd-112">Если *PageNumber* > n, то *PageNumber* = n.</span><span class="sxs-lookup"><span data-stu-id="fa4fd-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="fa4fd-113">Пробелы в строке следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="fa4fd-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="fa4fd-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fa4fd-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fa4fd-115">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="fa4fd-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="fa4fd-116">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fa4fd-116">Element Information</span></span>



| <span data-ttu-id="fa4fd-117">Имя</span><span class="sxs-lookup"><span data-stu-id="fa4fd-117">Name</span></span> | <span data-ttu-id="fa4fd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fa4fd-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="fa4fd-119">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="fa4fd-119">Element Type</span></span> <br/>   | <span data-ttu-id="fa4fd-120">параметердеф</span><span class="sxs-lookup"><span data-stu-id="fa4fd-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="fa4fd-121">Префикс области</span><span class="sxs-lookup"><span data-stu-id="fa4fd-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fa4fd-122">Документ</span><span class="sxs-lookup"><span data-stu-id="fa4fd-122">Document</span></span><br/>     |
| <span data-ttu-id="fa4fd-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa4fd-123">Notes</span></span> <br/>          | <span data-ttu-id="fa4fd-124">Нет</span><span class="sxs-lookup"><span data-stu-id="fa4fd-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="fa4fd-125">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="fa4fd-125">Structural Content</span></span>

<span data-ttu-id="fa4fd-126">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="fa4fd-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="fa4fd-127">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="fa4fd-127">Structure Properties</span></span>

<span data-ttu-id="fa4fd-128">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="fa4fd-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fa4fd-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="fa4fd-129">Property</span></span>                | <span data-ttu-id="fa4fd-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fa4fd-130">xsi:type</span></span>           | <span data-ttu-id="fa4fd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fa4fd-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fa4fd-132">DataType</span><span class="sxs-lookup"><span data-stu-id="fa4fd-132">DataType</span></span><br/>     | <span data-ttu-id="fa4fd-133">строка</span><span class="sxs-lookup"><span data-stu-id="fa4fd-133">string</span></span><br/>  | <span data-ttu-id="fa4fd-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa4fd-134">xs:string</span></span><br/>       |
| <span data-ttu-id="fa4fd-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fa4fd-135">DefaultValue</span></span><br/> | <span data-ttu-id="fa4fd-136">строка</span><span class="sxs-lookup"><span data-stu-id="fa4fd-136">string</span></span><br/>  | <span data-ttu-id="fa4fd-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="fa4fd-137">undefined</span></span><br/>       |
| <span data-ttu-id="fa4fd-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fa4fd-138">MaxLength</span></span><br/>    | <span data-ttu-id="fa4fd-139">Целое число</span><span class="sxs-lookup"><span data-stu-id="fa4fd-139">integer</span></span><br/> | <span data-ttu-id="fa4fd-140">неопределенный</span><span class="sxs-lookup"><span data-stu-id="fa4fd-140">undefined</span></span><br/>       |
| <span data-ttu-id="fa4fd-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="fa4fd-141">MinLength</span></span><br/>    | <span data-ttu-id="fa4fd-142">целое число</span><span class="sxs-lookup"><span data-stu-id="fa4fd-142">integer</span></span><br/> | <span data-ttu-id="fa4fd-143">1</span><span class="sxs-lookup"><span data-stu-id="fa4fd-143">1</span></span><br/>               |
| <span data-ttu-id="fa4fd-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fa4fd-144">Mandatory</span></span><br/>    | <span data-ttu-id="fa4fd-145">строка</span><span class="sxs-lookup"><span data-stu-id="fa4fd-145">string</span></span><br/>  | <span data-ttu-id="fa4fd-146">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="fa4fd-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fa4fd-147">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="fa4fd-147">UnitType</span></span><br/>     | <span data-ttu-id="fa4fd-148">строка</span><span class="sxs-lookup"><span data-stu-id="fa4fd-148">string</span></span><br/>  | <span data-ttu-id="fa4fd-149">characters</span><span class="sxs-lookup"><span data-stu-id="fa4fd-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fa4fd-150">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fa4fd-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa4fd-151">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="fa4fd-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




