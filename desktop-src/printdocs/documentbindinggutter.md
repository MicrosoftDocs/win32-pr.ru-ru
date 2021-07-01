---
description: Найдите сведения о параметре Документбиндинггуттер. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: документбиндинггуттер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118469"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="2fb1f-105">документбиндинггуттер</span><span class="sxs-lookup"><span data-stu-id="2fb1f-105">DocumentBindingGutter</span></span>

<span data-ttu-id="2fb1f-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2fb1f-106">This topic is not current.</span></span> <span data-ttu-id="2fb1f-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2fb1f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2fb1f-108">Задает ширину переплета привязки.</span><span class="sxs-lookup"><span data-stu-id="2fb1f-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="2fb1f-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2fb1f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2fb1f-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="2fb1f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2fb1f-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2fb1f-111">Element Information</span></span>



| <span data-ttu-id="2fb1f-112">Имя</span><span class="sxs-lookup"><span data-stu-id="2fb1f-112">Name</span></span> | <span data-ttu-id="2fb1f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb1f-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="2fb1f-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="2fb1f-114">Element Type</span></span> <br/>   | <span data-ttu-id="2fb1f-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="2fb1f-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="2fb1f-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="2fb1f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2fb1f-117">Документ</span><span class="sxs-lookup"><span data-stu-id="2fb1f-117">Document</span></span><br/>                          |
| <span data-ttu-id="2fb1f-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fb1f-118">Notes</span></span> <br/>          | <span data-ttu-id="2fb1f-119">Связано с элементом Документбиндинг</span><span class="sxs-lookup"><span data-stu-id="2fb1f-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2fb1f-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="2fb1f-120">Structure Content</span></span>

<span data-ttu-id="2fb1f-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="2fb1f-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2fb1f-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="2fb1f-122">Structure Properties</span></span>

<span data-ttu-id="2fb1f-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="2fb1f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2fb1f-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="2fb1f-124">Property</span></span>                | <span data-ttu-id="2fb1f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2fb1f-125">xsi:type</span></span>           | <span data-ttu-id="2fb1f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb1f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2fb1f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="2fb1f-127">DataType</span></span><br/>     | <span data-ttu-id="2fb1f-128">строка</span><span class="sxs-lookup"><span data-stu-id="2fb1f-128">string</span></span><br/>  | <span data-ttu-id="2fb1f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2fb1f-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="2fb1f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2fb1f-130">DefaultValue</span></span><br/> | <span data-ttu-id="2fb1f-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="2fb1f-131">integer</span></span><br/> | <span data-ttu-id="2fb1f-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="2fb1f-132">undefined</span></span><br/>       |
| <span data-ttu-id="2fb1f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2fb1f-133">MaxValue</span></span><br/>     | <span data-ttu-id="2fb1f-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="2fb1f-134">integer</span></span><br/> | <span data-ttu-id="2fb1f-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="2fb1f-135">undefined</span></span><br/>       |
| <span data-ttu-id="2fb1f-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="2fb1f-136">MinValue</span></span><br/>     | <span data-ttu-id="2fb1f-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="2fb1f-137">integer</span></span><br/> | <span data-ttu-id="2fb1f-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="2fb1f-138">undefined</span></span><br/>       |
| <span data-ttu-id="2fb1f-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2fb1f-139">Mandatory</span></span><br/>    | <span data-ttu-id="2fb1f-140">Строка</span><span class="sxs-lookup"><span data-stu-id="2fb1f-140">String</span></span><br/>  | <span data-ttu-id="2fb1f-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="2fb1f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2fb1f-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="2fb1f-142">Multiple</span></span><br/>     | <span data-ttu-id="2fb1f-143">целое число</span><span class="sxs-lookup"><span data-stu-id="2fb1f-143">integer</span></span><br/> | <span data-ttu-id="2fb1f-144">1</span><span class="sxs-lookup"><span data-stu-id="2fb1f-144">1</span></span><br/>               |
| <span data-ttu-id="2fb1f-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="2fb1f-145">UnitType</span></span><br/>     | <span data-ttu-id="2fb1f-146">строка</span><span class="sxs-lookup"><span data-stu-id="2fb1f-146">string</span></span><br/>  | <span data-ttu-id="2fb1f-147">мкм</span><span class="sxs-lookup"><span data-stu-id="2fb1f-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="2fb1f-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2fb1f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb1f-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2fb1f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




