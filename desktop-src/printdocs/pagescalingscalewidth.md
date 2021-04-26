---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: пажескалингскалевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ef53d9fe2906ae04cd1e7e3ea1513a631bc162
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997461"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="5c3ea-104">пажескалингскалевидс</span><span class="sxs-lookup"><span data-stu-id="5c3ea-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="5c3ea-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5c3ea-105">This topic is not current.</span></span> <span data-ttu-id="5c3ea-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5c3ea-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5c3ea-107">Задает коэффициент масштабирования в направлении Имажеаблесизевидс для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5c3ea-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="5c3ea-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5c3ea-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5c3ea-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="5c3ea-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5c3ea-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5c3ea-110">Element Information</span></span>



| <span data-ttu-id="5c3ea-111">Имя</span><span class="sxs-lookup"><span data-stu-id="5c3ea-111">Name</span></span> | <span data-ttu-id="5c3ea-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5c3ea-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="5c3ea-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5c3ea-113">Element Type</span></span> <br/>   | <span data-ttu-id="5c3ea-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="5c3ea-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="5c3ea-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5c3ea-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5c3ea-116">Страница</span><span class="sxs-lookup"><span data-stu-id="5c3ea-116">Page</span></span><br/>                                         |
| <span data-ttu-id="5c3ea-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c3ea-117">Notes</span></span> <br/>          | <span data-ttu-id="5c3ea-118">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="5c3ea-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5c3ea-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="5c3ea-119">Structure Content</span></span>

<span data-ttu-id="5c3ea-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="5c3ea-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5c3ea-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="5c3ea-121">Structure Properties</span></span>

<span data-ttu-id="5c3ea-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5c3ea-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5c3ea-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c3ea-123">Property</span></span>                | <span data-ttu-id="5c3ea-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5c3ea-124">xsi:type</span></span>           | <span data-ttu-id="5c3ea-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5c3ea-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5c3ea-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5c3ea-126">DataType</span></span><br/>     | <span data-ttu-id="5c3ea-127">Строковый</span><span class="sxs-lookup"><span data-stu-id="5c3ea-127">String</span></span><br/>  | <span data-ttu-id="5c3ea-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5c3ea-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="5c3ea-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5c3ea-129">DefaultValue</span></span><br/> | <span data-ttu-id="5c3ea-130">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5c3ea-130">Integer</span></span><br/> | <span data-ttu-id="5c3ea-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="5c3ea-131">undefined</span></span><br/>       |
| <span data-ttu-id="5c3ea-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5c3ea-132">MaxValue</span></span><br/>     | <span data-ttu-id="5c3ea-133">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="5c3ea-133">Integer</span></span><br/> | <span data-ttu-id="5c3ea-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="5c3ea-134">undefined</span></span><br/>       |
| <span data-ttu-id="5c3ea-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5c3ea-135">MinValue</span></span><br/>     | <span data-ttu-id="5c3ea-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="5c3ea-136">Integer</span></span><br/> | <span data-ttu-id="5c3ea-137">1</span><span class="sxs-lookup"><span data-stu-id="5c3ea-137">1</span></span><br/>               |
| <span data-ttu-id="5c3ea-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5c3ea-138">Mandatory</span></span><br/>    | <span data-ttu-id="5c3ea-139">Строковый</span><span class="sxs-lookup"><span data-stu-id="5c3ea-139">String</span></span><br/>  | <span data-ttu-id="5c3ea-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="5c3ea-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5c3ea-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="5c3ea-141">Multiple</span></span><br/>     | <span data-ttu-id="5c3ea-142">Целое число</span><span class="sxs-lookup"><span data-stu-id="5c3ea-142">Integer</span></span><br/> | <span data-ttu-id="5c3ea-143">1</span><span class="sxs-lookup"><span data-stu-id="5c3ea-143">1</span></span><br/>               |
| <span data-ttu-id="5c3ea-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="5c3ea-144">UnitType</span></span><br/>     | <span data-ttu-id="5c3ea-145">Строковый</span><span class="sxs-lookup"><span data-stu-id="5c3ea-145">String</span></span><br/>  | <span data-ttu-id="5c3ea-146">мкм</span><span class="sxs-lookup"><span data-stu-id="5c3ea-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5c3ea-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5c3ea-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c3ea-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5c3ea-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




