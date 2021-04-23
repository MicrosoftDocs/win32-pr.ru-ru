---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: документковерфронтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f67ab3f3dc3515a494dad2ab72f1413de88cd00
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273333"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="f597a-104">документковерфронтсаурце</span><span class="sxs-lookup"><span data-stu-id="f597a-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="f597a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f597a-105">This topic is not current.</span></span> <span data-ttu-id="f597a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f597a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f597a-107">Указывает источник пользовательского внешнего титульного листа.</span><span class="sxs-lookup"><span data-stu-id="f597a-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="f597a-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f597a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f597a-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f597a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f597a-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f597a-110">Element Information</span></span>



| <span data-ttu-id="f597a-111">Имя</span><span class="sxs-lookup"><span data-stu-id="f597a-111">Name</span></span>                       |                                                 |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="f597a-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f597a-112">Element Type</span></span> <br/>   | <span data-ttu-id="f597a-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="f597a-113">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="f597a-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f597a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f597a-115">Документ</span><span class="sxs-lookup"><span data-stu-id="f597a-115">Document</span></span><br/>                             |
| <span data-ttu-id="f597a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f597a-116">Notes</span></span> <br/>          | <span data-ttu-id="f597a-117">Связано с элементом Документковерфронт</span><span class="sxs-lookup"><span data-stu-id="f597a-117">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f597a-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f597a-118">Structure Content</span></span>

<span data-ttu-id="f597a-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f597a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="f597a-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="f597a-120">Structure Properties</span></span>

<span data-ttu-id="f597a-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f597a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f597a-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="f597a-122">Property</span></span>                | <span data-ttu-id="f597a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f597a-123">xsi:type</span></span>           | <span data-ttu-id="f597a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f597a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f597a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f597a-125">DataType</span></span><br/>     | <span data-ttu-id="f597a-126">строка</span><span class="sxs-lookup"><span data-stu-id="f597a-126">string</span></span><br/>  | <span data-ttu-id="f597a-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f597a-127">xs:string</span></span><br/>       |
| <span data-ttu-id="f597a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f597a-128">DefaultValue</span></span><br/> | <span data-ttu-id="f597a-129">строка</span><span class="sxs-lookup"><span data-stu-id="f597a-129">string</span></span><br/>  | <span data-ttu-id="f597a-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="f597a-130">undefined</span></span><br/>       |
| <span data-ttu-id="f597a-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f597a-131">MaxLength</span></span><br/>    | <span data-ttu-id="f597a-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="f597a-132">integer</span></span><br/> | <span data-ttu-id="f597a-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="f597a-133">undefined</span></span><br/>       |
| <span data-ttu-id="f597a-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="f597a-134">MinLength</span></span><br/>    | <span data-ttu-id="f597a-135">целое число</span><span class="sxs-lookup"><span data-stu-id="f597a-135">integer</span></span><br/> | <span data-ttu-id="f597a-136">1</span><span class="sxs-lookup"><span data-stu-id="f597a-136">1</span></span><br/>               |
| <span data-ttu-id="f597a-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f597a-137">Mandatory</span></span><br/>    | <span data-ttu-id="f597a-138">строка</span><span class="sxs-lookup"><span data-stu-id="f597a-138">string</span></span><br/>  | <span data-ttu-id="f597a-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="f597a-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f597a-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="f597a-140">UnitType</span></span><br/>     | <span data-ttu-id="f597a-141">строка</span><span class="sxs-lookup"><span data-stu-id="f597a-141">string</span></span><br/>  | <span data-ttu-id="f597a-142">characters</span><span class="sxs-lookup"><span data-stu-id="f597a-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f597a-143">См. также</span><span class="sxs-lookup"><span data-stu-id="f597a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f597a-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f597a-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




