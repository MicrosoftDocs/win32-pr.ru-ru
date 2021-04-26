---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: жобкоммент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998351"
---
# <a name="jobcomment"></a><span data-ttu-id="8d1bd-104">жобкоммент</span><span class="sxs-lookup"><span data-stu-id="8d1bd-104">JobComment</span></span>

<span data-ttu-id="8d1bd-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8d1bd-105">This topic is not current.</span></span> <span data-ttu-id="8d1bd-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8d1bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8d1bd-107">Указывает комментарий, связанный с заданием.</span><span class="sxs-lookup"><span data-stu-id="8d1bd-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="8d1bd-108">Пример: "доставлять в комнату 1234 по завершении".</span><span class="sxs-lookup"><span data-stu-id="8d1bd-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="8d1bd-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8d1bd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8d1bd-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8d1bd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8d1bd-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8d1bd-111">Element Information</span></span>



| <span data-ttu-id="8d1bd-112">Имя</span><span class="sxs-lookup"><span data-stu-id="8d1bd-112">Name</span></span> | <span data-ttu-id="8d1bd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8d1bd-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="8d1bd-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8d1bd-114">Element Type</span></span> <br/>   | <span data-ttu-id="8d1bd-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="8d1bd-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="8d1bd-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8d1bd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8d1bd-117">Задание</span><span class="sxs-lookup"><span data-stu-id="8d1bd-117">Job</span></span><br/>          |
| <span data-ttu-id="8d1bd-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d1bd-118">Notes</span></span> <br/>          | <span data-ttu-id="8d1bd-119">Нет</span><span class="sxs-lookup"><span data-stu-id="8d1bd-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="8d1bd-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8d1bd-120">Structure Content</span></span>

<span data-ttu-id="8d1bd-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8d1bd-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8d1bd-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="8d1bd-122">Structure Properties</span></span>

<span data-ttu-id="8d1bd-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8d1bd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8d1bd-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d1bd-124">Property</span></span>                | <span data-ttu-id="8d1bd-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8d1bd-125">xsi:type</span></span>           | <span data-ttu-id="8d1bd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8d1bd-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8d1bd-127">DataType</span><span class="sxs-lookup"><span data-stu-id="8d1bd-127">DataType</span></span><br/>     | <span data-ttu-id="8d1bd-128">строка</span><span class="sxs-lookup"><span data-stu-id="8d1bd-128">string</span></span><br/>  | <span data-ttu-id="8d1bd-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d1bd-129">xs:string</span></span><br/>       |
| <span data-ttu-id="8d1bd-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8d1bd-130">DefaultValue</span></span><br/> | <span data-ttu-id="8d1bd-131">строка</span><span class="sxs-lookup"><span data-stu-id="8d1bd-131">string</span></span><br/>  | <span data-ttu-id="8d1bd-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8d1bd-132">undefined</span></span><br/>       |
| <span data-ttu-id="8d1bd-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="8d1bd-133">MaxLength</span></span><br/>    | <span data-ttu-id="8d1bd-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="8d1bd-134">integer</span></span><br/> | <span data-ttu-id="8d1bd-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8d1bd-135">undefined</span></span><br/>       |
| <span data-ttu-id="8d1bd-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="8d1bd-136">MinLength</span></span><br/>    | <span data-ttu-id="8d1bd-137">целое число</span><span class="sxs-lookup"><span data-stu-id="8d1bd-137">integer</span></span><br/> | <span data-ttu-id="8d1bd-138">1</span><span class="sxs-lookup"><span data-stu-id="8d1bd-138">1</span></span><br/>               |
| <span data-ttu-id="8d1bd-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d1bd-139">Mandatory</span></span><br/>    | <span data-ttu-id="8d1bd-140">строка</span><span class="sxs-lookup"><span data-stu-id="8d1bd-140">string</span></span><br/>  | <span data-ttu-id="8d1bd-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="8d1bd-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8d1bd-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="8d1bd-142">UnitType</span></span><br/>     | <span data-ttu-id="8d1bd-143">строка</span><span class="sxs-lookup"><span data-stu-id="8d1bd-143">string</span></span><br/>  | <span data-ttu-id="8d1bd-144">characters</span><span class="sxs-lookup"><span data-stu-id="8d1bd-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="8d1bd-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8d1bd-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d1bd-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8d1bd-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




