---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: жобпримарибаннершитсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556390d58df3073263a6a6b666d98c48ceed6469
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997741"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="fcb13-104">жобпримарибаннершитсаурце</span><span class="sxs-lookup"><span data-stu-id="fcb13-104">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="fcb13-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="fcb13-105">This topic is not current.</span></span> <span data-ttu-id="fcb13-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fcb13-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fcb13-107">Указывает источник для основного настраиваемого листа заголовка для задания.</span><span class="sxs-lookup"><span data-stu-id="fcb13-107">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="fcb13-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fcb13-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fcb13-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="fcb13-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fcb13-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fcb13-110">Element Information</span></span>



| <span data-ttu-id="fcb13-111">Имя</span><span class="sxs-lookup"><span data-stu-id="fcb13-111">Name</span></span> | <span data-ttu-id="fcb13-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb13-112">Value</span></span> |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="fcb13-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="fcb13-113">Element Type</span></span> <br/>   | <span data-ttu-id="fcb13-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="fcb13-114">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="fcb13-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="fcb13-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fcb13-116">Задание</span><span class="sxs-lookup"><span data-stu-id="fcb13-116">Job</span></span><br/>                              |
| <span data-ttu-id="fcb13-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="fcb13-117">Notes</span></span> <br/>          | <span data-ttu-id="fcb13-118">Связано с элементом Жоббаннершит</span><span class="sxs-lookup"><span data-stu-id="fcb13-118">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fcb13-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="fcb13-119">Structure Content</span></span>

<span data-ttu-id="fcb13-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="fcb13-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="fcb13-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="fcb13-121">Structure Properties</span></span>

<span data-ttu-id="fcb13-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="fcb13-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fcb13-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="fcb13-123">Property</span></span>                | <span data-ttu-id="fcb13-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fcb13-124">xsi:type</span></span>           | <span data-ttu-id="fcb13-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb13-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fcb13-126">DataType</span><span class="sxs-lookup"><span data-stu-id="fcb13-126">DataType</span></span><br/>     | <span data-ttu-id="fcb13-127">строка</span><span class="sxs-lookup"><span data-stu-id="fcb13-127">string</span></span><br/>  | <span data-ttu-id="fcb13-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcb13-128">xs:string</span></span><br/>       |
| <span data-ttu-id="fcb13-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fcb13-129">DefaultValue</span></span><br/> | <span data-ttu-id="fcb13-130">строка</span><span class="sxs-lookup"><span data-stu-id="fcb13-130">string</span></span><br/>  | <span data-ttu-id="fcb13-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="fcb13-131">undefined</span></span><br/>       |
| <span data-ttu-id="fcb13-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fcb13-132">MaxLength</span></span><br/>    | <span data-ttu-id="fcb13-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="fcb13-133">integer</span></span><br/> | <span data-ttu-id="fcb13-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="fcb13-134">undefined</span></span><br/>       |
| <span data-ttu-id="fcb13-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="fcb13-135">MinLength</span></span><br/>    | <span data-ttu-id="fcb13-136">целое число</span><span class="sxs-lookup"><span data-stu-id="fcb13-136">integer</span></span><br/> | <span data-ttu-id="fcb13-137">1</span><span class="sxs-lookup"><span data-stu-id="fcb13-137">1</span></span><br/>               |
| <span data-ttu-id="fcb13-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fcb13-138">Mandatory</span></span><br/>    | <span data-ttu-id="fcb13-139">строка</span><span class="sxs-lookup"><span data-stu-id="fcb13-139">string</span></span><br/>  | <span data-ttu-id="fcb13-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="fcb13-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fcb13-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="fcb13-141">UnitType</span></span><br/>     | <span data-ttu-id="fcb13-142">строка</span><span class="sxs-lookup"><span data-stu-id="fcb13-142">string</span></span><br/>  | <span data-ttu-id="fcb13-143">characters</span><span class="sxs-lookup"><span data-stu-id="fcb13-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fcb13-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fcb13-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb13-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="fcb13-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




