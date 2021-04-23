---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: документбаннершитсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157cea832015c0dfb208e3f89b31ec19ac2c4313
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713329"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="c1d67-104">документбаннершитсаурце</span><span class="sxs-lookup"><span data-stu-id="c1d67-104">DocumentBannerSheetSource</span></span>

<span data-ttu-id="c1d67-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c1d67-105">This topic is not current.</span></span> <span data-ttu-id="c1d67-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c1d67-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1d67-107">Указывает источник настраиваемого таблицы заголовков.</span><span class="sxs-lookup"><span data-stu-id="c1d67-107">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="c1d67-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c1d67-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c1d67-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c1d67-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c1d67-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c1d67-110">Element Information</span></span>



| <span data-ttu-id="c1d67-111">Имя</span><span class="sxs-lookup"><span data-stu-id="c1d67-111">Name</span></span>                       |                                                  |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="c1d67-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c1d67-112">Element Type</span></span> <br/>   | <span data-ttu-id="c1d67-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="c1d67-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="c1d67-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c1d67-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c1d67-115">Документ</span><span class="sxs-lookup"><span data-stu-id="c1d67-115">Document</span></span><br/>                              |
| <span data-ttu-id="c1d67-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1d67-116">Notes</span></span> <br/>          | <span data-ttu-id="c1d67-117">Связано с элементом Документбаннершит</span><span class="sxs-lookup"><span data-stu-id="c1d67-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c1d67-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c1d67-118">Structure Content</span></span>

<span data-ttu-id="c1d67-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c1d67-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="c1d67-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="c1d67-120">Structure Properties</span></span>

<span data-ttu-id="c1d67-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c1d67-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c1d67-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1d67-122">Property</span></span>                | <span data-ttu-id="c1d67-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c1d67-123">xsi:type</span></span>           | <span data-ttu-id="c1d67-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c1d67-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c1d67-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c1d67-125">DataType</span></span><br/>     | <span data-ttu-id="c1d67-126">строка</span><span class="sxs-lookup"><span data-stu-id="c1d67-126">string</span></span><br/>  | <span data-ttu-id="c1d67-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="c1d67-127">xs:string</span></span><br/>       |
| <span data-ttu-id="c1d67-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c1d67-128">DefaultValue</span></span><br/> | <span data-ttu-id="c1d67-129">строка</span><span class="sxs-lookup"><span data-stu-id="c1d67-129">string</span></span><br/>  | <span data-ttu-id="c1d67-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c1d67-130">undefined</span></span><br/>       |
| <span data-ttu-id="c1d67-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c1d67-131">MaxLength</span></span><br/>    | <span data-ttu-id="c1d67-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="c1d67-132">integer</span></span><br/> | <span data-ttu-id="c1d67-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c1d67-133">undefined</span></span><br/>       |
| <span data-ttu-id="c1d67-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="c1d67-134">MinLength</span></span><br/>    | <span data-ttu-id="c1d67-135">целое число</span><span class="sxs-lookup"><span data-stu-id="c1d67-135">integer</span></span><br/> | <span data-ttu-id="c1d67-136">1</span><span class="sxs-lookup"><span data-stu-id="c1d67-136">1</span></span><br/>               |
| <span data-ttu-id="c1d67-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c1d67-137">Mandatory</span></span><br/>    | <span data-ttu-id="c1d67-138">строка</span><span class="sxs-lookup"><span data-stu-id="c1d67-138">string</span></span><br/>  | <span data-ttu-id="c1d67-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="c1d67-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c1d67-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="c1d67-140">UnitType</span></span><br/>     | <span data-ttu-id="c1d67-141">строка</span><span class="sxs-lookup"><span data-stu-id="c1d67-141">string</span></span><br/>  | <span data-ttu-id="c1d67-142">characters</span><span class="sxs-lookup"><span data-stu-id="c1d67-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c1d67-143">См. также</span><span class="sxs-lookup"><span data-stu-id="c1d67-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1d67-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c1d67-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




