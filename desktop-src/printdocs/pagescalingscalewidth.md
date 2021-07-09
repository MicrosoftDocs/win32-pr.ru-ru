---
description: Получение сведений о параметре Пажескалингскалевидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: пажескалингскалевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6180395eb656ee40d8558f7208fec2ad2fce8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548802"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="a1d6f-105">пажескалингскалевидс</span><span class="sxs-lookup"><span data-stu-id="a1d6f-105">PageScalingScaleWidth</span></span>

<span data-ttu-id="a1d6f-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="a1d6f-106">This topic is not current.</span></span> <span data-ttu-id="a1d6f-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a1d6f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a1d6f-108">Задает коэффициент масштабирования в направлении Имажеаблесизевидс для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="a1d6f-108">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="a1d6f-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a1d6f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a1d6f-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="a1d6f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a1d6f-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a1d6f-111">Element Information</span></span>



| <span data-ttu-id="a1d6f-112">Имя</span><span class="sxs-lookup"><span data-stu-id="a1d6f-112">Name</span></span> | <span data-ttu-id="a1d6f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a1d6f-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="a1d6f-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a1d6f-114">Element Type</span></span> <br/>   | <span data-ttu-id="a1d6f-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="a1d6f-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="a1d6f-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="a1d6f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a1d6f-117">Страница</span><span class="sxs-lookup"><span data-stu-id="a1d6f-117">Page</span></span><br/>                                         |
| <span data-ttu-id="a1d6f-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1d6f-118">Notes</span></span> <br/>          | <span data-ttu-id="a1d6f-119">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="a1d6f-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a1d6f-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="a1d6f-120">Structure Content</span></span>

<span data-ttu-id="a1d6f-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="a1d6f-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a1d6f-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="a1d6f-122">Structure Properties</span></span>

<span data-ttu-id="a1d6f-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="a1d6f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a1d6f-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="a1d6f-124">Property</span></span>                | <span data-ttu-id="a1d6f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a1d6f-125">xsi:type</span></span>           | <span data-ttu-id="a1d6f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a1d6f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a1d6f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="a1d6f-127">DataType</span></span><br/>     | <span data-ttu-id="a1d6f-128">Строка</span><span class="sxs-lookup"><span data-stu-id="a1d6f-128">String</span></span><br/>  | <span data-ttu-id="a1d6f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a1d6f-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="a1d6f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a1d6f-130">DefaultValue</span></span><br/> | <span data-ttu-id="a1d6f-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="a1d6f-131">Integer</span></span><br/> | <span data-ttu-id="a1d6f-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a1d6f-132">undefined</span></span><br/>       |
| <span data-ttu-id="a1d6f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a1d6f-133">MaxValue</span></span><br/>     | <span data-ttu-id="a1d6f-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="a1d6f-134">Integer</span></span><br/> | <span data-ttu-id="a1d6f-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="a1d6f-135">undefined</span></span><br/>       |
| <span data-ttu-id="a1d6f-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="a1d6f-136">MinValue</span></span><br/>     | <span data-ttu-id="a1d6f-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="a1d6f-137">Integer</span></span><br/> | <span data-ttu-id="a1d6f-138">1</span><span class="sxs-lookup"><span data-stu-id="a1d6f-138">1</span></span><br/>               |
| <span data-ttu-id="a1d6f-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a1d6f-139">Mandatory</span></span><br/>    | <span data-ttu-id="a1d6f-140">Строка</span><span class="sxs-lookup"><span data-stu-id="a1d6f-140">String</span></span><br/>  | <span data-ttu-id="a1d6f-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="a1d6f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a1d6f-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="a1d6f-142">Multiple</span></span><br/>     | <span data-ttu-id="a1d6f-143">Целое число</span><span class="sxs-lookup"><span data-stu-id="a1d6f-143">Integer</span></span><br/> | <span data-ttu-id="a1d6f-144">1</span><span class="sxs-lookup"><span data-stu-id="a1d6f-144">1</span></span><br/>               |
| <span data-ttu-id="a1d6f-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="a1d6f-145">UnitType</span></span><br/>     | <span data-ttu-id="a1d6f-146">Строка</span><span class="sxs-lookup"><span data-stu-id="a1d6f-146">String</span></span><br/>  | <span data-ttu-id="a1d6f-147">мкм</span><span class="sxs-lookup"><span data-stu-id="a1d6f-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a1d6f-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a1d6f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1d6f-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a1d6f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




