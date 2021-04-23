---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: пажемедиасизепсориентатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703484"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="2cf57-104">пажемедиасизепсориентатион</span><span class="sxs-lookup"><span data-stu-id="2cf57-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="2cf57-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2cf57-105">This topic is not current.</span></span> <span data-ttu-id="2cf57-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2cf57-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2cf57-107">Задает ориентацию относительно направления ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="2cf57-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="2cf57-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2cf57-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2cf57-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="2cf57-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2cf57-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2cf57-110">Element Information</span></span>



| <span data-ttu-id="2cf57-111">Имя</span><span class="sxs-lookup"><span data-stu-id="2cf57-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2cf57-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="2cf57-112">Element Type</span></span> <br/>   | <span data-ttu-id="2cf57-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="2cf57-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="2cf57-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="2cf57-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2cf57-115">Страница</span><span class="sxs-lookup"><span data-stu-id="2cf57-115">Page</span></span><br/>                                             |
| <span data-ttu-id="2cf57-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2cf57-116">Notes</span></span> <br/>          | <span data-ttu-id="2cf57-117">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="2cf57-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2cf57-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="2cf57-118">Structure Content</span></span>

<span data-ttu-id="2cf57-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="2cf57-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2cf57-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="2cf57-120">Structure Properties</span></span>

<span data-ttu-id="2cf57-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="2cf57-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2cf57-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="2cf57-122">Property</span></span>                | <span data-ttu-id="2cf57-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2cf57-123">xsi:type</span></span>           | <span data-ttu-id="2cf57-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2cf57-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="2cf57-125">DataType</span><span class="sxs-lookup"><span data-stu-id="2cf57-125">DataType</span></span><br/>     | <span data-ttu-id="2cf57-126">строка</span><span class="sxs-lookup"><span data-stu-id="2cf57-126">string</span></span><br/>  | <span data-ttu-id="2cf57-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2cf57-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="2cf57-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2cf57-128">DefaultValue</span></span><br/> | <span data-ttu-id="2cf57-129">целое число</span><span class="sxs-lookup"><span data-stu-id="2cf57-129">integer</span></span><br/> | <span data-ttu-id="2cf57-130">0</span><span class="sxs-lookup"><span data-stu-id="2cf57-130">0</span></span><br/>                 |
| <span data-ttu-id="2cf57-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2cf57-131">MaxValue</span></span><br/>     | <span data-ttu-id="2cf57-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="2cf57-132">integer</span></span><br/> | <span data-ttu-id="2cf57-133">3</span><span class="sxs-lookup"><span data-stu-id="2cf57-133">3</span></span><br/>                 |
| <span data-ttu-id="2cf57-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="2cf57-134">MinValue</span></span><br/>     | <span data-ttu-id="2cf57-135">целое число</span><span class="sxs-lookup"><span data-stu-id="2cf57-135">integer</span></span><br/> | <span data-ttu-id="2cf57-136">0</span><span class="sxs-lookup"><span data-stu-id="2cf57-136">0</span></span><br/>                 |
| <span data-ttu-id="2cf57-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2cf57-137">Mandatory</span></span><br/>    | <span data-ttu-id="2cf57-138">строка</span><span class="sxs-lookup"><span data-stu-id="2cf57-138">string</span></span><br/>  | <span data-ttu-id="2cf57-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="2cf57-139">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="2cf57-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="2cf57-140">Multiple</span></span><br/>     | <span data-ttu-id="2cf57-141">целое число</span><span class="sxs-lookup"><span data-stu-id="2cf57-141">integer</span></span><br/> | <span data-ttu-id="2cf57-142">1</span><span class="sxs-lookup"><span data-stu-id="2cf57-142">1</span></span><br/>                 |
| <span data-ttu-id="2cf57-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="2cf57-143">UnitType</span></span><br/>     | <span data-ttu-id="2cf57-144">строка</span><span class="sxs-lookup"><span data-stu-id="2cf57-144">string</span></span><br/>  | <span data-ttu-id="2cf57-145">пажемедиасизинум</span><span class="sxs-lookup"><span data-stu-id="2cf57-145">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2cf57-146">См. также</span><span class="sxs-lookup"><span data-stu-id="2cf57-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cf57-147">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="2cf57-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="2cf57-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2cf57-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




