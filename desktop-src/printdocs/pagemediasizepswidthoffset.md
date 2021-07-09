---
description: Получение сведений о параметре Пажемедиасизепсвидсоффсет. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: пажемедиасизепсвидсоффсет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549110"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="c3c2c-105">пажемедиасизепсвидсоффсет</span><span class="sxs-lookup"><span data-stu-id="c3c2c-105">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="c3c2c-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-106">This topic is not current.</span></span> <span data-ttu-id="c3c2c-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c3c2c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c3c2c-108">задает смещение, перпендикулярное направлению ориентации веб-канала [PostScript (спецификация формата файла описания принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="c3c2c-108">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="c3c2c-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c3c2c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c3c2c-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c3c2c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c3c2c-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c3c2c-111">Element Information</span></span>



| <span data-ttu-id="c3c2c-112">Имя</span><span class="sxs-lookup"><span data-stu-id="c3c2c-112">Name</span></span> | <span data-ttu-id="c3c2c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c3c2c-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c3c2c-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c3c2c-114">Element Type</span></span> <br/>   | <span data-ttu-id="c3c2c-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="c3c2c-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="c3c2c-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c3c2c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c3c2c-117">Страница</span><span class="sxs-lookup"><span data-stu-id="c3c2c-117">Page</span></span><br/>                                             |
| <span data-ttu-id="c3c2c-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3c2c-118">Notes</span></span> <br/>          | <span data-ttu-id="c3c2c-119">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="c3c2c-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c3c2c-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c3c2c-120">Structure Content</span></span>

<span data-ttu-id="c3c2c-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c3c2c-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c3c2c-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="c3c2c-122">Structure Properties</span></span>

<span data-ttu-id="c3c2c-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c3c2c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c3c2c-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="c3c2c-124">Property</span></span>                | <span data-ttu-id="c3c2c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c3c2c-125">xsi:type</span></span>           | <span data-ttu-id="c3c2c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c3c2c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c3c2c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="c3c2c-127">DataType</span></span><br/>     | <span data-ttu-id="c3c2c-128">строка</span><span class="sxs-lookup"><span data-stu-id="c3c2c-128">string</span></span><br/>  | <span data-ttu-id="c3c2c-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c3c2c-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="c3c2c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c3c2c-130">DefaultValue</span></span><br/> | <span data-ttu-id="c3c2c-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="c3c2c-131">integer</span></span><br/> | <span data-ttu-id="c3c2c-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c3c2c-132">undefined</span></span><br/>       |
| <span data-ttu-id="c3c2c-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c3c2c-133">MaxValue</span></span><br/>     | <span data-ttu-id="c3c2c-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="c3c2c-134">integer</span></span><br/> | <span data-ttu-id="c3c2c-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c3c2c-135">undefined</span></span><br/>       |
| <span data-ttu-id="c3c2c-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="c3c2c-136">MinValue</span></span><br/>     | <span data-ttu-id="c3c2c-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="c3c2c-137">integer</span></span><br/> | <span data-ttu-id="c3c2c-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c3c2c-138">undefined</span></span><br/>       |
| <span data-ttu-id="c3c2c-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c3c2c-139">Mandatory</span></span><br/>    | <span data-ttu-id="c3c2c-140">строка</span><span class="sxs-lookup"><span data-stu-id="c3c2c-140">string</span></span><br/>  | <span data-ttu-id="c3c2c-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="c3c2c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c3c2c-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="c3c2c-142">Multiple</span></span><br/>     | <span data-ttu-id="c3c2c-143">целое число</span><span class="sxs-lookup"><span data-stu-id="c3c2c-143">integer</span></span><br/> | <span data-ttu-id="c3c2c-144">1</span><span class="sxs-lookup"><span data-stu-id="c3c2c-144">1</span></span><br/>               |
| <span data-ttu-id="c3c2c-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="c3c2c-145">UnitType</span></span><br/>     | <span data-ttu-id="c3c2c-146">строка</span><span class="sxs-lookup"><span data-stu-id="c3c2c-146">string</span></span><br/>  | <span data-ttu-id="c3c2c-147">мкм</span><span class="sxs-lookup"><span data-stu-id="c3c2c-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c3c2c-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c3c2c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3c2c-149">PostScript Спецификация формата файла описания принтера</span><span class="sxs-lookup"><span data-stu-id="c3c2c-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="c3c2c-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c3c2c-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




