---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: жоббиндаллдокументсгуттер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219a86f016edf820532c20fa473876265776a4ee
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273346"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="30e2a-104">жоббиндаллдокументсгуттер</span><span class="sxs-lookup"><span data-stu-id="30e2a-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="30e2a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="30e2a-105">This topic is not current.</span></span> <span data-ttu-id="30e2a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="30e2a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="30e2a-107">Задает ширину переплета привязки.</span><span class="sxs-lookup"><span data-stu-id="30e2a-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="30e2a-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="30e2a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="30e2a-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="30e2a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="30e2a-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="30e2a-110">Element Information</span></span>



| <span data-ttu-id="30e2a-111">Имя</span><span class="sxs-lookup"><span data-stu-id="30e2a-111">Name</span></span>                       |                                         |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="30e2a-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="30e2a-112">Element Type</span></span> <br/>   | <span data-ttu-id="30e2a-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="30e2a-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="30e2a-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="30e2a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="30e2a-115">Задание</span><span class="sxs-lookup"><span data-stu-id="30e2a-115">Job</span></span> <br/>                         |
| <span data-ttu-id="30e2a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="30e2a-116">Notes</span></span> <br/>          | <span data-ttu-id="30e2a-117">Связано с элементом Жоббиндинг</span><span class="sxs-lookup"><span data-stu-id="30e2a-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="30e2a-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="30e2a-118">Structure Content</span></span>

<span data-ttu-id="30e2a-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="30e2a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="30e2a-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="30e2a-120">Structure Properties</span></span>

<span data-ttu-id="30e2a-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="30e2a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="30e2a-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="30e2a-122">Property</span></span>                | <span data-ttu-id="30e2a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="30e2a-123">xsi:type</span></span>           | <span data-ttu-id="30e2a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="30e2a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="30e2a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="30e2a-125">DataType</span></span><br/>     | <span data-ttu-id="30e2a-126">строка</span><span class="sxs-lookup"><span data-stu-id="30e2a-126">string</span></span><br/>  | <span data-ttu-id="30e2a-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30e2a-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="30e2a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="30e2a-128">DefaultValue</span></span><br/> | <span data-ttu-id="30e2a-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="30e2a-129">integer</span></span><br/> | <span data-ttu-id="30e2a-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="30e2a-130">undefined</span></span><br/>       |
| <span data-ttu-id="30e2a-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="30e2a-131">MaxValue</span></span><br/>     | <span data-ttu-id="30e2a-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="30e2a-132">integer</span></span><br/> | <span data-ttu-id="30e2a-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="30e2a-133">undefined</span></span><br/>       |
| <span data-ttu-id="30e2a-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="30e2a-134">MinValue</span></span><br/>     | <span data-ttu-id="30e2a-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="30e2a-135">integer</span></span><br/> | <span data-ttu-id="30e2a-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="30e2a-136">undefined</span></span><br/>       |
| <span data-ttu-id="30e2a-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="30e2a-137">Mandatory</span></span><br/>    | <span data-ttu-id="30e2a-138">Строка</span><span class="sxs-lookup"><span data-stu-id="30e2a-138">String</span></span><br/>  | <span data-ttu-id="30e2a-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="30e2a-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="30e2a-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="30e2a-140">Multiple</span></span><br/>     | <span data-ttu-id="30e2a-141">целое число</span><span class="sxs-lookup"><span data-stu-id="30e2a-141">integer</span></span><br/> | <span data-ttu-id="30e2a-142">1</span><span class="sxs-lookup"><span data-stu-id="30e2a-142">1</span></span><br/>               |
| <span data-ttu-id="30e2a-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="30e2a-143">UnitType</span></span><br/>     | <span data-ttu-id="30e2a-144">строка</span><span class="sxs-lookup"><span data-stu-id="30e2a-144">string</span></span><br/>  | <span data-ttu-id="30e2a-145">мкм</span><span class="sxs-lookup"><span data-stu-id="30e2a-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="30e2a-146">См. также</span><span class="sxs-lookup"><span data-stu-id="30e2a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e2a-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="30e2a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




