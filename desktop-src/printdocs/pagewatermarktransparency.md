---
description: Получение сведений о параметре Пажеватермарктранспаренци. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: пажеватермарктранспаренци
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394789"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="60980-105">пажеватермарктранспаренци</span><span class="sxs-lookup"><span data-stu-id="60980-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="60980-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="60980-106">This topic is not current.</span></span> <span data-ttu-id="60980-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="60980-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="60980-108">Задает прозрачность для водяного знака.</span><span class="sxs-lookup"><span data-stu-id="60980-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="60980-109">Полностью непрозрачное значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="60980-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="60980-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="60980-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="60980-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="60980-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="60980-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="60980-112">Element Information</span></span>



| <span data-ttu-id="60980-113">Имя</span><span class="sxs-lookup"><span data-stu-id="60980-113">Name</span></span> | <span data-ttu-id="60980-114">Значение</span><span class="sxs-lookup"><span data-stu-id="60980-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="60980-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="60980-115">Element Type</span></span> <br/>   | <span data-ttu-id="60980-116">параметердеф</span><span class="sxs-lookup"><span data-stu-id="60980-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="60980-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="60980-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="60980-118">Страница</span><span class="sxs-lookup"><span data-stu-id="60980-118">Page</span></span><br/>                            |
| <span data-ttu-id="60980-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="60980-119">Notes</span></span> <br/>          | <span data-ttu-id="60980-120">Связано с элементом Пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="60980-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="60980-121">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="60980-121">Structure Content</span></span>

<span data-ttu-id="60980-122">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="60980-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="60980-123">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="60980-123">Structure Properties</span></span>

<span data-ttu-id="60980-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="60980-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="60980-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="60980-125">Property</span></span>                | <span data-ttu-id="60980-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="60980-126">xsi:type</span></span>           | <span data-ttu-id="60980-127">Значение</span><span class="sxs-lookup"><span data-stu-id="60980-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="60980-128">DataType</span><span class="sxs-lookup"><span data-stu-id="60980-128">DataType</span></span><br/>     | <span data-ttu-id="60980-129">строка</span><span class="sxs-lookup"><span data-stu-id="60980-129">string</span></span><br/>  | <span data-ttu-id="60980-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="60980-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="60980-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="60980-131">DefaultValue</span></span><br/> | <span data-ttu-id="60980-132">целое число</span><span class="sxs-lookup"><span data-stu-id="60980-132">integer</span></span><br/> | <span data-ttu-id="60980-133">0</span><span class="sxs-lookup"><span data-stu-id="60980-133">0</span></span><br/>               |
| <span data-ttu-id="60980-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="60980-134">MaxValue</span></span><br/>     | <span data-ttu-id="60980-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="60980-135">integer</span></span><br/> | <span data-ttu-id="60980-136">100</span><span class="sxs-lookup"><span data-stu-id="60980-136">100</span></span><br/>             |
| <span data-ttu-id="60980-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="60980-137">MinValue</span></span><br/>     | <span data-ttu-id="60980-138">целое число</span><span class="sxs-lookup"><span data-stu-id="60980-138">integer</span></span><br/> | <span data-ttu-id="60980-139">0</span><span class="sxs-lookup"><span data-stu-id="60980-139">0</span></span><br/>               |
| <span data-ttu-id="60980-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="60980-140">Multiple</span></span><br/>     | <span data-ttu-id="60980-141">целое число</span><span class="sxs-lookup"><span data-stu-id="60980-141">integer</span></span><br/> | <span data-ttu-id="60980-142">1</span><span class="sxs-lookup"><span data-stu-id="60980-142">1</span></span><br/>               |
| <span data-ttu-id="60980-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60980-143">Mandatory</span></span><br/>    | <span data-ttu-id="60980-144">строка</span><span class="sxs-lookup"><span data-stu-id="60980-144">string</span></span><br/>  | <span data-ttu-id="60980-145">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="60980-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="60980-146">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="60980-146">UnitType</span></span><br/>     | <span data-ttu-id="60980-147">строка</span><span class="sxs-lookup"><span data-stu-id="60980-147">string</span></span><br/>  | <span data-ttu-id="60980-148">percent</span><span class="sxs-lookup"><span data-stu-id="60980-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="60980-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="60980-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60980-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="60980-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




