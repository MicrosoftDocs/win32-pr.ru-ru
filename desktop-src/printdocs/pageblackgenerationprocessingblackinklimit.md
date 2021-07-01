---
description: Сведения о параметре Пажеблаккженератионпроцессингблаккинклимит. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: пажеблаккженератионпроцессингблаккинклимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118429"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="ca1e3-105">пажеблаккженератионпроцессингблаккинклимит</span><span class="sxs-lookup"><span data-stu-id="ca1e3-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="ca1e3-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ca1e3-106">This topic is not current.</span></span> <span data-ttu-id="ca1e3-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ca1e3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ca1e3-108">Содержимое приложения с меткой указанного именованного цвета должно отображаться во всех цветоделении.</span><span class="sxs-lookup"><span data-stu-id="ca1e3-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="ca1e3-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ca1e3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ca1e3-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ca1e3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ca1e3-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ca1e3-111">Element Information</span></span>



| <span data-ttu-id="ca1e3-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ca1e3-112">Name</span></span> | <span data-ttu-id="ca1e3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ca1e3-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="ca1e3-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ca1e3-114">Element Type</span></span> <br/>   | <span data-ttu-id="ca1e3-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="ca1e3-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="ca1e3-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ca1e3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ca1e3-117">Страница</span><span class="sxs-lookup"><span data-stu-id="ca1e3-117">Page</span></span><br/>                                            |
| <span data-ttu-id="ca1e3-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca1e3-118">Notes</span></span> <br/>          | <span data-ttu-id="ca1e3-119">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="ca1e3-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ca1e3-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="ca1e3-120">Structure Content</span></span>

<span data-ttu-id="ca1e3-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ca1e3-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="ca1e3-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="ca1e3-122">Structure Properties</span></span>

<span data-ttu-id="ca1e3-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ca1e3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ca1e3-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="ca1e3-124">Property</span></span>                | <span data-ttu-id="ca1e3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ca1e3-125">xsi:type</span></span>           | <span data-ttu-id="ca1e3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ca1e3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ca1e3-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ca1e3-127">DataType</span></span><br/>     | <span data-ttu-id="ca1e3-128">строка</span><span class="sxs-lookup"><span data-stu-id="ca1e3-128">string</span></span><br/>  | <span data-ttu-id="ca1e3-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ca1e3-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="ca1e3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ca1e3-130">DefaultValue</span></span><br/> | <span data-ttu-id="ca1e3-131">строка</span><span class="sxs-lookup"><span data-stu-id="ca1e3-131">string</span></span><br/>  | <span data-ttu-id="ca1e3-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="ca1e3-132">undefined</span></span><br/>       |
| <span data-ttu-id="ca1e3-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ca1e3-133">MaxValue</span></span><br/>     | <span data-ttu-id="ca1e3-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="ca1e3-134">integer</span></span><br/> | <span data-ttu-id="ca1e3-135">100</span><span class="sxs-lookup"><span data-stu-id="ca1e3-135">100</span></span><br/>             |
| <span data-ttu-id="ca1e3-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="ca1e3-136">MinValue</span></span><br/>     | <span data-ttu-id="ca1e3-137">целое число</span><span class="sxs-lookup"><span data-stu-id="ca1e3-137">integer</span></span><br/> | <span data-ttu-id="ca1e3-138">0</span><span class="sxs-lookup"><span data-stu-id="ca1e3-138">0</span></span><br/>               |
| <span data-ttu-id="ca1e3-139">Несколько</span><span class="sxs-lookup"><span data-stu-id="ca1e3-139">Multiple</span></span><br/>     | <span data-ttu-id="ca1e3-140">целое число</span><span class="sxs-lookup"><span data-stu-id="ca1e3-140">integer</span></span><br/> | <span data-ttu-id="ca1e3-141">1</span><span class="sxs-lookup"><span data-stu-id="ca1e3-141">1</span></span><br/>               |
| <span data-ttu-id="ca1e3-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca1e3-142">Mandatory</span></span><br/>    | <span data-ttu-id="ca1e3-143">строка</span><span class="sxs-lookup"><span data-stu-id="ca1e3-143">string</span></span><br/>  | <span data-ttu-id="ca1e3-144">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="ca1e3-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ca1e3-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="ca1e3-145">UnitType</span></span><br/>     | <span data-ttu-id="ca1e3-146">строка</span><span class="sxs-lookup"><span data-stu-id="ca1e3-146">string</span></span><br/>  | <span data-ttu-id="ca1e3-147">percent</span><span class="sxs-lookup"><span data-stu-id="ca1e3-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ca1e3-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ca1e3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca1e3-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ca1e3-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




