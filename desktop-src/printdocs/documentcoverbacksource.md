---
description: Сведения об элементе Документковербакксаурце, который указывает источник для пользовательского листового обложки.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: документковербакксаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be16ab26a4aa3dd7109fee7d630ed354b9b686d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409357"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="985d3-103">документковербакксаурце</span><span class="sxs-lookup"><span data-stu-id="985d3-103">DocumentCoverBackSource</span></span>

<span data-ttu-id="985d3-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="985d3-104">This topic is not current.</span></span> <span data-ttu-id="985d3-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="985d3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="985d3-106">Указывает источник для пользовательского листового обложки.</span><span class="sxs-lookup"><span data-stu-id="985d3-106">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="985d3-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="985d3-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="985d3-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="985d3-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="985d3-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="985d3-109">Element Information</span></span>



| <span data-ttu-id="985d3-110">Имя</span><span class="sxs-lookup"><span data-stu-id="985d3-110">Name</span></span> | <span data-ttu-id="985d3-111">Значение</span><span class="sxs-lookup"><span data-stu-id="985d3-111">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="985d3-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="985d3-112">Element Type</span></span> <br/>   | <span data-ttu-id="985d3-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="985d3-113">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="985d3-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="985d3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="985d3-115">Документ</span><span class="sxs-lookup"><span data-stu-id="985d3-115">Document</span></span><br/>                            |
| <span data-ttu-id="985d3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="985d3-116">Notes</span></span> <br/>          | <span data-ttu-id="985d3-117">Связано с элементом Документковербакк</span><span class="sxs-lookup"><span data-stu-id="985d3-117">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="985d3-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="985d3-118">Structure Content</span></span>

<span data-ttu-id="985d3-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="985d3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="985d3-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="985d3-120">Structure Properties</span></span>

<span data-ttu-id="985d3-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="985d3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="985d3-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="985d3-122">Property</span></span>                | <span data-ttu-id="985d3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="985d3-123">xsi:type</span></span>           | <span data-ttu-id="985d3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="985d3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="985d3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="985d3-125">DataType</span></span><br/>     | <span data-ttu-id="985d3-126">строка</span><span class="sxs-lookup"><span data-stu-id="985d3-126">string</span></span><br/>  | <span data-ttu-id="985d3-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="985d3-127">xs:string</span></span><br/>       |
| <span data-ttu-id="985d3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="985d3-128">DefaultValue</span></span><br/> | <span data-ttu-id="985d3-129">строка</span><span class="sxs-lookup"><span data-stu-id="985d3-129">string</span></span><br/>  | <span data-ttu-id="985d3-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="985d3-130">undefined</span></span><br/>       |
| <span data-ttu-id="985d3-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="985d3-131">MaxLength</span></span><br/>    | <span data-ttu-id="985d3-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="985d3-132">integer</span></span><br/> | <span data-ttu-id="985d3-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="985d3-133">undefined</span></span><br/>       |
| <span data-ttu-id="985d3-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="985d3-134">MinLength</span></span><br/>    | <span data-ttu-id="985d3-135">целое число</span><span class="sxs-lookup"><span data-stu-id="985d3-135">integer</span></span><br/> | <span data-ttu-id="985d3-136">1</span><span class="sxs-lookup"><span data-stu-id="985d3-136">1</span></span><br/>               |
| <span data-ttu-id="985d3-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="985d3-137">Mandatory</span></span><br/>    | <span data-ttu-id="985d3-138">строка</span><span class="sxs-lookup"><span data-stu-id="985d3-138">string</span></span><br/>  | <span data-ttu-id="985d3-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="985d3-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="985d3-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="985d3-140">UnitType</span></span><br/>     | <span data-ttu-id="985d3-141">строка</span><span class="sxs-lookup"><span data-stu-id="985d3-141">string</span></span><br/>  | <span data-ttu-id="985d3-142">characters</span><span class="sxs-lookup"><span data-stu-id="985d3-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="985d3-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="985d3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="985d3-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="985d3-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




