---
description: Сведения об элементе Жобкоммент, который указывает комментарий, связанный с заданием, например, доставляется в комнату 1234 после завершения.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: жобкоммент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409047"
---
# <a name="jobcomment"></a><span data-ttu-id="89203-103">жобкоммент</span><span class="sxs-lookup"><span data-stu-id="89203-103">JobComment</span></span>

<span data-ttu-id="89203-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="89203-104">This topic is not current.</span></span> <span data-ttu-id="89203-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="89203-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="89203-106">Указывает комментарий, связанный с заданием.</span><span class="sxs-lookup"><span data-stu-id="89203-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="89203-107">Пример: "доставлять в комнату 1234 по завершении".</span><span class="sxs-lookup"><span data-stu-id="89203-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="89203-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="89203-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="89203-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="89203-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="89203-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="89203-110">Element Information</span></span>



| <span data-ttu-id="89203-111">Имя</span><span class="sxs-lookup"><span data-stu-id="89203-111">Name</span></span> | <span data-ttu-id="89203-112">Значение</span><span class="sxs-lookup"><span data-stu-id="89203-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="89203-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="89203-113">Element Type</span></span> <br/>   | <span data-ttu-id="89203-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="89203-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="89203-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="89203-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="89203-116">Задание</span><span class="sxs-lookup"><span data-stu-id="89203-116">Job</span></span><br/>          |
| <span data-ttu-id="89203-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="89203-117">Notes</span></span> <br/>          | <span data-ttu-id="89203-118">Нет</span><span class="sxs-lookup"><span data-stu-id="89203-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="89203-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="89203-119">Structure Content</span></span>

<span data-ttu-id="89203-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="89203-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="89203-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="89203-121">Structure Properties</span></span>

<span data-ttu-id="89203-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="89203-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="89203-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="89203-123">Property</span></span>                | <span data-ttu-id="89203-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="89203-124">xsi:type</span></span>           | <span data-ttu-id="89203-125">Значение</span><span class="sxs-lookup"><span data-stu-id="89203-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="89203-126">DataType</span><span class="sxs-lookup"><span data-stu-id="89203-126">DataType</span></span><br/>     | <span data-ttu-id="89203-127">строка</span><span class="sxs-lookup"><span data-stu-id="89203-127">string</span></span><br/>  | <span data-ttu-id="89203-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="89203-128">xs:string</span></span><br/>       |
| <span data-ttu-id="89203-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="89203-129">DefaultValue</span></span><br/> | <span data-ttu-id="89203-130">строка</span><span class="sxs-lookup"><span data-stu-id="89203-130">string</span></span><br/>  | <span data-ttu-id="89203-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="89203-131">undefined</span></span><br/>       |
| <span data-ttu-id="89203-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="89203-132">MaxLength</span></span><br/>    | <span data-ttu-id="89203-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="89203-133">integer</span></span><br/> | <span data-ttu-id="89203-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="89203-134">undefined</span></span><br/>       |
| <span data-ttu-id="89203-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="89203-135">MinLength</span></span><br/>    | <span data-ttu-id="89203-136">целое число</span><span class="sxs-lookup"><span data-stu-id="89203-136">integer</span></span><br/> | <span data-ttu-id="89203-137">1</span><span class="sxs-lookup"><span data-stu-id="89203-137">1</span></span><br/>               |
| <span data-ttu-id="89203-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="89203-138">Mandatory</span></span><br/>    | <span data-ttu-id="89203-139">строка</span><span class="sxs-lookup"><span data-stu-id="89203-139">string</span></span><br/>  | <span data-ttu-id="89203-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="89203-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="89203-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="89203-141">UnitType</span></span><br/>     | <span data-ttu-id="89203-142">строка</span><span class="sxs-lookup"><span data-stu-id="89203-142">string</span></span><br/>  | <span data-ttu-id="89203-143">characters</span><span class="sxs-lookup"><span data-stu-id="89203-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="89203-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="89203-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89203-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="89203-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




