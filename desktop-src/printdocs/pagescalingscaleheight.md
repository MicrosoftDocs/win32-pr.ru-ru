---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: пажескалингскалехеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d718d80f6b3cc369ddcb5c088a1299d639634b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997481"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="06cab-104">пажескалингскалехеигхт</span><span class="sxs-lookup"><span data-stu-id="06cab-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="06cab-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="06cab-105">This topic is not current.</span></span> <span data-ttu-id="06cab-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="06cab-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06cab-107">Задает коэффициент масштабирования в направлении Имажеаблесизехеигхт для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="06cab-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="06cab-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="06cab-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06cab-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="06cab-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="06cab-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="06cab-110">Element Information</span></span>



| <span data-ttu-id="06cab-111">Имя</span><span class="sxs-lookup"><span data-stu-id="06cab-111">Name</span></span> | <span data-ttu-id="06cab-112">Значение</span><span class="sxs-lookup"><span data-stu-id="06cab-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="06cab-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="06cab-113">Element Type</span></span> <br/>   | <span data-ttu-id="06cab-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="06cab-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="06cab-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="06cab-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06cab-116">Страница</span><span class="sxs-lookup"><span data-stu-id="06cab-116">Page</span></span><br/>                                         |
| <span data-ttu-id="06cab-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="06cab-117">Notes</span></span> <br/>          | <span data-ttu-id="06cab-118">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="06cab-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="06cab-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="06cab-119">Structure Content</span></span>

<span data-ttu-id="06cab-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="06cab-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="06cab-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="06cab-121">Structure Properties</span></span>

<span data-ttu-id="06cab-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="06cab-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06cab-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="06cab-123">Property</span></span>                | <span data-ttu-id="06cab-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="06cab-124">xsi:type</span></span>           | <span data-ttu-id="06cab-125">Значение</span><span class="sxs-lookup"><span data-stu-id="06cab-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="06cab-126">DataType</span><span class="sxs-lookup"><span data-stu-id="06cab-126">DataType</span></span><br/>     | <span data-ttu-id="06cab-127">Строковый</span><span class="sxs-lookup"><span data-stu-id="06cab-127">String</span></span><br/>  | <span data-ttu-id="06cab-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06cab-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="06cab-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="06cab-129">DefaultValue</span></span><br/> | <span data-ttu-id="06cab-130">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="06cab-130">Integer</span></span><br/> | <span data-ttu-id="06cab-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="06cab-131">undefined</span></span><br/>       |
| <span data-ttu-id="06cab-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="06cab-132">MaxValue</span></span><br/>     | <span data-ttu-id="06cab-133">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="06cab-133">Integer</span></span><br/> | <span data-ttu-id="06cab-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="06cab-134">undefined</span></span><br/>       |
| <span data-ttu-id="06cab-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="06cab-135">MinValue</span></span><br/>     | <span data-ttu-id="06cab-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="06cab-136">Integer</span></span><br/> | <span data-ttu-id="06cab-137">1</span><span class="sxs-lookup"><span data-stu-id="06cab-137">1</span></span><br/>               |
| <span data-ttu-id="06cab-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="06cab-138">Mandatory</span></span><br/>    | <span data-ttu-id="06cab-139">Строковый</span><span class="sxs-lookup"><span data-stu-id="06cab-139">String</span></span><br/>  | <span data-ttu-id="06cab-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="06cab-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="06cab-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="06cab-141">Multiple</span></span><br/>     | <span data-ttu-id="06cab-142">Целое число</span><span class="sxs-lookup"><span data-stu-id="06cab-142">Integer</span></span><br/> | <span data-ttu-id="06cab-143">1</span><span class="sxs-lookup"><span data-stu-id="06cab-143">1</span></span><br/>               |
| <span data-ttu-id="06cab-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="06cab-144">UnitType</span></span><br/>     | <span data-ttu-id="06cab-145">Строковый</span><span class="sxs-lookup"><span data-stu-id="06cab-145">String</span></span><br/>  | <span data-ttu-id="06cab-146">percent</span><span class="sxs-lookup"><span data-stu-id="06cab-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="06cab-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="06cab-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06cab-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="06cab-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




