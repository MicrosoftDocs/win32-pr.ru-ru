---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: жоберроршитсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c87a31e645b9ea5eedb22b48000991a99bc7e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998161"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="4c662-104">жоберроршитсаурце</span><span class="sxs-lookup"><span data-stu-id="4c662-104">JobErrorSheetSource</span></span>

<span data-ttu-id="4c662-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="4c662-105">This topic is not current.</span></span> <span data-ttu-id="4c662-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4c662-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4c662-107">Указывает источник настраиваемого листа ошибок.</span><span class="sxs-lookup"><span data-stu-id="4c662-107">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="4c662-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4c662-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4c662-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="4c662-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4c662-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4c662-110">Element Information</span></span>



| <span data-ttu-id="4c662-111">Имя</span><span class="sxs-lookup"><span data-stu-id="4c662-111">Name</span></span> | <span data-ttu-id="4c662-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4c662-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="4c662-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="4c662-113">Element Type</span></span> <br/>   | <span data-ttu-id="4c662-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="4c662-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="4c662-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="4c662-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4c662-116">Документ</span><span class="sxs-lookup"><span data-stu-id="4c662-116">Document</span></span><br/>                        |
| <span data-ttu-id="4c662-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c662-117">Notes</span></span> <br/>          | <span data-ttu-id="4c662-118">Связано с элементом Жоберроршит</span><span class="sxs-lookup"><span data-stu-id="4c662-118">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4c662-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="4c662-119">Structure Content</span></span>

<span data-ttu-id="4c662-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="4c662-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobErrorSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="4c662-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="4c662-121">Structure Properties</span></span>

<span data-ttu-id="4c662-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="4c662-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4c662-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="4c662-123">Property</span></span>                | <span data-ttu-id="4c662-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4c662-124">xsi:type</span></span>           | <span data-ttu-id="4c662-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4c662-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4c662-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4c662-126">DataType</span></span><br/>     | <span data-ttu-id="4c662-127">строка</span><span class="sxs-lookup"><span data-stu-id="4c662-127">string</span></span><br/>  | <span data-ttu-id="4c662-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c662-128">xs:string</span></span><br/>       |
| <span data-ttu-id="4c662-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4c662-129">DefaultValue</span></span><br/> | <span data-ttu-id="4c662-130">строка</span><span class="sxs-lookup"><span data-stu-id="4c662-130">string</span></span><br/>  | <span data-ttu-id="4c662-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4c662-131">undefined</span></span><br/>       |
| <span data-ttu-id="4c662-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4c662-132">MaxLength</span></span><br/>    | <span data-ttu-id="4c662-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="4c662-133">integer</span></span><br/> | <span data-ttu-id="4c662-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4c662-134">undefined</span></span><br/>       |
| <span data-ttu-id="4c662-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="4c662-135">MinLength</span></span><br/>    | <span data-ttu-id="4c662-136">целое число</span><span class="sxs-lookup"><span data-stu-id="4c662-136">integer</span></span><br/> | <span data-ttu-id="4c662-137">1</span><span class="sxs-lookup"><span data-stu-id="4c662-137">1</span></span><br/>               |
| <span data-ttu-id="4c662-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4c662-138">Mandatory</span></span><br/>    | <span data-ttu-id="4c662-139">строка</span><span class="sxs-lookup"><span data-stu-id="4c662-139">string</span></span><br/>  | <span data-ttu-id="4c662-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="4c662-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4c662-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="4c662-141">UnitType</span></span><br/>     | <span data-ttu-id="4c662-142">строка</span><span class="sxs-lookup"><span data-stu-id="4c662-142">string</span></span><br/>  | <span data-ttu-id="4c662-143">characters</span><span class="sxs-lookup"><span data-stu-id="4c662-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4c662-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4c662-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c662-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="4c662-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




