---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: документпажеранжес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351805"
---
# <a name="documentpageranges"></a><span data-ttu-id="3144c-104">документпажеранжес</span><span class="sxs-lookup"><span data-stu-id="3144c-104">DocumentPageRanges</span></span>

<span data-ttu-id="3144c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="3144c-105">This topic is not current.</span></span> <span data-ttu-id="3144c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3144c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3144c-107">Описывает диапазон выходных данных документа на страницах.</span><span class="sxs-lookup"><span data-stu-id="3144c-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="3144c-108">Значение параметра должно соответствовать следующей структуре:</span><span class="sxs-lookup"><span data-stu-id="3144c-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="3144c-109">Пажеранжетекст: "*пажеранже*" или "*пажеранже*,*пажеранже*"</span><span class="sxs-lookup"><span data-stu-id="3144c-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="3144c-110">Пажеранже: "*PageNumber*" или "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="3144c-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="3144c-111">PageNumber: от 1 до N, где N — число страниц в документе.</span><span class="sxs-lookup"><span data-stu-id="3144c-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="3144c-112">Если *PageNumber* > n, то *PageNumber* = n.</span><span class="sxs-lookup"><span data-stu-id="3144c-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="3144c-113">Пробелы в строке следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="3144c-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="3144c-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3144c-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3144c-115">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3144c-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="3144c-116">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3144c-116">Element Information</span></span>



| <span data-ttu-id="3144c-117">Имя</span><span class="sxs-lookup"><span data-stu-id="3144c-117">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="3144c-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="3144c-118">Element Type</span></span> <br/>   | <span data-ttu-id="3144c-119">параметердеф</span><span class="sxs-lookup"><span data-stu-id="3144c-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="3144c-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="3144c-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3144c-121">Документ</span><span class="sxs-lookup"><span data-stu-id="3144c-121">Document</span></span><br/>     |
| <span data-ttu-id="3144c-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="3144c-122">Notes</span></span> <br/>          | <span data-ttu-id="3144c-123">Нет</span><span class="sxs-lookup"><span data-stu-id="3144c-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="3144c-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3144c-124">Structural Content</span></span>

<span data-ttu-id="3144c-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="3144c-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3144c-126">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="3144c-126">Structure Properties</span></span>

<span data-ttu-id="3144c-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="3144c-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3144c-128">Свойство</span><span class="sxs-lookup"><span data-stu-id="3144c-128">Property</span></span>                | <span data-ttu-id="3144c-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3144c-129">xsi:type</span></span>           | <span data-ttu-id="3144c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3144c-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3144c-131">DataType</span><span class="sxs-lookup"><span data-stu-id="3144c-131">DataType</span></span><br/>     | <span data-ttu-id="3144c-132">строка</span><span class="sxs-lookup"><span data-stu-id="3144c-132">string</span></span><br/>  | <span data-ttu-id="3144c-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="3144c-133">xs:string</span></span><br/>       |
| <span data-ttu-id="3144c-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3144c-134">DefaultValue</span></span><br/> | <span data-ttu-id="3144c-135">строка</span><span class="sxs-lookup"><span data-stu-id="3144c-135">string</span></span><br/>  | <span data-ttu-id="3144c-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="3144c-136">undefined</span></span><br/>       |
| <span data-ttu-id="3144c-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3144c-137">MaxLength</span></span><br/>    | <span data-ttu-id="3144c-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="3144c-138">integer</span></span><br/> | <span data-ttu-id="3144c-139">неопределенный</span><span class="sxs-lookup"><span data-stu-id="3144c-139">undefined</span></span><br/>       |
| <span data-ttu-id="3144c-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="3144c-140">MinLength</span></span><br/>    | <span data-ttu-id="3144c-141">целое число</span><span class="sxs-lookup"><span data-stu-id="3144c-141">integer</span></span><br/> | <span data-ttu-id="3144c-142">1</span><span class="sxs-lookup"><span data-stu-id="3144c-142">1</span></span><br/>               |
| <span data-ttu-id="3144c-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3144c-143">Mandatory</span></span><br/>    | <span data-ttu-id="3144c-144">строка</span><span class="sxs-lookup"><span data-stu-id="3144c-144">string</span></span><br/>  | <span data-ttu-id="3144c-145">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="3144c-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3144c-146">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="3144c-146">UnitType</span></span><br/>     | <span data-ttu-id="3144c-147">строка</span><span class="sxs-lookup"><span data-stu-id="3144c-147">string</span></span><br/>  | <span data-ttu-id="3144c-148">characters</span><span class="sxs-lookup"><span data-stu-id="3144c-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3144c-149">См. также</span><span class="sxs-lookup"><span data-stu-id="3144c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3144c-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="3144c-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




