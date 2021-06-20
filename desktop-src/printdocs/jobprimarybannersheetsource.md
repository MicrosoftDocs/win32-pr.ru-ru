---
description: Сведения об элементе Жобпримарибаннершитсаурце, который указывает источник для основного настраиваемого листа заголовка для задания.
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: жобпримарибаннершитсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366266576fca98762fd7d3dcb7e491a6cc94f529
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408717"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="c7456-103">жобпримарибаннершитсаурце</span><span class="sxs-lookup"><span data-stu-id="c7456-103">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="c7456-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c7456-104">This topic is not current.</span></span> <span data-ttu-id="c7456-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c7456-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c7456-106">Указывает источник для основного настраиваемого листа заголовка для задания.</span><span class="sxs-lookup"><span data-stu-id="c7456-106">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="c7456-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c7456-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c7456-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c7456-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c7456-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c7456-109">Element Information</span></span>



| <span data-ttu-id="c7456-110">Имя</span><span class="sxs-lookup"><span data-stu-id="c7456-110">Name</span></span> | <span data-ttu-id="c7456-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c7456-111">Value</span></span> |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="c7456-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c7456-112">Element Type</span></span> <br/>   | <span data-ttu-id="c7456-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="c7456-113">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="c7456-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c7456-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c7456-115">Задание</span><span class="sxs-lookup"><span data-stu-id="c7456-115">Job</span></span><br/>                              |
| <span data-ttu-id="c7456-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7456-116">Notes</span></span> <br/>          | <span data-ttu-id="c7456-117">Связано с элементом Жоббаннершит</span><span class="sxs-lookup"><span data-stu-id="c7456-117">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c7456-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c7456-118">Structure Content</span></span>

<span data-ttu-id="c7456-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c7456-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c7456-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="c7456-120">Structure Properties</span></span>

<span data-ttu-id="c7456-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c7456-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c7456-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="c7456-122">Property</span></span>                | <span data-ttu-id="c7456-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c7456-123">xsi:type</span></span>           | <span data-ttu-id="c7456-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c7456-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c7456-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c7456-125">DataType</span></span><br/>     | <span data-ttu-id="c7456-126">строка</span><span class="sxs-lookup"><span data-stu-id="c7456-126">string</span></span><br/>  | <span data-ttu-id="c7456-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7456-127">xs:string</span></span><br/>       |
| <span data-ttu-id="c7456-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c7456-128">DefaultValue</span></span><br/> | <span data-ttu-id="c7456-129">строка</span><span class="sxs-lookup"><span data-stu-id="c7456-129">string</span></span><br/>  | <span data-ttu-id="c7456-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c7456-130">undefined</span></span><br/>       |
| <span data-ttu-id="c7456-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="c7456-131">MaxLength</span></span><br/>    | <span data-ttu-id="c7456-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="c7456-132">integer</span></span><br/> | <span data-ttu-id="c7456-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c7456-133">undefined</span></span><br/>       |
| <span data-ttu-id="c7456-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="c7456-134">MinLength</span></span><br/>    | <span data-ttu-id="c7456-135">целое число</span><span class="sxs-lookup"><span data-stu-id="c7456-135">integer</span></span><br/> | <span data-ttu-id="c7456-136">1</span><span class="sxs-lookup"><span data-stu-id="c7456-136">1</span></span><br/>               |
| <span data-ttu-id="c7456-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c7456-137">Mandatory</span></span><br/>    | <span data-ttu-id="c7456-138">строка</span><span class="sxs-lookup"><span data-stu-id="c7456-138">string</span></span><br/>  | <span data-ttu-id="c7456-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="c7456-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c7456-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="c7456-140">UnitType</span></span><br/>     | <span data-ttu-id="c7456-141">строка</span><span class="sxs-lookup"><span data-stu-id="c7456-141">string</span></span><br/>  | <span data-ttu-id="c7456-142">characters</span><span class="sxs-lookup"><span data-stu-id="c7456-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="c7456-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c7456-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7456-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c7456-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




