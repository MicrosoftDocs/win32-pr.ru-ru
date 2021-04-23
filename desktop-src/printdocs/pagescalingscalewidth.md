---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: пажескалингскалевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7918f1a466621377e57190e0b967980fec1a07e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693931"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="f48d9-104">пажескалингскалевидс</span><span class="sxs-lookup"><span data-stu-id="f48d9-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="f48d9-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f48d9-105">This topic is not current.</span></span> <span data-ttu-id="f48d9-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f48d9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f48d9-107">Задает коэффициент масштабирования в направлении Имажеаблесизевидс для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f48d9-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="f48d9-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f48d9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f48d9-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f48d9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f48d9-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f48d9-110">Element Information</span></span>



| <span data-ttu-id="f48d9-111">Имя</span><span class="sxs-lookup"><span data-stu-id="f48d9-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="f48d9-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f48d9-112">Element Type</span></span> <br/>   | <span data-ttu-id="f48d9-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="f48d9-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="f48d9-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f48d9-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f48d9-115">Страница</span><span class="sxs-lookup"><span data-stu-id="f48d9-115">Page</span></span><br/>                                         |
| <span data-ttu-id="f48d9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f48d9-116">Notes</span></span> <br/>          | <span data-ttu-id="f48d9-117">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="f48d9-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f48d9-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="f48d9-118">Structure Content</span></span>

<span data-ttu-id="f48d9-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f48d9-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="f48d9-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="f48d9-120">Structure Properties</span></span>

<span data-ttu-id="f48d9-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f48d9-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f48d9-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="f48d9-122">Property</span></span>                | <span data-ttu-id="f48d9-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f48d9-123">xsi:type</span></span>           | <span data-ttu-id="f48d9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f48d9-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f48d9-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f48d9-125">DataType</span></span><br/>     | <span data-ttu-id="f48d9-126">Строка</span><span class="sxs-lookup"><span data-stu-id="f48d9-126">String</span></span><br/>  | <span data-ttu-id="f48d9-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f48d9-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f48d9-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f48d9-128">DefaultValue</span></span><br/> | <span data-ttu-id="f48d9-129">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="f48d9-129">Integer</span></span><br/> | <span data-ttu-id="f48d9-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="f48d9-130">undefined</span></span><br/>       |
| <span data-ttu-id="f48d9-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f48d9-131">MaxValue</span></span><br/>     | <span data-ttu-id="f48d9-132">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="f48d9-132">Integer</span></span><br/> | <span data-ttu-id="f48d9-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="f48d9-133">undefined</span></span><br/>       |
| <span data-ttu-id="f48d9-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f48d9-134">MinValue</span></span><br/>     | <span data-ttu-id="f48d9-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="f48d9-135">Integer</span></span><br/> | <span data-ttu-id="f48d9-136">1</span><span class="sxs-lookup"><span data-stu-id="f48d9-136">1</span></span><br/>               |
| <span data-ttu-id="f48d9-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f48d9-137">Mandatory</span></span><br/>    | <span data-ttu-id="f48d9-138">Строка</span><span class="sxs-lookup"><span data-stu-id="f48d9-138">String</span></span><br/>  | <span data-ttu-id="f48d9-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="f48d9-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f48d9-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="f48d9-140">Multiple</span></span><br/>     | <span data-ttu-id="f48d9-141">Целое число</span><span class="sxs-lookup"><span data-stu-id="f48d9-141">Integer</span></span><br/> | <span data-ttu-id="f48d9-142">1</span><span class="sxs-lookup"><span data-stu-id="f48d9-142">1</span></span><br/>               |
| <span data-ttu-id="f48d9-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="f48d9-143">UnitType</span></span><br/>     | <span data-ttu-id="f48d9-144">Строка</span><span class="sxs-lookup"><span data-stu-id="f48d9-144">String</span></span><br/>  | <span data-ttu-id="f48d9-145">мкм</span><span class="sxs-lookup"><span data-stu-id="f48d9-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f48d9-146">См. также</span><span class="sxs-lookup"><span data-stu-id="f48d9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f48d9-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f48d9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




