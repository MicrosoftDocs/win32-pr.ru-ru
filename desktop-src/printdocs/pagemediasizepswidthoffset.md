---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: пажемедиасизепсвидсоффсет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cb8440af2b35bbe8f3f4a82a567beee43d1d44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703506"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="41413-104">пажемедиасизепсвидсоффсет</span><span class="sxs-lookup"><span data-stu-id="41413-104">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="41413-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="41413-105">This topic is not current.</span></span> <span data-ttu-id="41413-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="41413-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="41413-107">Задает смещение, перпендикулярное направлению ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="41413-107">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="41413-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="41413-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="41413-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="41413-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="41413-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="41413-110">Element Information</span></span>



| <span data-ttu-id="41413-111">Имя</span><span class="sxs-lookup"><span data-stu-id="41413-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="41413-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="41413-112">Element Type</span></span> <br/>   | <span data-ttu-id="41413-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="41413-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="41413-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="41413-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="41413-115">Страница</span><span class="sxs-lookup"><span data-stu-id="41413-115">Page</span></span><br/>                                             |
| <span data-ttu-id="41413-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="41413-116">Notes</span></span> <br/>          | <span data-ttu-id="41413-117">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="41413-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="41413-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="41413-118">Structure Content</span></span>

<span data-ttu-id="41413-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="41413-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="41413-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="41413-120">Structure Properties</span></span>

<span data-ttu-id="41413-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="41413-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="41413-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="41413-122">Property</span></span>                | <span data-ttu-id="41413-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="41413-123">xsi:type</span></span>           | <span data-ttu-id="41413-124">Значение</span><span class="sxs-lookup"><span data-stu-id="41413-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="41413-125">DataType</span><span class="sxs-lookup"><span data-stu-id="41413-125">DataType</span></span><br/>     | <span data-ttu-id="41413-126">строка</span><span class="sxs-lookup"><span data-stu-id="41413-126">string</span></span><br/>  | <span data-ttu-id="41413-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="41413-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="41413-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="41413-128">DefaultValue</span></span><br/> | <span data-ttu-id="41413-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="41413-129">integer</span></span><br/> | <span data-ttu-id="41413-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="41413-130">undefined</span></span><br/>       |
| <span data-ttu-id="41413-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="41413-131">MaxValue</span></span><br/>     | <span data-ttu-id="41413-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="41413-132">integer</span></span><br/> | <span data-ttu-id="41413-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="41413-133">undefined</span></span><br/>       |
| <span data-ttu-id="41413-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="41413-134">MinValue</span></span><br/>     | <span data-ttu-id="41413-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="41413-135">integer</span></span><br/> | <span data-ttu-id="41413-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="41413-136">undefined</span></span><br/>       |
| <span data-ttu-id="41413-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="41413-137">Mandatory</span></span><br/>    | <span data-ttu-id="41413-138">строка</span><span class="sxs-lookup"><span data-stu-id="41413-138">string</span></span><br/>  | <span data-ttu-id="41413-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="41413-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="41413-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="41413-140">Multiple</span></span><br/>     | <span data-ttu-id="41413-141">целое число</span><span class="sxs-lookup"><span data-stu-id="41413-141">integer</span></span><br/> | <span data-ttu-id="41413-142">1</span><span class="sxs-lookup"><span data-stu-id="41413-142">1</span></span><br/>               |
| <span data-ttu-id="41413-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="41413-143">UnitType</span></span><br/>     | <span data-ttu-id="41413-144">строка</span><span class="sxs-lookup"><span data-stu-id="41413-144">string</span></span><br/>  | <span data-ttu-id="41413-145">мкм</span><span class="sxs-lookup"><span data-stu-id="41413-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="41413-146">См. также</span><span class="sxs-lookup"><span data-stu-id="41413-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41413-147">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="41413-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="41413-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="41413-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




