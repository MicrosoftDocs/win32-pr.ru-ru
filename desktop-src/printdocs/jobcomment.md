---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: жобкоммент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105647767"
---
# <a name="jobcomment"></a><span data-ttu-id="a71a2-104">жобкоммент</span><span class="sxs-lookup"><span data-stu-id="a71a2-104">JobComment</span></span>

<span data-ttu-id="a71a2-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="a71a2-105">This topic is not current.</span></span> <span data-ttu-id="a71a2-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a71a2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a71a2-107">Указывает комментарий, связанный с заданием.</span><span class="sxs-lookup"><span data-stu-id="a71a2-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="a71a2-108">Пример: "доставлять в комнату 1234 по завершении".</span><span class="sxs-lookup"><span data-stu-id="a71a2-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="a71a2-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a71a2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a71a2-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="a71a2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a71a2-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a71a2-111">Element Information</span></span>



| <span data-ttu-id="a71a2-112">Имя</span><span class="sxs-lookup"><span data-stu-id="a71a2-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="a71a2-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a71a2-113">Element Type</span></span> <br/>   | <span data-ttu-id="a71a2-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="a71a2-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="a71a2-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="a71a2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a71a2-116">Задание</span><span class="sxs-lookup"><span data-stu-id="a71a2-116">Job</span></span><br/>          |
| <span data-ttu-id="a71a2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a71a2-117">Notes</span></span> <br/>          | <span data-ttu-id="a71a2-118">Нет</span><span class="sxs-lookup"><span data-stu-id="a71a2-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="a71a2-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="a71a2-119">Structure Content</span></span>

<span data-ttu-id="a71a2-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a71a2-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a71a2-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="a71a2-121">Structure Properties</span></span>

<span data-ttu-id="a71a2-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="a71a2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a71a2-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="a71a2-123">Property</span></span>                | <span data-ttu-id="a71a2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a71a2-124">xsi:type</span></span>           | <span data-ttu-id="a71a2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a71a2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a71a2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a71a2-126">DataType</span></span><br/>     | <span data-ttu-id="a71a2-127">строка</span><span class="sxs-lookup"><span data-stu-id="a71a2-127">string</span></span><br/>  | <span data-ttu-id="a71a2-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a71a2-128">xs:string</span></span><br/>       |
| <span data-ttu-id="a71a2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a71a2-129">DefaultValue</span></span><br/> | <span data-ttu-id="a71a2-130">строка</span><span class="sxs-lookup"><span data-stu-id="a71a2-130">string</span></span><br/>  | <span data-ttu-id="a71a2-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a71a2-131">undefined</span></span><br/>       |
| <span data-ttu-id="a71a2-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a71a2-132">MaxLength</span></span><br/>    | <span data-ttu-id="a71a2-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="a71a2-133">integer</span></span><br/> | <span data-ttu-id="a71a2-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a71a2-134">undefined</span></span><br/>       |
| <span data-ttu-id="a71a2-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="a71a2-135">MinLength</span></span><br/>    | <span data-ttu-id="a71a2-136">целое число</span><span class="sxs-lookup"><span data-stu-id="a71a2-136">integer</span></span><br/> | <span data-ttu-id="a71a2-137">1</span><span class="sxs-lookup"><span data-stu-id="a71a2-137">1</span></span><br/>               |
| <span data-ttu-id="a71a2-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a71a2-138">Mandatory</span></span><br/>    | <span data-ttu-id="a71a2-139">строка</span><span class="sxs-lookup"><span data-stu-id="a71a2-139">string</span></span><br/>  | <span data-ttu-id="a71a2-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="a71a2-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a71a2-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="a71a2-141">UnitType</span></span><br/>     | <span data-ttu-id="a71a2-142">строка</span><span class="sxs-lookup"><span data-stu-id="a71a2-142">string</span></span><br/>  | <span data-ttu-id="a71a2-143">characters</span><span class="sxs-lookup"><span data-stu-id="a71a2-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a71a2-144">См. также</span><span class="sxs-lookup"><span data-stu-id="a71a2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a71a2-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a71a2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




