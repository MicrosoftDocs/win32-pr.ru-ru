---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: пажеватермарктексттекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674561"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="26ec9-104">пажеватермарктексттекст</span><span class="sxs-lookup"><span data-stu-id="26ec9-104">PageWatermarkTextText</span></span>

<span data-ttu-id="26ec9-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="26ec9-105">This topic is not current.</span></span> <span data-ttu-id="26ec9-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="26ec9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="26ec9-107">Задает текст водяного знака.</span><span class="sxs-lookup"><span data-stu-id="26ec9-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="26ec9-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="26ec9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="26ec9-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="26ec9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="26ec9-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="26ec9-110">Element Information</span></span>



| <span data-ttu-id="26ec9-111">Имя</span><span class="sxs-lookup"><span data-stu-id="26ec9-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="26ec9-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="26ec9-112">Element Type</span></span> <br/>   | <span data-ttu-id="26ec9-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="26ec9-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="26ec9-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="26ec9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="26ec9-115">Страница</span><span class="sxs-lookup"><span data-stu-id="26ec9-115">Page</span></span><br/>                            |
| <span data-ttu-id="26ec9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="26ec9-116">Notes</span></span> <br/>          | <span data-ttu-id="26ec9-117">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="26ec9-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="26ec9-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="26ec9-118">Structure Content</span></span>

<span data-ttu-id="26ec9-119">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="26ec9-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="26ec9-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="26ec9-120">Structure Properties</span></span>

<span data-ttu-id="26ec9-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="26ec9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="26ec9-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="26ec9-122">Property</span></span>                | <span data-ttu-id="26ec9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="26ec9-123">xsi:type</span></span>           | <span data-ttu-id="26ec9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="26ec9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="26ec9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="26ec9-125">DataType</span></span><br/>     | <span data-ttu-id="26ec9-126">Строка</span><span class="sxs-lookup"><span data-stu-id="26ec9-126">String</span></span><br/>  | <span data-ttu-id="26ec9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="26ec9-127">xs:string</span></span><br/>       |
| <span data-ttu-id="26ec9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="26ec9-128">DefaultValue</span></span><br/> | <span data-ttu-id="26ec9-129">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="26ec9-129">Integer</span></span><br/> | <span data-ttu-id="26ec9-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="26ec9-130">undefined</span></span><br/>       |
| <span data-ttu-id="26ec9-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="26ec9-131">MaxLength</span></span><br/>    | <span data-ttu-id="26ec9-132">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="26ec9-132">Integer</span></span><br/> | <span data-ttu-id="26ec9-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="26ec9-133">undefined</span></span><br/>       |
| <span data-ttu-id="26ec9-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="26ec9-134">MinLength</span></span><br/>    | <span data-ttu-id="26ec9-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="26ec9-135">Integer</span></span><br/> | <span data-ttu-id="26ec9-136">1</span><span class="sxs-lookup"><span data-stu-id="26ec9-136">1</span></span><br/>               |
| <span data-ttu-id="26ec9-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="26ec9-137">Mandatory</span></span><br/>    | <span data-ttu-id="26ec9-138">Строка</span><span class="sxs-lookup"><span data-stu-id="26ec9-138">String</span></span><br/>  | <span data-ttu-id="26ec9-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="26ec9-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="26ec9-140">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="26ec9-140">UnitType</span></span><br/>     | <span data-ttu-id="26ec9-141">Строка</span><span class="sxs-lookup"><span data-stu-id="26ec9-141">String</span></span><br/>  | <span data-ttu-id="26ec9-142">characters</span><span class="sxs-lookup"><span data-stu-id="26ec9-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="26ec9-143">См. также</span><span class="sxs-lookup"><span data-stu-id="26ec9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ec9-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="26ec9-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




