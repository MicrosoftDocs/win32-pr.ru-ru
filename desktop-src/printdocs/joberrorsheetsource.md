---
description: Получение сведений о параметре Жоберроршитсаурце. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: жоберроршитсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656d71422c46800d6155c1dea1e221f9c6dfe021
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549392"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="ddb1a-105">жоберроршитсаурце</span><span class="sxs-lookup"><span data-stu-id="ddb1a-105">JobErrorSheetSource</span></span>

<span data-ttu-id="ddb1a-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-106">This topic is not current.</span></span> <span data-ttu-id="ddb1a-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ddb1a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ddb1a-108">Указывает источник настраиваемого листа ошибок.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-108">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="ddb1a-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ddb1a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ddb1a-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ddb1a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ddb1a-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ddb1a-111">Element Information</span></span>



| <span data-ttu-id="ddb1a-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ddb1a-112">Name</span></span> | <span data-ttu-id="ddb1a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ddb1a-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="ddb1a-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ddb1a-114">Element Type</span></span> <br/>   | <span data-ttu-id="ddb1a-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="ddb1a-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="ddb1a-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ddb1a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ddb1a-117">Документ</span><span class="sxs-lookup"><span data-stu-id="ddb1a-117">Document</span></span><br/>                        |
| <span data-ttu-id="ddb1a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ddb1a-118">Notes</span></span> <br/>          | <span data-ttu-id="ddb1a-119">Связано с элементом Жоберроршит</span><span class="sxs-lookup"><span data-stu-id="ddb1a-119">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ddb1a-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ddb1a-120">Structure Content</span></span>

<span data-ttu-id="ddb1a-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ddb1a-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ddb1a-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="ddb1a-122">Structure Properties</span></span>

<span data-ttu-id="ddb1a-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ddb1a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ddb1a-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="ddb1a-124">Property</span></span>                | <span data-ttu-id="ddb1a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ddb1a-125">xsi:type</span></span>           | <span data-ttu-id="ddb1a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ddb1a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ddb1a-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ddb1a-127">DataType</span></span><br/>     | <span data-ttu-id="ddb1a-128">строка</span><span class="sxs-lookup"><span data-stu-id="ddb1a-128">string</span></span><br/>  | <span data-ttu-id="ddb1a-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddb1a-129">xs:string</span></span><br/>       |
| <span data-ttu-id="ddb1a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ddb1a-130">DefaultValue</span></span><br/> | <span data-ttu-id="ddb1a-131">строка</span><span class="sxs-lookup"><span data-stu-id="ddb1a-131">string</span></span><br/>  | <span data-ttu-id="ddb1a-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ddb1a-132">undefined</span></span><br/>       |
| <span data-ttu-id="ddb1a-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="ddb1a-133">MaxLength</span></span><br/>    | <span data-ttu-id="ddb1a-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="ddb1a-134">integer</span></span><br/> | <span data-ttu-id="ddb1a-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ddb1a-135">undefined</span></span><br/>       |
| <span data-ttu-id="ddb1a-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="ddb1a-136">MinLength</span></span><br/>    | <span data-ttu-id="ddb1a-137">целое число</span><span class="sxs-lookup"><span data-stu-id="ddb1a-137">integer</span></span><br/> | <span data-ttu-id="ddb1a-138">1</span><span class="sxs-lookup"><span data-stu-id="ddb1a-138">1</span></span><br/>               |
| <span data-ttu-id="ddb1a-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddb1a-139">Mandatory</span></span><br/>    | <span data-ttu-id="ddb1a-140">строка</span><span class="sxs-lookup"><span data-stu-id="ddb1a-140">string</span></span><br/>  | <span data-ttu-id="ddb1a-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="ddb1a-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ddb1a-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="ddb1a-142">UnitType</span></span><br/>     | <span data-ttu-id="ddb1a-143">строка</span><span class="sxs-lookup"><span data-stu-id="ddb1a-143">string</span></span><br/>  | <span data-ttu-id="ddb1a-144">characters</span><span class="sxs-lookup"><span data-stu-id="ddb1a-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="ddb1a-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ddb1a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddb1a-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ddb1a-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




