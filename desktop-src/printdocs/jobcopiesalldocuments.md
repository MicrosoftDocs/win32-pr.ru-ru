---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: жобкопиесаллдокументс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f8be33f98b540cab56b88df49cfb1e3c067988
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820420"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="9dec2-104">жобкопиесаллдокументс</span><span class="sxs-lookup"><span data-stu-id="9dec2-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="9dec2-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="9dec2-105">This topic is not current.</span></span> <span data-ttu-id="9dec2-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9dec2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9dec2-107">Указывает количество копий задания.</span><span class="sxs-lookup"><span data-stu-id="9dec2-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="9dec2-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9dec2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9dec2-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="9dec2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9dec2-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9dec2-110">Element Information</span></span>



| <span data-ttu-id="9dec2-111">Имя</span><span class="sxs-lookup"><span data-stu-id="9dec2-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="9dec2-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="9dec2-112">Element Type</span></span> <br/>   | <span data-ttu-id="9dec2-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="9dec2-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="9dec2-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="9dec2-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9dec2-115">Задание</span><span class="sxs-lookup"><span data-stu-id="9dec2-115">Job</span></span><br/>          |
| <span data-ttu-id="9dec2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9dec2-116">Notes</span></span> <br/>          | <span data-ttu-id="9dec2-117">Нет</span><span class="sxs-lookup"><span data-stu-id="9dec2-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="9dec2-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="9dec2-118">Structure Content</span></span>

<span data-ttu-id="9dec2-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="9dec2-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="9dec2-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="9dec2-120">Structure Properties</span></span>

<span data-ttu-id="9dec2-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="9dec2-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9dec2-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="9dec2-122">Property</span></span>                | <span data-ttu-id="9dec2-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9dec2-123">xsi:type</span></span>           | <span data-ttu-id="9dec2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9dec2-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="9dec2-125">DataType</span><span class="sxs-lookup"><span data-stu-id="9dec2-125">DataType</span></span><br/>     | <span data-ttu-id="9dec2-126">строка</span><span class="sxs-lookup"><span data-stu-id="9dec2-126">string</span></span><br/>  | <span data-ttu-id="9dec2-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9dec2-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="9dec2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9dec2-128">DefaultValue</span></span><br/> | <span data-ttu-id="9dec2-129">целое число</span><span class="sxs-lookup"><span data-stu-id="9dec2-129">integer</span></span><br/> | <span data-ttu-id="9dec2-130">1</span><span class="sxs-lookup"><span data-stu-id="9dec2-130">1</span></span><br/>                 |
| <span data-ttu-id="9dec2-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9dec2-131">MaxValue</span></span><br/>     | <span data-ttu-id="9dec2-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="9dec2-132">integer</span></span><br/> | <span data-ttu-id="9dec2-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="9dec2-133">undefined</span></span><br/>         |
| <span data-ttu-id="9dec2-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="9dec2-134">MinValue</span></span><br/>     | <span data-ttu-id="9dec2-135">целое число</span><span class="sxs-lookup"><span data-stu-id="9dec2-135">integer</span></span><br/> | <span data-ttu-id="9dec2-136">1</span><span class="sxs-lookup"><span data-stu-id="9dec2-136">1</span></span><br/>                 |
| <span data-ttu-id="9dec2-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9dec2-137">Mandatory</span></span><br/>    | <span data-ttu-id="9dec2-138">строка</span><span class="sxs-lookup"><span data-stu-id="9dec2-138">string</span></span><br/>  | <span data-ttu-id="9dec2-139">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="9dec2-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="9dec2-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="9dec2-140">Multiple</span></span><br/>     | <span data-ttu-id="9dec2-141">целое число</span><span class="sxs-lookup"><span data-stu-id="9dec2-141">integer</span></span><br/> | <span data-ttu-id="9dec2-142">1</span><span class="sxs-lookup"><span data-stu-id="9dec2-142">1</span></span><br/>                 |
| <span data-ttu-id="9dec2-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="9dec2-143">UnitType</span></span><br/>     | <span data-ttu-id="9dec2-144">строка</span><span class="sxs-lookup"><span data-stu-id="9dec2-144">string</span></span><br/>  | <span data-ttu-id="9dec2-145">Копи</span><span class="sxs-lookup"><span data-stu-id="9dec2-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="9dec2-146">См. также</span><span class="sxs-lookup"><span data-stu-id="9dec2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dec2-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="9dec2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




