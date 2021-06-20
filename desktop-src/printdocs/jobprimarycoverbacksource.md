---
description: Сведения об элементе Жобпримариковербакксаурце, который указывает источник для пользовательского первичного основного листа для задания.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: жобпримариковербакксаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408697"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="afc47-103">жобпримариковербакксаурце</span><span class="sxs-lookup"><span data-stu-id="afc47-103">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="afc47-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="afc47-104">This topic is not current.</span></span> <span data-ttu-id="afc47-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="afc47-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="afc47-106">Указывает источник пользовательского первичного листа для задания.</span><span class="sxs-lookup"><span data-stu-id="afc47-106">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="afc47-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="afc47-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="afc47-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="afc47-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="afc47-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="afc47-109">Element Information</span></span>



| <span data-ttu-id="afc47-110">Имя</span><span class="sxs-lookup"><span data-stu-id="afc47-110">Name</span></span> | <span data-ttu-id="afc47-111">Значение</span><span class="sxs-lookup"><span data-stu-id="afc47-111">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="afc47-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="afc47-112">Element Type</span></span> <br/>   | <span data-ttu-id="afc47-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="afc47-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="afc47-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="afc47-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="afc47-115">Задание</span><span class="sxs-lookup"><span data-stu-id="afc47-115">Job</span></span><br/>                            |
| <span data-ttu-id="afc47-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="afc47-116">Notes</span></span> <br/>          | <span data-ttu-id="afc47-117">Связано с элементом Жобковербакк</span><span class="sxs-lookup"><span data-stu-id="afc47-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="afc47-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="afc47-118">Structure Content</span></span>

<span data-ttu-id="afc47-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="afc47-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="afc47-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="afc47-120">Structure Properties</span></span>

<span data-ttu-id="afc47-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="afc47-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="afc47-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="afc47-122">Property</span></span>                | <span data-ttu-id="afc47-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="afc47-123">xsi:type</span></span>           | <span data-ttu-id="afc47-124">Значение</span><span class="sxs-lookup"><span data-stu-id="afc47-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="afc47-125">DataType</span><span class="sxs-lookup"><span data-stu-id="afc47-125">DataType</span></span><br/>     | <span data-ttu-id="afc47-126">строка</span><span class="sxs-lookup"><span data-stu-id="afc47-126">string</span></span><br/>  | <span data-ttu-id="afc47-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="afc47-127">xs:string</span></span><br/>       |
| <span data-ttu-id="afc47-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="afc47-128">DefaultValue</span></span><br/> | <span data-ttu-id="afc47-129">строка</span><span class="sxs-lookup"><span data-stu-id="afc47-129">string</span></span><br/>  | <span data-ttu-id="afc47-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="afc47-130">undefined</span></span><br/>       |
| <span data-ttu-id="afc47-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="afc47-131">MaxLength</span></span><br/>    | <span data-ttu-id="afc47-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="afc47-132">integer</span></span><br/> | <span data-ttu-id="afc47-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="afc47-133">undefined</span></span><br/>       |
| <span data-ttu-id="afc47-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="afc47-134">MinLength</span></span><br/>    | <span data-ttu-id="afc47-135">целое число</span><span class="sxs-lookup"><span data-stu-id="afc47-135">integer</span></span><br/> | <span data-ttu-id="afc47-136">1</span><span class="sxs-lookup"><span data-stu-id="afc47-136">1</span></span><br/>               |
| <span data-ttu-id="afc47-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="afc47-137">Mandatory</span></span><br/>    | <span data-ttu-id="afc47-138">строка</span><span class="sxs-lookup"><span data-stu-id="afc47-138">string</span></span><br/>  | <span data-ttu-id="afc47-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="afc47-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="afc47-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="afc47-140">UnitType</span></span><br/>     | <span data-ttu-id="afc47-141">строка</span><span class="sxs-lookup"><span data-stu-id="afc47-141">string</span></span><br/>  | <span data-ttu-id="afc47-142">characters</span><span class="sxs-lookup"><span data-stu-id="afc47-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="afc47-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="afc47-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afc47-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="afc47-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




