---
description: Получение сведений о параметре Пажескалингоффсетвидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: пажескалингоффсетвидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63152e6a3d9f8ea47bac3b5a0efe559e71e0cb35
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548852"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="51f88-105">пажескалингоффсетвидс</span><span class="sxs-lookup"><span data-stu-id="51f88-105">PageScalingOffsetWidth</span></span>

<span data-ttu-id="51f88-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="51f88-106">This topic is not current.</span></span> <span data-ttu-id="51f88-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="51f88-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="51f88-108">Задает смещение масштабирования в направлении Имажеаблесизевидс для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="51f88-108">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="51f88-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="51f88-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="51f88-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="51f88-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="51f88-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="51f88-111">Element Information</span></span>



| <span data-ttu-id="51f88-112">Имя</span><span class="sxs-lookup"><span data-stu-id="51f88-112">Name</span></span> | <span data-ttu-id="51f88-113">Значение</span><span class="sxs-lookup"><span data-stu-id="51f88-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="51f88-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="51f88-114">Element Type</span></span> <br/>   | <span data-ttu-id="51f88-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="51f88-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="51f88-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="51f88-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="51f88-117">Страница</span><span class="sxs-lookup"><span data-stu-id="51f88-117">Page</span></span><br/>                                         |
| <span data-ttu-id="51f88-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="51f88-118">Notes</span></span> <br/>          | <span data-ttu-id="51f88-119">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="51f88-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="51f88-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="51f88-120">Structure Content</span></span>

<span data-ttu-id="51f88-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="51f88-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="51f88-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="51f88-122">Structure Properties</span></span>

<span data-ttu-id="51f88-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="51f88-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="51f88-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="51f88-124">Property</span></span>                | <span data-ttu-id="51f88-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="51f88-125">xsi:type</span></span>           | <span data-ttu-id="51f88-126">Значение</span><span class="sxs-lookup"><span data-stu-id="51f88-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="51f88-127">DataType</span><span class="sxs-lookup"><span data-stu-id="51f88-127">DataType</span></span><br/>     | <span data-ttu-id="51f88-128">строка</span><span class="sxs-lookup"><span data-stu-id="51f88-128">string</span></span><br/>  | <span data-ttu-id="51f88-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="51f88-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="51f88-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="51f88-130">DefaultValue</span></span><br/> | <span data-ttu-id="51f88-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="51f88-131">integer</span></span><br/> | <span data-ttu-id="51f88-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="51f88-132">undefined</span></span><br/>       |
| <span data-ttu-id="51f88-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="51f88-133">MaxValue</span></span><br/>     | <span data-ttu-id="51f88-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="51f88-134">integer</span></span><br/> | <span data-ttu-id="51f88-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="51f88-135">undefined</span></span><br/>       |
| <span data-ttu-id="51f88-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="51f88-136">MinValue</span></span><br/>     | <span data-ttu-id="51f88-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="51f88-137">integer</span></span><br/> | <span data-ttu-id="51f88-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="51f88-138">undefined</span></span><br/>       |
| <span data-ttu-id="51f88-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51f88-139">Mandatory</span></span><br/>    | <span data-ttu-id="51f88-140">строка</span><span class="sxs-lookup"><span data-stu-id="51f88-140">string</span></span><br/>  | <span data-ttu-id="51f88-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="51f88-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="51f88-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="51f88-142">Multiple</span></span><br/>     | <span data-ttu-id="51f88-143">целое число</span><span class="sxs-lookup"><span data-stu-id="51f88-143">integer</span></span><br/> | <span data-ttu-id="51f88-144">1</span><span class="sxs-lookup"><span data-stu-id="51f88-144">1</span></span><br/>               |
| <span data-ttu-id="51f88-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="51f88-145">UnitType</span></span><br/>     | <span data-ttu-id="51f88-146">строка</span><span class="sxs-lookup"><span data-stu-id="51f88-146">string</span></span><br/>  | <span data-ttu-id="51f88-147">мкм</span><span class="sxs-lookup"><span data-stu-id="51f88-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="51f88-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="51f88-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51f88-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="51f88-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




