---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: жобпримариковерфронтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3dfc50d060093c1c2ee1baf494305ae6afd6ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664847"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="c837e-104">жобпримариковерфронтсаурце</span><span class="sxs-lookup"><span data-stu-id="c837e-104">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="c837e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c837e-105">This topic is not current.</span></span> <span data-ttu-id="c837e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c837e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c837e-107">Указывает источник пользовательского внешнего титульного листа для задания.</span><span class="sxs-lookup"><span data-stu-id="c837e-107">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="c837e-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c837e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c837e-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c837e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c837e-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c837e-110">Element Information</span></span>



| <span data-ttu-id="c837e-111">Имя</span><span class="sxs-lookup"><span data-stu-id="c837e-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="c837e-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c837e-112">Element Type</span></span> <br/>   | <span data-ttu-id="c837e-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="c837e-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="c837e-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c837e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c837e-115">Задание</span><span class="sxs-lookup"><span data-stu-id="c837e-115">Job</span></span><br/>                             |
| <span data-ttu-id="c837e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c837e-116">Notes</span></span> <br/>          | <span data-ttu-id="c837e-117">Связано с элементом Жобковерфронт</span><span class="sxs-lookup"><span data-stu-id="c837e-117">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c837e-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c837e-118">Structure Content</span></span>

<span data-ttu-id="c837e-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c837e-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="c837e-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="c837e-120">Structure Properties</span></span>

<span data-ttu-id="c837e-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c837e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c837e-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="c837e-122">Property</span></span>                | <span data-ttu-id="c837e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c837e-123">xsi:type</span></span>           | <span data-ttu-id="c837e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c837e-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c837e-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c837e-125">DataType</span></span><br/>     | <span data-ttu-id="c837e-126">строка</span><span class="sxs-lookup"><span data-stu-id="c837e-126">string</span></span><br/>  | <span data-ttu-id="c837e-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="c837e-127">xs:string</span></span><br/>       |
| <span data-ttu-id="c837e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c837e-128">DefaultValue</span></span><br/> | <span data-ttu-id="c837e-129">строка</span><span class="sxs-lookup"><span data-stu-id="c837e-129">string</span></span><br/>  | <span data-ttu-id="c837e-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c837e-130">undefined</span></span><br/>       |
| <span data-ttu-id="c837e-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c837e-131">MaxLength</span></span><br/>    | <span data-ttu-id="c837e-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="c837e-132">integer</span></span><br/> | <span data-ttu-id="c837e-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c837e-133">undefined</span></span><br/>       |
| <span data-ttu-id="c837e-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="c837e-134">MinLength</span></span><br/>    | <span data-ttu-id="c837e-135">целое число</span><span class="sxs-lookup"><span data-stu-id="c837e-135">integer</span></span><br/> | <span data-ttu-id="c837e-136">1</span><span class="sxs-lookup"><span data-stu-id="c837e-136">1</span></span><br/>               |
| <span data-ttu-id="c837e-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c837e-137">Mandatory</span></span><br/>    | <span data-ttu-id="c837e-138">строка</span><span class="sxs-lookup"><span data-stu-id="c837e-138">string</span></span><br/>  | <span data-ttu-id="c837e-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="c837e-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c837e-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="c837e-140">UnitType</span></span><br/>     | <span data-ttu-id="c837e-141">строка</span><span class="sxs-lookup"><span data-stu-id="c837e-141">string</span></span><br/>  | <span data-ttu-id="c837e-142">characters</span><span class="sxs-lookup"><span data-stu-id="c837e-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c837e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="c837e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c837e-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c837e-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




