---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: документбиндинггуттер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2372636ea22610e6a209cfad3f1fe6297be34833
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997191"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="ba1be-104">документбиндинггуттер</span><span class="sxs-lookup"><span data-stu-id="ba1be-104">DocumentBindingGutter</span></span>

<span data-ttu-id="ba1be-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ba1be-105">This topic is not current.</span></span> <span data-ttu-id="ba1be-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ba1be-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ba1be-107">Задает ширину переплета привязки.</span><span class="sxs-lookup"><span data-stu-id="ba1be-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="ba1be-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ba1be-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ba1be-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ba1be-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ba1be-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ba1be-110">Element Information</span></span>



| <span data-ttu-id="ba1be-111">Имя</span><span class="sxs-lookup"><span data-stu-id="ba1be-111">Name</span></span> | <span data-ttu-id="ba1be-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ba1be-112">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="ba1be-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ba1be-113">Element Type</span></span> <br/>   | <span data-ttu-id="ba1be-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="ba1be-114">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="ba1be-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ba1be-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ba1be-116">Документ</span><span class="sxs-lookup"><span data-stu-id="ba1be-116">Document</span></span><br/>                          |
| <span data-ttu-id="ba1be-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba1be-117">Notes</span></span> <br/>          | <span data-ttu-id="ba1be-118">Связано с элементом Документбиндинг</span><span class="sxs-lookup"><span data-stu-id="ba1be-118">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ba1be-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ba1be-119">Structure Content</span></span>

<span data-ttu-id="ba1be-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ba1be-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="ba1be-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="ba1be-121">Structure Properties</span></span>

<span data-ttu-id="ba1be-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ba1be-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ba1be-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="ba1be-123">Property</span></span>                | <span data-ttu-id="ba1be-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ba1be-124">xsi:type</span></span>           | <span data-ttu-id="ba1be-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ba1be-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ba1be-126">DataType</span><span class="sxs-lookup"><span data-stu-id="ba1be-126">DataType</span></span><br/>     | <span data-ttu-id="ba1be-127">строка</span><span class="sxs-lookup"><span data-stu-id="ba1be-127">string</span></span><br/>  | <span data-ttu-id="ba1be-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ba1be-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="ba1be-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ba1be-129">DefaultValue</span></span><br/> | <span data-ttu-id="ba1be-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="ba1be-130">integer</span></span><br/> | <span data-ttu-id="ba1be-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ba1be-131">undefined</span></span><br/>       |
| <span data-ttu-id="ba1be-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ba1be-132">MaxValue</span></span><br/>     | <span data-ttu-id="ba1be-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="ba1be-133">integer</span></span><br/> | <span data-ttu-id="ba1be-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ba1be-134">undefined</span></span><br/>       |
| <span data-ttu-id="ba1be-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="ba1be-135">MinValue</span></span><br/>     | <span data-ttu-id="ba1be-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="ba1be-136">integer</span></span><br/> | <span data-ttu-id="ba1be-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ba1be-137">undefined</span></span><br/>       |
| <span data-ttu-id="ba1be-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ba1be-138">Mandatory</span></span><br/>    | <span data-ttu-id="ba1be-139">Строковый</span><span class="sxs-lookup"><span data-stu-id="ba1be-139">String</span></span><br/>  | <span data-ttu-id="ba1be-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="ba1be-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ba1be-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="ba1be-141">Multiple</span></span><br/>     | <span data-ttu-id="ba1be-142">целое число</span><span class="sxs-lookup"><span data-stu-id="ba1be-142">integer</span></span><br/> | <span data-ttu-id="ba1be-143">1</span><span class="sxs-lookup"><span data-stu-id="ba1be-143">1</span></span><br/>               |
| <span data-ttu-id="ba1be-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="ba1be-144">UnitType</span></span><br/>     | <span data-ttu-id="ba1be-145">строка</span><span class="sxs-lookup"><span data-stu-id="ba1be-145">string</span></span><br/>  | <span data-ttu-id="ba1be-146">мкм</span><span class="sxs-lookup"><span data-stu-id="ba1be-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ba1be-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ba1be-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba1be-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ba1be-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




