---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: жобпримариковербакксаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2145bae0843323928d8a7d016fc61f10c0e388ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993981"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="eeb6f-104">жобпримариковербакксаурце</span><span class="sxs-lookup"><span data-stu-id="eeb6f-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="eeb6f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="eeb6f-105">This topic is not current.</span></span> <span data-ttu-id="eeb6f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eeb6f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eeb6f-107">Указывает источник пользовательского первичного листа для задания.</span><span class="sxs-lookup"><span data-stu-id="eeb6f-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="eeb6f-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eeb6f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eeb6f-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="eeb6f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="eeb6f-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eeb6f-110">Element Information</span></span>



| <span data-ttu-id="eeb6f-111">Имя</span><span class="sxs-lookup"><span data-stu-id="eeb6f-111">Name</span></span> | <span data-ttu-id="eeb6f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="eeb6f-112">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="eeb6f-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="eeb6f-113">Element Type</span></span> <br/>   | <span data-ttu-id="eeb6f-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="eeb6f-114">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="eeb6f-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="eeb6f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eeb6f-116">Задание</span><span class="sxs-lookup"><span data-stu-id="eeb6f-116">Job</span></span><br/>                            |
| <span data-ttu-id="eeb6f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="eeb6f-117">Notes</span></span> <br/>          | <span data-ttu-id="eeb6f-118">Связано с элементом Жобковербакк</span><span class="sxs-lookup"><span data-stu-id="eeb6f-118">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="eeb6f-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="eeb6f-119">Structure Content</span></span>

<span data-ttu-id="eeb6f-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="eeb6f-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="eeb6f-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="eeb6f-121">Structure Properties</span></span>

<span data-ttu-id="eeb6f-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="eeb6f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eeb6f-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="eeb6f-123">Property</span></span>                | <span data-ttu-id="eeb6f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="eeb6f-124">xsi:type</span></span>           | <span data-ttu-id="eeb6f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="eeb6f-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="eeb6f-126">DataType</span><span class="sxs-lookup"><span data-stu-id="eeb6f-126">DataType</span></span><br/>     | <span data-ttu-id="eeb6f-127">строка</span><span class="sxs-lookup"><span data-stu-id="eeb6f-127">string</span></span><br/>  | <span data-ttu-id="eeb6f-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="eeb6f-128">xs:string</span></span><br/>       |
| <span data-ttu-id="eeb6f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="eeb6f-129">DefaultValue</span></span><br/> | <span data-ttu-id="eeb6f-130">строка</span><span class="sxs-lookup"><span data-stu-id="eeb6f-130">string</span></span><br/>  | <span data-ttu-id="eeb6f-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="eeb6f-131">undefined</span></span><br/>       |
| <span data-ttu-id="eeb6f-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="eeb6f-132">MaxLength</span></span><br/>    | <span data-ttu-id="eeb6f-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="eeb6f-133">integer</span></span><br/> | <span data-ttu-id="eeb6f-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="eeb6f-134">undefined</span></span><br/>       |
| <span data-ttu-id="eeb6f-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="eeb6f-135">MinLength</span></span><br/>    | <span data-ttu-id="eeb6f-136">целое число</span><span class="sxs-lookup"><span data-stu-id="eeb6f-136">integer</span></span><br/> | <span data-ttu-id="eeb6f-137">1</span><span class="sxs-lookup"><span data-stu-id="eeb6f-137">1</span></span><br/>               |
| <span data-ttu-id="eeb6f-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eeb6f-138">Mandatory</span></span><br/>    | <span data-ttu-id="eeb6f-139">строка</span><span class="sxs-lookup"><span data-stu-id="eeb6f-139">string</span></span><br/>  | <span data-ttu-id="eeb6f-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="eeb6f-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="eeb6f-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="eeb6f-141">UnitType</span></span><br/>     | <span data-ttu-id="eeb6f-142">строка</span><span class="sxs-lookup"><span data-stu-id="eeb6f-142">string</span></span><br/>  | <span data-ttu-id="eeb6f-143">characters</span><span class="sxs-lookup"><span data-stu-id="eeb6f-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="eeb6f-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="eeb6f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb6f-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="eeb6f-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




