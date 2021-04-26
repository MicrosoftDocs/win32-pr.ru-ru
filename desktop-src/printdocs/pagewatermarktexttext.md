---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: пажеватермарктексттекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb19f5965347e79732aa116e5be51f90e4ef6943
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996081"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="00dbf-104">пажеватермарктексттекст</span><span class="sxs-lookup"><span data-stu-id="00dbf-104">PageWatermarkTextText</span></span>

<span data-ttu-id="00dbf-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="00dbf-105">This topic is not current.</span></span> <span data-ttu-id="00dbf-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="00dbf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="00dbf-107">Задает текст водяного знака.</span><span class="sxs-lookup"><span data-stu-id="00dbf-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="00dbf-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="00dbf-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="00dbf-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="00dbf-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="00dbf-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="00dbf-110">Element Information</span></span>



| <span data-ttu-id="00dbf-111">Имя</span><span class="sxs-lookup"><span data-stu-id="00dbf-111">Name</span></span> | <span data-ttu-id="00dbf-112">Значение</span><span class="sxs-lookup"><span data-stu-id="00dbf-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="00dbf-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="00dbf-113">Element Type</span></span> <br/>   | <span data-ttu-id="00dbf-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="00dbf-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="00dbf-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="00dbf-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="00dbf-116">Страница</span><span class="sxs-lookup"><span data-stu-id="00dbf-116">Page</span></span><br/>                            |
| <span data-ttu-id="00dbf-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="00dbf-117">Notes</span></span> <br/>          | <span data-ttu-id="00dbf-118">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="00dbf-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="00dbf-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="00dbf-119">Structure Content</span></span>

<span data-ttu-id="00dbf-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="00dbf-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="00dbf-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="00dbf-121">Structure Properties</span></span>

<span data-ttu-id="00dbf-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="00dbf-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="00dbf-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="00dbf-123">Property</span></span>                | <span data-ttu-id="00dbf-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="00dbf-124">xsi:type</span></span>           | <span data-ttu-id="00dbf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="00dbf-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="00dbf-126">DataType</span><span class="sxs-lookup"><span data-stu-id="00dbf-126">DataType</span></span><br/>     | <span data-ttu-id="00dbf-127">Строковый</span><span class="sxs-lookup"><span data-stu-id="00dbf-127">String</span></span><br/>  | <span data-ttu-id="00dbf-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="00dbf-128">xs:string</span></span><br/>       |
| <span data-ttu-id="00dbf-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="00dbf-129">DefaultValue</span></span><br/> | <span data-ttu-id="00dbf-130">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="00dbf-130">Integer</span></span><br/> | <span data-ttu-id="00dbf-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="00dbf-131">undefined</span></span><br/>       |
| <span data-ttu-id="00dbf-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="00dbf-132">MaxLength</span></span><br/>    | <span data-ttu-id="00dbf-133">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="00dbf-133">Integer</span></span><br/> | <span data-ttu-id="00dbf-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="00dbf-134">undefined</span></span><br/>       |
| <span data-ttu-id="00dbf-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="00dbf-135">MinLength</span></span><br/>    | <span data-ttu-id="00dbf-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="00dbf-136">Integer</span></span><br/> | <span data-ttu-id="00dbf-137">1</span><span class="sxs-lookup"><span data-stu-id="00dbf-137">1</span></span><br/>               |
| <span data-ttu-id="00dbf-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00dbf-138">Mandatory</span></span><br/>    | <span data-ttu-id="00dbf-139">Строковый</span><span class="sxs-lookup"><span data-stu-id="00dbf-139">String</span></span><br/>  | <span data-ttu-id="00dbf-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="00dbf-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="00dbf-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="00dbf-141">UnitType</span></span><br/>     | <span data-ttu-id="00dbf-142">Строковый</span><span class="sxs-lookup"><span data-stu-id="00dbf-142">String</span></span><br/>  | <span data-ttu-id="00dbf-143">characters</span><span class="sxs-lookup"><span data-stu-id="00dbf-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="00dbf-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="00dbf-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00dbf-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="00dbf-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




