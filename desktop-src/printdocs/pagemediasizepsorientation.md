---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: пажемедиасизепсориентатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997561"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="e9c7d-104">пажемедиасизепсориентатион</span><span class="sxs-lookup"><span data-stu-id="e9c7d-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="e9c7d-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-105">This topic is not current.</span></span> <span data-ttu-id="e9c7d-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e9c7d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e9c7d-107">Задает ориентацию относительно направления ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="e9c7d-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="e9c7d-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e9c7d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e9c7d-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e9c7d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e9c7d-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e9c7d-110">Element Information</span></span>



| <span data-ttu-id="e9c7d-111">Имя</span><span class="sxs-lookup"><span data-stu-id="e9c7d-111">Name</span></span> | <span data-ttu-id="e9c7d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e9c7d-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e9c7d-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e9c7d-113">Element Type</span></span> <br/>   | <span data-ttu-id="e9c7d-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="e9c7d-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="e9c7d-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e9c7d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e9c7d-116">Страница</span><span class="sxs-lookup"><span data-stu-id="e9c7d-116">Page</span></span><br/>                                             |
| <span data-ttu-id="e9c7d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9c7d-117">Notes</span></span> <br/>          | <span data-ttu-id="e9c7d-118">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="e9c7d-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e9c7d-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e9c7d-119">Structure Content</span></span>

<span data-ttu-id="e9c7d-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e9c7d-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="e9c7d-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="e9c7d-121">Structure Properties</span></span>

<span data-ttu-id="e9c7d-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e9c7d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e9c7d-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="e9c7d-123">Property</span></span>                | <span data-ttu-id="e9c7d-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e9c7d-124">xsi:type</span></span>           | <span data-ttu-id="e9c7d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e9c7d-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="e9c7d-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e9c7d-126">DataType</span></span><br/>     | <span data-ttu-id="e9c7d-127">строка</span><span class="sxs-lookup"><span data-stu-id="e9c7d-127">string</span></span><br/>  | <span data-ttu-id="e9c7d-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e9c7d-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="e9c7d-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e9c7d-129">DefaultValue</span></span><br/> | <span data-ttu-id="e9c7d-130">целое число</span><span class="sxs-lookup"><span data-stu-id="e9c7d-130">integer</span></span><br/> | <span data-ttu-id="e9c7d-131">0</span><span class="sxs-lookup"><span data-stu-id="e9c7d-131">0</span></span><br/>                 |
| <span data-ttu-id="e9c7d-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e9c7d-132">MaxValue</span></span><br/>     | <span data-ttu-id="e9c7d-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="e9c7d-133">integer</span></span><br/> | <span data-ttu-id="e9c7d-134">3</span><span class="sxs-lookup"><span data-stu-id="e9c7d-134">3</span></span><br/>                 |
| <span data-ttu-id="e9c7d-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="e9c7d-135">MinValue</span></span><br/>     | <span data-ttu-id="e9c7d-136">целое число</span><span class="sxs-lookup"><span data-stu-id="e9c7d-136">integer</span></span><br/> | <span data-ttu-id="e9c7d-137">0</span><span class="sxs-lookup"><span data-stu-id="e9c7d-137">0</span></span><br/>                 |
| <span data-ttu-id="e9c7d-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9c7d-138">Mandatory</span></span><br/>    | <span data-ttu-id="e9c7d-139">строка</span><span class="sxs-lookup"><span data-stu-id="e9c7d-139">string</span></span><br/>  | <span data-ttu-id="e9c7d-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="e9c7d-140">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="e9c7d-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="e9c7d-141">Multiple</span></span><br/>     | <span data-ttu-id="e9c7d-142">целое число</span><span class="sxs-lookup"><span data-stu-id="e9c7d-142">integer</span></span><br/> | <span data-ttu-id="e9c7d-143">1</span><span class="sxs-lookup"><span data-stu-id="e9c7d-143">1</span></span><br/>                 |
| <span data-ttu-id="e9c7d-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="e9c7d-144">UnitType</span></span><br/>     | <span data-ttu-id="e9c7d-145">строка</span><span class="sxs-lookup"><span data-stu-id="e9c7d-145">string</span></span><br/>  | <span data-ttu-id="e9c7d-146">пажемедиасизинум</span><span class="sxs-lookup"><span data-stu-id="e9c7d-146">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e9c7d-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e9c7d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9c7d-148">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="e9c7d-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="e9c7d-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e9c7d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




