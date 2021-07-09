---
description: Получение сведений о параметре Пажескалингскалехеигхт. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: пажескалингскалехеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51bdb5577b5e3863cfadab1fa9eb74ff40d54da
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548842"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="994eb-105">пажескалингскалехеигхт</span><span class="sxs-lookup"><span data-stu-id="994eb-105">PageScalingScaleHeight</span></span>

<span data-ttu-id="994eb-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="994eb-106">This topic is not current.</span></span> <span data-ttu-id="994eb-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="994eb-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="994eb-108">Задает коэффициент масштабирования в направлении Имажеаблесизехеигхт для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="994eb-108">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="994eb-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="994eb-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="994eb-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="994eb-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="994eb-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="994eb-111">Element Information</span></span>



| <span data-ttu-id="994eb-112">Имя</span><span class="sxs-lookup"><span data-stu-id="994eb-112">Name</span></span> | <span data-ttu-id="994eb-113">Значение</span><span class="sxs-lookup"><span data-stu-id="994eb-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="994eb-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="994eb-114">Element Type</span></span> <br/>   | <span data-ttu-id="994eb-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="994eb-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="994eb-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="994eb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="994eb-117">Страница</span><span class="sxs-lookup"><span data-stu-id="994eb-117">Page</span></span><br/>                                         |
| <span data-ttu-id="994eb-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="994eb-118">Notes</span></span> <br/>          | <span data-ttu-id="994eb-119">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="994eb-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="994eb-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="994eb-120">Structure Content</span></span>

<span data-ttu-id="994eb-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="994eb-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="994eb-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="994eb-122">Structure Properties</span></span>

<span data-ttu-id="994eb-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="994eb-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="994eb-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="994eb-124">Property</span></span>                | <span data-ttu-id="994eb-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="994eb-125">xsi:type</span></span>           | <span data-ttu-id="994eb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="994eb-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="994eb-127">DataType</span><span class="sxs-lookup"><span data-stu-id="994eb-127">DataType</span></span><br/>     | <span data-ttu-id="994eb-128">Строка</span><span class="sxs-lookup"><span data-stu-id="994eb-128">String</span></span><br/>  | <span data-ttu-id="994eb-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="994eb-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="994eb-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="994eb-130">DefaultValue</span></span><br/> | <span data-ttu-id="994eb-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="994eb-131">Integer</span></span><br/> | <span data-ttu-id="994eb-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="994eb-132">undefined</span></span><br/>       |
| <span data-ttu-id="994eb-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="994eb-133">MaxValue</span></span><br/>     | <span data-ttu-id="994eb-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="994eb-134">Integer</span></span><br/> | <span data-ttu-id="994eb-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="994eb-135">undefined</span></span><br/>       |
| <span data-ttu-id="994eb-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="994eb-136">MinValue</span></span><br/>     | <span data-ttu-id="994eb-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="994eb-137">Integer</span></span><br/> | <span data-ttu-id="994eb-138">1</span><span class="sxs-lookup"><span data-stu-id="994eb-138">1</span></span><br/>               |
| <span data-ttu-id="994eb-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="994eb-139">Mandatory</span></span><br/>    | <span data-ttu-id="994eb-140">Строка</span><span class="sxs-lookup"><span data-stu-id="994eb-140">String</span></span><br/>  | <span data-ttu-id="994eb-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="994eb-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="994eb-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="994eb-142">Multiple</span></span><br/>     | <span data-ttu-id="994eb-143">Целое число</span><span class="sxs-lookup"><span data-stu-id="994eb-143">Integer</span></span><br/> | <span data-ttu-id="994eb-144">1</span><span class="sxs-lookup"><span data-stu-id="994eb-144">1</span></span><br/>               |
| <span data-ttu-id="994eb-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="994eb-145">UnitType</span></span><br/>     | <span data-ttu-id="994eb-146">Строка</span><span class="sxs-lookup"><span data-stu-id="994eb-146">String</span></span><br/>  | <span data-ttu-id="994eb-147">percent</span><span class="sxs-lookup"><span data-stu-id="994eb-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="994eb-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="994eb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="994eb-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="994eb-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




