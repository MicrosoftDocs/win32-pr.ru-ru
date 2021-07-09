---
description: Получение сведений о параметре Пажескалингоффсесеигхт. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: пажескалингоффсесеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f02370d28716dd3a8840001959bb7d963307d2f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548962"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="e71ed-105">пажескалингоффсесеигхт</span><span class="sxs-lookup"><span data-stu-id="e71ed-105">PageScalingOffsetHeight</span></span>

<span data-ttu-id="e71ed-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e71ed-106">This topic is not current.</span></span> <span data-ttu-id="e71ed-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e71ed-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e71ed-108">Задает смещение масштабирования в направлении Имажеаблесизехеигхт для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e71ed-108">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="e71ed-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e71ed-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e71ed-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e71ed-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e71ed-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e71ed-111">Element Information</span></span>



| <span data-ttu-id="e71ed-112">Имя</span><span class="sxs-lookup"><span data-stu-id="e71ed-112">Name</span></span> | <span data-ttu-id="e71ed-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e71ed-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="e71ed-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e71ed-114">Element Type</span></span> <br/>   | <span data-ttu-id="e71ed-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="e71ed-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="e71ed-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e71ed-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e71ed-117">Страница</span><span class="sxs-lookup"><span data-stu-id="e71ed-117">Page</span></span><br/>                                         |
| <span data-ttu-id="e71ed-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="e71ed-118">Notes</span></span> <br/>          | <span data-ttu-id="e71ed-119">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="e71ed-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e71ed-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e71ed-120">Structure Content</span></span>

<span data-ttu-id="e71ed-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e71ed-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="e71ed-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="e71ed-122">Structure Properties</span></span>

<span data-ttu-id="e71ed-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e71ed-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e71ed-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="e71ed-124">Property</span></span>                | <span data-ttu-id="e71ed-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e71ed-125">xsi:type</span></span>           | <span data-ttu-id="e71ed-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e71ed-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e71ed-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e71ed-127">DataType</span></span><br/>     | <span data-ttu-id="e71ed-128">строка</span><span class="sxs-lookup"><span data-stu-id="e71ed-128">string</span></span><br/>  | <span data-ttu-id="e71ed-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e71ed-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="e71ed-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e71ed-130">DefaultValue</span></span><br/> | <span data-ttu-id="e71ed-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="e71ed-131">integer</span></span><br/> | <span data-ttu-id="e71ed-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e71ed-132">undefined</span></span><br/>       |
| <span data-ttu-id="e71ed-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e71ed-133">MaxValue</span></span><br/>     | <span data-ttu-id="e71ed-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="e71ed-134">integer</span></span><br/> | <span data-ttu-id="e71ed-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e71ed-135">undefined</span></span><br/>       |
| <span data-ttu-id="e71ed-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="e71ed-136">MinValue</span></span><br/>     | <span data-ttu-id="e71ed-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="e71ed-137">integer</span></span><br/> | <span data-ttu-id="e71ed-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e71ed-138">undefined</span></span><br/>       |
| <span data-ttu-id="e71ed-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e71ed-139">Mandatory</span></span><br/>    | <span data-ttu-id="e71ed-140">строка</span><span class="sxs-lookup"><span data-stu-id="e71ed-140">string</span></span><br/>  | <span data-ttu-id="e71ed-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="e71ed-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e71ed-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="e71ed-142">Multiple</span></span><br/>     | <span data-ttu-id="e71ed-143">целое число</span><span class="sxs-lookup"><span data-stu-id="e71ed-143">integer</span></span><br/> | <span data-ttu-id="e71ed-144">1</span><span class="sxs-lookup"><span data-stu-id="e71ed-144">1</span></span><br/>               |
| <span data-ttu-id="e71ed-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="e71ed-145">UnitType</span></span><br/>     | <span data-ttu-id="e71ed-146">строка</span><span class="sxs-lookup"><span data-stu-id="e71ed-146">string</span></span><br/>  | <span data-ttu-id="e71ed-147">мкм</span><span class="sxs-lookup"><span data-stu-id="e71ed-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e71ed-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e71ed-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e71ed-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e71ed-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




