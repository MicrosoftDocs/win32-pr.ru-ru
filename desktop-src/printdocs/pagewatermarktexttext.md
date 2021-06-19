---
description: Получите дополнительные сведения о параметре Пажеватермарктексттекст. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: пажеватермарктексттекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395969"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="cf853-105">пажеватермарктексттекст</span><span class="sxs-lookup"><span data-stu-id="cf853-105">PageWatermarkTextText</span></span>

<span data-ttu-id="cf853-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="cf853-106">This topic is not current.</span></span> <span data-ttu-id="cf853-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cf853-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cf853-108">Задает текст водяного знака.</span><span class="sxs-lookup"><span data-stu-id="cf853-108">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="cf853-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cf853-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cf853-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="cf853-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cf853-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cf853-111">Element Information</span></span>



| <span data-ttu-id="cf853-112">Имя</span><span class="sxs-lookup"><span data-stu-id="cf853-112">Name</span></span> | <span data-ttu-id="cf853-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cf853-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="cf853-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="cf853-114">Element Type</span></span> <br/>   | <span data-ttu-id="cf853-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="cf853-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="cf853-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="cf853-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cf853-117">Страница</span><span class="sxs-lookup"><span data-stu-id="cf853-117">Page</span></span><br/>                            |
| <span data-ttu-id="cf853-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf853-118">Notes</span></span> <br/>          | <span data-ttu-id="cf853-119">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="cf853-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cf853-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="cf853-120">Structure Content</span></span>

<span data-ttu-id="cf853-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cf853-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cf853-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="cf853-122">Structure Properties</span></span>

<span data-ttu-id="cf853-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="cf853-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cf853-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="cf853-124">Property</span></span>                | <span data-ttu-id="cf853-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cf853-125">xsi:type</span></span>           | <span data-ttu-id="cf853-126">Значение</span><span class="sxs-lookup"><span data-stu-id="cf853-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cf853-127">DataType</span><span class="sxs-lookup"><span data-stu-id="cf853-127">DataType</span></span><br/>     | <span data-ttu-id="cf853-128">Строка</span><span class="sxs-lookup"><span data-stu-id="cf853-128">String</span></span><br/>  | <span data-ttu-id="cf853-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="cf853-129">xs:string</span></span><br/>       |
| <span data-ttu-id="cf853-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cf853-130">DefaultValue</span></span><br/> | <span data-ttu-id="cf853-131">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="cf853-131">Integer</span></span><br/> | <span data-ttu-id="cf853-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="cf853-132">undefined</span></span><br/>       |
| <span data-ttu-id="cf853-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="cf853-133">MaxLength</span></span><br/>    | <span data-ttu-id="cf853-134">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="cf853-134">Integer</span></span><br/> | <span data-ttu-id="cf853-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="cf853-135">undefined</span></span><br/>       |
| <span data-ttu-id="cf853-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="cf853-136">MinLength</span></span><br/>    | <span data-ttu-id="cf853-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="cf853-137">Integer</span></span><br/> | <span data-ttu-id="cf853-138">1</span><span class="sxs-lookup"><span data-stu-id="cf853-138">1</span></span><br/>               |
| <span data-ttu-id="cf853-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cf853-139">Mandatory</span></span><br/>    | <span data-ttu-id="cf853-140">Строка</span><span class="sxs-lookup"><span data-stu-id="cf853-140">String</span></span><br/>  | <span data-ttu-id="cf853-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="cf853-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cf853-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="cf853-142">UnitType</span></span><br/>     | <span data-ttu-id="cf853-143">Строка</span><span class="sxs-lookup"><span data-stu-id="cf853-143">String</span></span><br/>  | <span data-ttu-id="cf853-144">characters</span><span class="sxs-lookup"><span data-stu-id="cf853-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="cf853-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cf853-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf853-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="cf853-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




