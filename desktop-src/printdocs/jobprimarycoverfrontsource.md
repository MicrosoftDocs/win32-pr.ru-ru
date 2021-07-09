---
description: Получение сведений о параметре Жобпримариковерфронтсаурце. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: жобпримариковерфронтсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4698d826e59e513d5eb171381cd1b18ea4a751
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549402"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="733e9-105">жобпримариковерфронтсаурце</span><span class="sxs-lookup"><span data-stu-id="733e9-105">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="733e9-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="733e9-106">This topic is not current.</span></span> <span data-ttu-id="733e9-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="733e9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="733e9-108">Указывает источник пользовательского внешнего титульного листа для задания.</span><span class="sxs-lookup"><span data-stu-id="733e9-108">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="733e9-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="733e9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="733e9-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="733e9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="733e9-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="733e9-111">Element Information</span></span>



| <span data-ttu-id="733e9-112">Имя</span><span class="sxs-lookup"><span data-stu-id="733e9-112">Name</span></span> | <span data-ttu-id="733e9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="733e9-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="733e9-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="733e9-114">Element Type</span></span> <br/>   | <span data-ttu-id="733e9-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="733e9-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="733e9-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="733e9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="733e9-117">Задание</span><span class="sxs-lookup"><span data-stu-id="733e9-117">Job</span></span><br/>                             |
| <span data-ttu-id="733e9-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="733e9-118">Notes</span></span> <br/>          | <span data-ttu-id="733e9-119">Связано с элементом Жобковерфронт</span><span class="sxs-lookup"><span data-stu-id="733e9-119">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="733e9-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="733e9-120">Structure Content</span></span>

<span data-ttu-id="733e9-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="733e9-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="733e9-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="733e9-122">Structure Properties</span></span>

<span data-ttu-id="733e9-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="733e9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="733e9-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="733e9-124">Property</span></span>                | <span data-ttu-id="733e9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="733e9-125">xsi:type</span></span>           | <span data-ttu-id="733e9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="733e9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="733e9-127">DataType</span><span class="sxs-lookup"><span data-stu-id="733e9-127">DataType</span></span><br/>     | <span data-ttu-id="733e9-128">строка</span><span class="sxs-lookup"><span data-stu-id="733e9-128">string</span></span><br/>  | <span data-ttu-id="733e9-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="733e9-129">xs:string</span></span><br/>       |
| <span data-ttu-id="733e9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="733e9-130">DefaultValue</span></span><br/> | <span data-ttu-id="733e9-131">строка</span><span class="sxs-lookup"><span data-stu-id="733e9-131">string</span></span><br/>  | <span data-ttu-id="733e9-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="733e9-132">undefined</span></span><br/>       |
| <span data-ttu-id="733e9-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="733e9-133">MaxLength</span></span><br/>    | <span data-ttu-id="733e9-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="733e9-134">integer</span></span><br/> | <span data-ttu-id="733e9-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="733e9-135">undefined</span></span><br/>       |
| <span data-ttu-id="733e9-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="733e9-136">MinLength</span></span><br/>    | <span data-ttu-id="733e9-137">целое число</span><span class="sxs-lookup"><span data-stu-id="733e9-137">integer</span></span><br/> | <span data-ttu-id="733e9-138">1</span><span class="sxs-lookup"><span data-stu-id="733e9-138">1</span></span><br/>               |
| <span data-ttu-id="733e9-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="733e9-139">Mandatory</span></span><br/>    | <span data-ttu-id="733e9-140">строка</span><span class="sxs-lookup"><span data-stu-id="733e9-140">string</span></span><br/>  | <span data-ttu-id="733e9-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="733e9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="733e9-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="733e9-142">UnitType</span></span><br/>     | <span data-ttu-id="733e9-143">строка</span><span class="sxs-lookup"><span data-stu-id="733e9-143">string</span></span><br/>  | <span data-ttu-id="733e9-144">characters</span><span class="sxs-lookup"><span data-stu-id="733e9-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="733e9-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="733e9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="733e9-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="733e9-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




