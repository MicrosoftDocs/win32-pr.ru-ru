---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: пажескалингоффсесеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424138"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="8fbda-104">пажескалингоффсесеигхт</span><span class="sxs-lookup"><span data-stu-id="8fbda-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="8fbda-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8fbda-105">This topic is not current.</span></span> <span data-ttu-id="8fbda-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8fbda-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8fbda-107">Задает смещение масштабирования в направлении Имажеаблесизехеигхт для пользовательского масштабирования.</span><span class="sxs-lookup"><span data-stu-id="8fbda-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="8fbda-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8fbda-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8fbda-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8fbda-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8fbda-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8fbda-110">Element Information</span></span>



| <span data-ttu-id="8fbda-111">Имя</span><span class="sxs-lookup"><span data-stu-id="8fbda-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="8fbda-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8fbda-112">Element Type</span></span> <br/>   | <span data-ttu-id="8fbda-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="8fbda-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="8fbda-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8fbda-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8fbda-115">Страница</span><span class="sxs-lookup"><span data-stu-id="8fbda-115">Page</span></span><br/>                                         |
| <span data-ttu-id="8fbda-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8fbda-116">Notes</span></span> <br/>          | <span data-ttu-id="8fbda-117">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="8fbda-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8fbda-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8fbda-118">Structure Content</span></span>

<span data-ttu-id="8fbda-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8fbda-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8fbda-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="8fbda-120">Structure Properties</span></span>

<span data-ttu-id="8fbda-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8fbda-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8fbda-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="8fbda-122">Property</span></span>                | <span data-ttu-id="8fbda-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8fbda-123">xsi:type</span></span>           | <span data-ttu-id="8fbda-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbda-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8fbda-125">DataType</span><span class="sxs-lookup"><span data-stu-id="8fbda-125">DataType</span></span><br/>     | <span data-ttu-id="8fbda-126">строка</span><span class="sxs-lookup"><span data-stu-id="8fbda-126">string</span></span><br/>  | <span data-ttu-id="8fbda-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8fbda-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="8fbda-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8fbda-128">DefaultValue</span></span><br/> | <span data-ttu-id="8fbda-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="8fbda-129">integer</span></span><br/> | <span data-ttu-id="8fbda-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8fbda-130">undefined</span></span><br/>       |
| <span data-ttu-id="8fbda-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8fbda-131">MaxValue</span></span><br/>     | <span data-ttu-id="8fbda-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="8fbda-132">integer</span></span><br/> | <span data-ttu-id="8fbda-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8fbda-133">undefined</span></span><br/>       |
| <span data-ttu-id="8fbda-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="8fbda-134">MinValue</span></span><br/>     | <span data-ttu-id="8fbda-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="8fbda-135">integer</span></span><br/> | <span data-ttu-id="8fbda-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8fbda-136">undefined</span></span><br/>       |
| <span data-ttu-id="8fbda-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8fbda-137">Mandatory</span></span><br/>    | <span data-ttu-id="8fbda-138">строка</span><span class="sxs-lookup"><span data-stu-id="8fbda-138">string</span></span><br/>  | <span data-ttu-id="8fbda-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="8fbda-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8fbda-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="8fbda-140">Multiple</span></span><br/>     | <span data-ttu-id="8fbda-141">целое число</span><span class="sxs-lookup"><span data-stu-id="8fbda-141">integer</span></span><br/> | <span data-ttu-id="8fbda-142">1</span><span class="sxs-lookup"><span data-stu-id="8fbda-142">1</span></span><br/>               |
| <span data-ttu-id="8fbda-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="8fbda-143">UnitType</span></span><br/>     | <span data-ttu-id="8fbda-144">строка</span><span class="sxs-lookup"><span data-stu-id="8fbda-144">string</span></span><br/>  | <span data-ttu-id="8fbda-145">мкм</span><span class="sxs-lookup"><span data-stu-id="8fbda-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8fbda-146">См. также</span><span class="sxs-lookup"><span data-stu-id="8fbda-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbda-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8fbda-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




