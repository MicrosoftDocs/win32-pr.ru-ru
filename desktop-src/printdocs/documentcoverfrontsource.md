---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: документковерфронтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b558a044716c5c13ae012665193f958f8ce6aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997901"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="3c029-104">документковерфронтсаурце</span><span class="sxs-lookup"><span data-stu-id="3c029-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="3c029-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="3c029-105">This topic is not current.</span></span> <span data-ttu-id="3c029-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3c029-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3c029-107">Указывает источник пользовательского внешнего титульного листа.</span><span class="sxs-lookup"><span data-stu-id="3c029-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="3c029-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3c029-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3c029-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="3c029-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3c029-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3c029-110">Element Information</span></span>



| <span data-ttu-id="3c029-111">Имя</span><span class="sxs-lookup"><span data-stu-id="3c029-111">Name</span></span> | <span data-ttu-id="3c029-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3c029-112">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="3c029-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="3c029-113">Element Type</span></span> <br/>   | <span data-ttu-id="3c029-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="3c029-114">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="3c029-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="3c029-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3c029-116">Документ</span><span class="sxs-lookup"><span data-stu-id="3c029-116">Document</span></span><br/>                             |
| <span data-ttu-id="3c029-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c029-117">Notes</span></span> <br/>          | <span data-ttu-id="3c029-118">Связано с элементом Документковерфронт</span><span class="sxs-lookup"><span data-stu-id="3c029-118">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3c029-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="3c029-119">Structure Content</span></span>

<span data-ttu-id="3c029-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="3c029-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3c029-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="3c029-121">Structure Properties</span></span>

<span data-ttu-id="3c029-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="3c029-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3c029-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="3c029-123">Property</span></span>                | <span data-ttu-id="3c029-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3c029-124">xsi:type</span></span>           | <span data-ttu-id="3c029-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3c029-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3c029-126">DataType</span><span class="sxs-lookup"><span data-stu-id="3c029-126">DataType</span></span><br/>     | <span data-ttu-id="3c029-127">строка</span><span class="sxs-lookup"><span data-stu-id="3c029-127">string</span></span><br/>  | <span data-ttu-id="3c029-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c029-128">xs:string</span></span><br/>       |
| <span data-ttu-id="3c029-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3c029-129">DefaultValue</span></span><br/> | <span data-ttu-id="3c029-130">строка</span><span class="sxs-lookup"><span data-stu-id="3c029-130">string</span></span><br/>  | <span data-ttu-id="3c029-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="3c029-131">undefined</span></span><br/>       |
| <span data-ttu-id="3c029-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3c029-132">MaxLength</span></span><br/>    | <span data-ttu-id="3c029-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="3c029-133">integer</span></span><br/> | <span data-ttu-id="3c029-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="3c029-134">undefined</span></span><br/>       |
| <span data-ttu-id="3c029-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="3c029-135">MinLength</span></span><br/>    | <span data-ttu-id="3c029-136">целое число</span><span class="sxs-lookup"><span data-stu-id="3c029-136">integer</span></span><br/> | <span data-ttu-id="3c029-137">1</span><span class="sxs-lookup"><span data-stu-id="3c029-137">1</span></span><br/>               |
| <span data-ttu-id="3c029-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c029-138">Mandatory</span></span><br/>    | <span data-ttu-id="3c029-139">строка</span><span class="sxs-lookup"><span data-stu-id="3c029-139">string</span></span><br/>  | <span data-ttu-id="3c029-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="3c029-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3c029-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="3c029-141">UnitType</span></span><br/>     | <span data-ttu-id="3c029-142">строка</span><span class="sxs-lookup"><span data-stu-id="3c029-142">string</span></span><br/>  | <span data-ttu-id="3c029-143">characters</span><span class="sxs-lookup"><span data-stu-id="3c029-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3c029-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3c029-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c029-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="3c029-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




