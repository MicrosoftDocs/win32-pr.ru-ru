---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: документковербакксаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6547ac2dc2c3f91ea4d0ebeea87622c790ae7d4d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996281"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="c43de-104">документковербакксаурце</span><span class="sxs-lookup"><span data-stu-id="c43de-104">DocumentCoverBackSource</span></span>

<span data-ttu-id="c43de-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c43de-105">This topic is not current.</span></span> <span data-ttu-id="c43de-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c43de-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c43de-107">Указывает источник для пользовательского листового обложки.</span><span class="sxs-lookup"><span data-stu-id="c43de-107">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="c43de-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c43de-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c43de-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c43de-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c43de-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c43de-110">Element Information</span></span>



| <span data-ttu-id="c43de-111">Имя</span><span class="sxs-lookup"><span data-stu-id="c43de-111">Name</span></span> | <span data-ttu-id="c43de-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c43de-112">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="c43de-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c43de-113">Element Type</span></span> <br/>   | <span data-ttu-id="c43de-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="c43de-114">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="c43de-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c43de-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c43de-116">Документ</span><span class="sxs-lookup"><span data-stu-id="c43de-116">Document</span></span><br/>                            |
| <span data-ttu-id="c43de-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c43de-117">Notes</span></span> <br/>          | <span data-ttu-id="c43de-118">Связано с элементом Документковербакк</span><span class="sxs-lookup"><span data-stu-id="c43de-118">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c43de-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c43de-119">Structure Content</span></span>

<span data-ttu-id="c43de-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c43de-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c43de-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="c43de-121">Structure Properties</span></span>

<span data-ttu-id="c43de-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c43de-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c43de-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="c43de-123">Property</span></span>                | <span data-ttu-id="c43de-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c43de-124">xsi:type</span></span>           | <span data-ttu-id="c43de-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c43de-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c43de-126">DataType</span><span class="sxs-lookup"><span data-stu-id="c43de-126">DataType</span></span><br/>     | <span data-ttu-id="c43de-127">строка</span><span class="sxs-lookup"><span data-stu-id="c43de-127">string</span></span><br/>  | <span data-ttu-id="c43de-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="c43de-128">xs:string</span></span><br/>       |
| <span data-ttu-id="c43de-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c43de-129">DefaultValue</span></span><br/> | <span data-ttu-id="c43de-130">строка</span><span class="sxs-lookup"><span data-stu-id="c43de-130">string</span></span><br/>  | <span data-ttu-id="c43de-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c43de-131">undefined</span></span><br/>       |
| <span data-ttu-id="c43de-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c43de-132">MaxLength</span></span><br/>    | <span data-ttu-id="c43de-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="c43de-133">integer</span></span><br/> | <span data-ttu-id="c43de-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c43de-134">undefined</span></span><br/>       |
| <span data-ttu-id="c43de-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="c43de-135">MinLength</span></span><br/>    | <span data-ttu-id="c43de-136">целое число</span><span class="sxs-lookup"><span data-stu-id="c43de-136">integer</span></span><br/> | <span data-ttu-id="c43de-137">1</span><span class="sxs-lookup"><span data-stu-id="c43de-137">1</span></span><br/>               |
| <span data-ttu-id="c43de-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c43de-138">Mandatory</span></span><br/>    | <span data-ttu-id="c43de-139">строка</span><span class="sxs-lookup"><span data-stu-id="c43de-139">string</span></span><br/>  | <span data-ttu-id="c43de-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="c43de-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c43de-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="c43de-141">UnitType</span></span><br/>     | <span data-ttu-id="c43de-142">строка</span><span class="sxs-lookup"><span data-stu-id="c43de-142">string</span></span><br/>  | <span data-ttu-id="c43de-143">characters</span><span class="sxs-lookup"><span data-stu-id="c43de-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c43de-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c43de-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c43de-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c43de-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




