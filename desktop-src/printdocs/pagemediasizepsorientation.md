---
description: Получение сведений о параметре Пажемедиасизепсориентатион. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: пажемедиасизепсориентатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1b3aff1099199a98d6c8be899824dd1a1f17c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395729"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="f2343-105">пажемедиасизепсориентатион</span><span class="sxs-lookup"><span data-stu-id="f2343-105">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="f2343-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f2343-106">This topic is not current.</span></span> <span data-ttu-id="f2343-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f2343-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f2343-108">Задает ориентацию относительно направления ориентации канала ( [Спецификация формата файла описания PostScript-принтера](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="f2343-108">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="f2343-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f2343-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f2343-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f2343-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f2343-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f2343-111">Element Information</span></span>



| <span data-ttu-id="f2343-112">Имя</span><span class="sxs-lookup"><span data-stu-id="f2343-112">Name</span></span> | <span data-ttu-id="f2343-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f2343-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f2343-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f2343-114">Element Type</span></span> <br/>   | <span data-ttu-id="f2343-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="f2343-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="f2343-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f2343-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f2343-117">Страница</span><span class="sxs-lookup"><span data-stu-id="f2343-117">Page</span></span><br/>                                             |
| <span data-ttu-id="f2343-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2343-118">Notes</span></span> <br/>          | <span data-ttu-id="f2343-119">Ссылка на элемент Пажемедиасизе, параметр Кустомпс</span><span class="sxs-lookup"><span data-stu-id="f2343-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f2343-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f2343-120">Structure Content</span></span>

<span data-ttu-id="f2343-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f2343-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f2343-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="f2343-122">Structure Properties</span></span>

<span data-ttu-id="f2343-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f2343-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f2343-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="f2343-124">Property</span></span>                | <span data-ttu-id="f2343-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f2343-125">xsi:type</span></span>           | <span data-ttu-id="f2343-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f2343-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="f2343-127">DataType</span><span class="sxs-lookup"><span data-stu-id="f2343-127">DataType</span></span><br/>     | <span data-ttu-id="f2343-128">строка</span><span class="sxs-lookup"><span data-stu-id="f2343-128">string</span></span><br/>  | <span data-ttu-id="f2343-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f2343-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="f2343-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f2343-130">DefaultValue</span></span><br/> | <span data-ttu-id="f2343-131">целое число</span><span class="sxs-lookup"><span data-stu-id="f2343-131">integer</span></span><br/> | <span data-ttu-id="f2343-132">0</span><span class="sxs-lookup"><span data-stu-id="f2343-132">0</span></span><br/>                 |
| <span data-ttu-id="f2343-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f2343-133">MaxValue</span></span><br/>     | <span data-ttu-id="f2343-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="f2343-134">integer</span></span><br/> | <span data-ttu-id="f2343-135">3</span><span class="sxs-lookup"><span data-stu-id="f2343-135">3</span></span><br/>                 |
| <span data-ttu-id="f2343-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="f2343-136">MinValue</span></span><br/>     | <span data-ttu-id="f2343-137">целое число</span><span class="sxs-lookup"><span data-stu-id="f2343-137">integer</span></span><br/> | <span data-ttu-id="f2343-138">0</span><span class="sxs-lookup"><span data-stu-id="f2343-138">0</span></span><br/>                 |
| <span data-ttu-id="f2343-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f2343-139">Mandatory</span></span><br/>    | <span data-ttu-id="f2343-140">строка</span><span class="sxs-lookup"><span data-stu-id="f2343-140">string</span></span><br/>  | <span data-ttu-id="f2343-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="f2343-141">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="f2343-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="f2343-142">Multiple</span></span><br/>     | <span data-ttu-id="f2343-143">целое число</span><span class="sxs-lookup"><span data-stu-id="f2343-143">integer</span></span><br/> | <span data-ttu-id="f2343-144">1</span><span class="sxs-lookup"><span data-stu-id="f2343-144">1</span></span><br/>                 |
| <span data-ttu-id="f2343-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="f2343-145">UnitType</span></span><br/>     | <span data-ttu-id="f2343-146">строка</span><span class="sxs-lookup"><span data-stu-id="f2343-146">string</span></span><br/>  | <span data-ttu-id="f2343-147">пажемедиасизинум</span><span class="sxs-lookup"><span data-stu-id="f2343-147">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f2343-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f2343-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2343-149">Спецификация формата файла описания PostScript Printer</span><span class="sxs-lookup"><span data-stu-id="f2343-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="f2343-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f2343-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




