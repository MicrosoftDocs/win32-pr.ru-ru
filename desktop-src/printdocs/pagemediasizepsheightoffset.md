---
description: Получение сведений о параметре Пажемедиасизепшеигхтоффсет. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: пажемедиасизепшеигхтоффсет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395739"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="a631b-105">пажемедиасизепшеигхтоффсет</span><span class="sxs-lookup"><span data-stu-id="a631b-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="a631b-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="a631b-106">This topic is not current.</span></span> <span data-ttu-id="a631b-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a631b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a631b-108">Задает смещение, параллельное направлению ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="a631b-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="a631b-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a631b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a631b-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="a631b-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a631b-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a631b-111">Element Information</span></span>



| <span data-ttu-id="a631b-112">Имя</span><span class="sxs-lookup"><span data-stu-id="a631b-112">Name</span></span> | <span data-ttu-id="a631b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a631b-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a631b-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a631b-114">Element Type</span></span> <br/>   | <span data-ttu-id="a631b-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="a631b-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="a631b-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="a631b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a631b-117">Страница</span><span class="sxs-lookup"><span data-stu-id="a631b-117">Page</span></span><br/>                                             |
| <span data-ttu-id="a631b-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a631b-118">Notes</span></span> <br/>          | <span data-ttu-id="a631b-119">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="a631b-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a631b-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="a631b-120">Structure Content</span></span>

<span data-ttu-id="a631b-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="a631b-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="a631b-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="a631b-122">Structure Properties</span></span>

<span data-ttu-id="a631b-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="a631b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a631b-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="a631b-124">Property</span></span>                | <span data-ttu-id="a631b-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a631b-125">xsi:type</span></span>           | <span data-ttu-id="a631b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a631b-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a631b-127">DataType</span><span class="sxs-lookup"><span data-stu-id="a631b-127">DataType</span></span><br/>     | <span data-ttu-id="a631b-128">строка</span><span class="sxs-lookup"><span data-stu-id="a631b-128">string</span></span><br/>  | <span data-ttu-id="a631b-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a631b-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="a631b-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a631b-130">DefaultValue</span></span><br/> | <span data-ttu-id="a631b-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="a631b-131">integer</span></span><br/> | <span data-ttu-id="a631b-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a631b-132">undefined</span></span><br/>       |
| <span data-ttu-id="a631b-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a631b-133">MaxValue</span></span><br/>     | <span data-ttu-id="a631b-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="a631b-134">integer</span></span><br/> | <span data-ttu-id="a631b-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a631b-135">undefined</span></span><br/>       |
| <span data-ttu-id="a631b-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="a631b-136">MinValue</span></span><br/>     | <span data-ttu-id="a631b-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="a631b-137">integer</span></span><br/> | <span data-ttu-id="a631b-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a631b-138">undefined</span></span><br/>       |
| <span data-ttu-id="a631b-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a631b-139">Mandatory</span></span><br/>    | <span data-ttu-id="a631b-140">строка</span><span class="sxs-lookup"><span data-stu-id="a631b-140">string</span></span><br/>  | <span data-ttu-id="a631b-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="a631b-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a631b-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="a631b-142">Multiple</span></span><br/>     | <span data-ttu-id="a631b-143">целое число</span><span class="sxs-lookup"><span data-stu-id="a631b-143">integer</span></span><br/> | <span data-ttu-id="a631b-144">1</span><span class="sxs-lookup"><span data-stu-id="a631b-144">1</span></span><br/>               |
| <span data-ttu-id="a631b-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="a631b-145">UnitType</span></span><br/>     | <span data-ttu-id="a631b-146">строка</span><span class="sxs-lookup"><span data-stu-id="a631b-146">string</span></span><br/>  | <span data-ttu-id="a631b-147">мкм</span><span class="sxs-lookup"><span data-stu-id="a631b-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a631b-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a631b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a631b-149">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="a631b-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="a631b-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a631b-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




