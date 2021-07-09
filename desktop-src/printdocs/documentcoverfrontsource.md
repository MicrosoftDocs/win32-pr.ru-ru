---
description: Получение сведений о параметре Документковерфронтсаурце. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: документковерфронтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb6ecb089eb271e0b8fff136e73a20194f0c8f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548762"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="740a4-105">документковерфронтсаурце</span><span class="sxs-lookup"><span data-stu-id="740a4-105">DocumentCoverFrontSource</span></span>

<span data-ttu-id="740a4-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="740a4-106">This topic is not current.</span></span> <span data-ttu-id="740a4-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="740a4-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="740a4-108">Указывает источник пользовательского внешнего титульного листа.</span><span class="sxs-lookup"><span data-stu-id="740a4-108">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="740a4-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="740a4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="740a4-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="740a4-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="740a4-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="740a4-111">Element Information</span></span>



| <span data-ttu-id="740a4-112">Имя</span><span class="sxs-lookup"><span data-stu-id="740a4-112">Name</span></span> | <span data-ttu-id="740a4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="740a4-113">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="740a4-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="740a4-114">Element Type</span></span> <br/>   | <span data-ttu-id="740a4-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="740a4-115">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="740a4-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="740a4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="740a4-117">Документ</span><span class="sxs-lookup"><span data-stu-id="740a4-117">Document</span></span><br/>                             |
| <span data-ttu-id="740a4-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="740a4-118">Notes</span></span> <br/>          | <span data-ttu-id="740a4-119">Связано с элементом Документковерфронт</span><span class="sxs-lookup"><span data-stu-id="740a4-119">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="740a4-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="740a4-120">Structure Content</span></span>

<span data-ttu-id="740a4-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="740a4-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="740a4-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="740a4-122">Structure Properties</span></span>

<span data-ttu-id="740a4-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="740a4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="740a4-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="740a4-124">Property</span></span>                | <span data-ttu-id="740a4-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="740a4-125">xsi:type</span></span>           | <span data-ttu-id="740a4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="740a4-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="740a4-127">DataType</span><span class="sxs-lookup"><span data-stu-id="740a4-127">DataType</span></span><br/>     | <span data-ttu-id="740a4-128">строка</span><span class="sxs-lookup"><span data-stu-id="740a4-128">string</span></span><br/>  | <span data-ttu-id="740a4-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="740a4-129">xs:string</span></span><br/>       |
| <span data-ttu-id="740a4-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="740a4-130">DefaultValue</span></span><br/> | <span data-ttu-id="740a4-131">строка</span><span class="sxs-lookup"><span data-stu-id="740a4-131">string</span></span><br/>  | <span data-ttu-id="740a4-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="740a4-132">undefined</span></span><br/>       |
| <span data-ttu-id="740a4-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="740a4-133">MaxLength</span></span><br/>    | <span data-ttu-id="740a4-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="740a4-134">integer</span></span><br/> | <span data-ttu-id="740a4-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="740a4-135">undefined</span></span><br/>       |
| <span data-ttu-id="740a4-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="740a4-136">MinLength</span></span><br/>    | <span data-ttu-id="740a4-137">целое число</span><span class="sxs-lookup"><span data-stu-id="740a4-137">integer</span></span><br/> | <span data-ttu-id="740a4-138">1</span><span class="sxs-lookup"><span data-stu-id="740a4-138">1</span></span><br/>               |
| <span data-ttu-id="740a4-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="740a4-139">Mandatory</span></span><br/>    | <span data-ttu-id="740a4-140">строка</span><span class="sxs-lookup"><span data-stu-id="740a4-140">string</span></span><br/>  | <span data-ttu-id="740a4-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="740a4-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="740a4-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="740a4-142">UnitType</span></span><br/>     | <span data-ttu-id="740a4-143">строка</span><span class="sxs-lookup"><span data-stu-id="740a4-143">string</span></span><br/>  | <span data-ttu-id="740a4-144">characters</span><span class="sxs-lookup"><span data-stu-id="740a4-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="740a4-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="740a4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="740a4-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="740a4-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




