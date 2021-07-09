---
description: Получение сведений о параметре Пажемедиасизепшеигхт. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: пажемедиасизепшеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1e7a30935c27fadb5d6ebb8dfb8f377e05a5e3
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549107"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="107e2-105">пажемедиасизепшеигхт</span><span class="sxs-lookup"><span data-stu-id="107e2-105">PageMediaSizePSHeight</span></span>

<span data-ttu-id="107e2-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="107e2-106">This topic is not current.</span></span> <span data-ttu-id="107e2-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="107e2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="107e2-108">задает высоту страницы, параллельную направлению ориентации канала (ссылка [PostScript принтера описание формата файла](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="107e2-108">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="107e2-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="107e2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="107e2-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="107e2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="107e2-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="107e2-111">Element Information</span></span>



| <span data-ttu-id="107e2-112">Имя</span><span class="sxs-lookup"><span data-stu-id="107e2-112">Name</span></span> | <span data-ttu-id="107e2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="107e2-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="107e2-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="107e2-114">Element Type</span></span> <br/>   | <span data-ttu-id="107e2-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="107e2-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="107e2-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="107e2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="107e2-117">Страница</span><span class="sxs-lookup"><span data-stu-id="107e2-117">Page</span></span><br/>                                             |
| <span data-ttu-id="107e2-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="107e2-118">Notes</span></span> <br/>          | <span data-ttu-id="107e2-119">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="107e2-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="107e2-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="107e2-120">Structure Content</span></span>

<span data-ttu-id="107e2-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="107e2-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="107e2-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="107e2-122">Structure Properties</span></span>

<span data-ttu-id="107e2-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="107e2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="107e2-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="107e2-124">Property</span></span>                | <span data-ttu-id="107e2-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="107e2-125">xsi:type</span></span>           | <span data-ttu-id="107e2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="107e2-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="107e2-127">DataType</span><span class="sxs-lookup"><span data-stu-id="107e2-127">DataType</span></span><br/>     | <span data-ttu-id="107e2-128">строка</span><span class="sxs-lookup"><span data-stu-id="107e2-128">string</span></span><br/>  | <span data-ttu-id="107e2-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="107e2-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="107e2-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="107e2-130">DefaultValue</span></span><br/> | <span data-ttu-id="107e2-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="107e2-131">integer</span></span><br/> | <span data-ttu-id="107e2-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="107e2-132">undefined</span></span><br/>       |
| <span data-ttu-id="107e2-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="107e2-133">MaxValue</span></span><br/>     | <span data-ttu-id="107e2-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="107e2-134">integer</span></span><br/> | <span data-ttu-id="107e2-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="107e2-135">undefined</span></span><br/>       |
| <span data-ttu-id="107e2-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="107e2-136">MinValue</span></span><br/>     | <span data-ttu-id="107e2-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="107e2-137">integer</span></span><br/> | <span data-ttu-id="107e2-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="107e2-138">undefined</span></span><br/>       |
| <span data-ttu-id="107e2-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="107e2-139">Mandatory</span></span><br/>    | <span data-ttu-id="107e2-140">строка</span><span class="sxs-lookup"><span data-stu-id="107e2-140">string</span></span><br/>  | <span data-ttu-id="107e2-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="107e2-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="107e2-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="107e2-142">Multiple</span></span><br/>     | <span data-ttu-id="107e2-143">целое число</span><span class="sxs-lookup"><span data-stu-id="107e2-143">integer</span></span><br/> | <span data-ttu-id="107e2-144">1</span><span class="sxs-lookup"><span data-stu-id="107e2-144">1</span></span><br/>               |
| <span data-ttu-id="107e2-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="107e2-145">UnitType</span></span><br/>     | <span data-ttu-id="107e2-146">строка</span><span class="sxs-lookup"><span data-stu-id="107e2-146">string</span></span><br/>  | <span data-ttu-id="107e2-147">мкм</span><span class="sxs-lookup"><span data-stu-id="107e2-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="107e2-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="107e2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="107e2-149">PostScript Спецификация формата файла описания принтера</span><span class="sxs-lookup"><span data-stu-id="107e2-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="107e2-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="107e2-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




